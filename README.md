# KMeanClustering

1. Import libraries
    pandas → to handle and process the dataset.
    matplotlib → to plot graphs and visualize clusters.
    KMeans (from scikit-learn) → algorithm for clustering.
    silhouette_score → to evaluate how well clusters are formed.
    PCA → reduces data dimensions for easier visualization.
2. Load dataset
    Reads the Mall Customers dataset (CSV/Excel).
    Contains customer details like CustomerID, Gender, Age, Annual Income, Spending Score.
3. Select features
    We choose Annual Income and Spending Score as input features (X).
    These two variables are the most relevant for customer segmentation.
4. Elbow Method
    Runs K-Means for different cluster numbers (k = 2 → 10).
    Records WCSS (Within-Cluster Sum of Squares) for each k.
    Plots WCSS vs k → the elbow point shows the best number of clusters.
5. Train K-Means
    Applies K-Means with the chosen optimal k (e.g., 5).
    Assigns each customer to one of the clusters (labels).
6. Cluster visualization
    Plots customers on a 2D graph (Annual Income vs Spending Score).
    Each cluster is shown in a different color.
    Centroids (cluster centers) are highlighted with a special marker (e.g., yellow X).
7. Evaluation (Silhouette Score)
    Calculates Silhouette Score → measures cluster quality.
    Near 1 → well-separated clusters.
    Around 0 → overlapping clusters.
    Negative → poor clustering.
