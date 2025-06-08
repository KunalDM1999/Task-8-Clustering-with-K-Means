# Task-8-Clustering-with-K-Means clustering.

  1. Dataset Used:
   
 You used the Volcano Eruptions dataset from Kaggle with 958 entries and 26 features, including location, elevation, and nearby population exposure.
 
  2. Feature Selection:

 Selected 7 numeric features that are continuous and relevant for clustering:
 latitude, longitude, elevation, population_within_5_km, population_within_10_km, population_within_30_km, and population_within_100_km.
 Excluded high-cardinality categorical features (e.g., country, region, tectonic_settings) to avoid sparse and noisy encodings.

 3. Preprocessing (3 Key Steps):

* Log Transformation: Applied np.log1p() to skewed features to reduce the effect of extreme values.

* Winsorization: Used 5% winsorization on elevation to cap outliers instead of removing data.

* Standardization: Applied StandardScaler() to all selected features to normalize scale for distance-based clustering.

 4. Clustering – KMeans Fit:
   
K-Means clustering was performed using k=3, and cluster labels were assigned to each volcano in a new cluster column.

5. 2D PCA Visualization:
   
Reduced the 7-dimensional feature space to 2 principal components using PCA and visualized the clusters on a 2D scatter plot with color-coded labels.

6. 3D PCA Visualization (for K=2):
   
You also generated a 3D PCA plot using the top 3 components to visualize volcano clusters spatially in 3D, specifically for k=2 clusters.

7. Elbow Method (K Optimization):
    
Plotted the inertia vs. number of clusters to identify the “elbow point” and determine the most suitable value for k.

8. Silhouette Score (Clustering Evaluation):
    
Computed the Silhouette Score to measure cluster separation. The best score was around 0.64 for K=2, indicating moderately well-separated clusters.

9. Final Output – v_data DataFrame:
    
The final dataset includes all preprocessed features, a cluster label, and PCA components. It’s ready for interpretation, analysis, or further modeling.

10. Libraries and Tools Used:

* Pandas, NumPy – data manipulation

* scikit-learn – StandardScaler, KMeans, PCA, silhouette_score

* scipy – winsorize for outlier capping

* Matplotlib, Seaborn, mpl_toolkits.mplot3d – 2D and 3D visualization
