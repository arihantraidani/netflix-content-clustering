# Netflix Content Clustering

An exploration of unsupervised machine learning clustering algorithms to group Netflix's TV shows and movies from the 2019 catalog. This project applies **K-Means**, **Agglomerative Clustering**, and **DBSCAN** to discover patterns and group similar content based on features such as genre, rating, and duration. The goal is to evaluate which clustering algorithm performs best and can potentially be used for content recommendations and insights into user preferences.

---

## **Table of Contents**

- [Overview](#overview)
- [Models Used](#models-used)
- [Installation](#installation)
- [How to Run](#how-to-run)
- [Evaluation](#evaluation)
- [Future Work](#future-work)
- [License](#license)

---

## **Overview**

This project uses unsupervised machine learning to analyze Netflix's 2019 TV show and movie dataset. We apply three different clustering algorithms—**K-Means**, **Agglomerative Clustering**, and **DBSCAN**—to group content based on similar features. The **Silhouette Score** is used to evaluate the clustering quality, with the aim of finding the best model for segmenting Netflix content. 

---

## **Models Used**

1. **K-Means Clustering**: A centroid-based algorithm that groups data points into `k` clusters, optimizing the centroids to minimize the variance within each cluster.
2. **Agglomerative Clustering**: A hierarchical clustering algorithm that merges closest clusters based on a distance metric, offering flexibility with different linkage methods.
3. **DBSCAN (Density-Based Spatial Clustering of Applications with Noise)**: A density-based algorithm that forms clusters based on the density of points, capable of detecting noise as outliers.

---

## **Installation**

Clone this repository to your local machine:

```bash
git clone https://github.com/your-username/netflix-content-clustering.git
```

Install the required dependencies:

```bash
pip install -r requirements.txt
```

---

## **How to Run**

1. **Download the Dataset**: Ensure you have the dataset containing Netflix’s 2019 TV shows and movies.
2. **Run the Code**: Use Jupyter Notebook or any Python environment to run the provided code.
   
```bash
python clustering_model.py
```

The code will execute the clustering algorithms, evaluate the models using the Silhouette Score, and display the results.

---

## **Evaluation**

The performance of each model is evaluated using the **Silhouette Score**, which measures how well-separated and compact the clusters are. A higher score indicates better-defined clusters.

- **K-Means**: Silhouette Score = 0.026
- **Agglomerative Clustering**: Silhouette Score = 0.151 (after tuning)
- **DBSCAN**: Silhouette Score = -0.191

**Agglomerative Clustering** performed the best, though there is room for improvement. Further work can involve exploring more sophisticated models and improving preprocessing techniques.

---

## **Future Work**

- **Model Improvement**: Experiment with other clustering techniques like **Gaussian Mixture Models (GMM)** or **Spectral Clustering** to improve cluster quality.
- **Deployment**: Deploy the best model for real-time content segmentation or as part of a recommendation system.
- **Feature Engineering**: Incorporate additional features like user behavior data, reviews, or external datasets (e.g., IMDB ratings).

