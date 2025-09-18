# Unsupervised Learning with PCA and KMeans on Wine & MNIST Datasets

This project demonstrates the application of **unsupervised learning** techniques — specifically **dimensionality reduction** using **Principal Component Analysis (PCA)** and **clustering** with the **K-Means algorithm** — on two benchmark datasets:

* **MNIST handwritten digits dataset**
* **Wine dataset** from scikit-learn (UCI repository)

---

## Project Overview

The main goal is to explore how unsupervised learning can discover hidden structures in high-dimensional data without relying on labels.

### 1. MNIST Dataset

* Applied **KMeans clustering** with 10 clusters on digit images.
* Reduced the dimensionality using **PCA** to 2 components for visualization.
* Visualized clusters to see how well digits are grouped.

### 2. Wine Dataset

* Contains **178 samples** with **13 chemical features** describing wines from 3 cultivators.
* **Preprocessing:** Standardized features using `StandardScaler`.
* **Dimensionality Reduction:** Applied PCA to reduce 13 features to 2 principal components.
* **Clustering:** Used **KMeans** with 3 clusters (to match actual classes).
* **Evaluation:** Computed **Silhouette Score** to measure clustering quality.
* **Visualization:** Plotted clusters and **cluster centers** using:

  * **Matplotlib** (scatter plot with centroids)
  * **OpenCV** (canvas visualization with points and centroids)
* **Exploratory Analysis:** Feature distributions (histograms) and a **correlation heatmap** for feature relationships.

---

## Results

* **MNIST:** Cluster centers resemble digits even without labels. PCA-based visualization shows some overlap but captures meaningful digit structures.
* **Wine Dataset:** PCA + KMeans produces well-separated clusters with a good **silhouette score**, confirming meaningful grouping.

---

## How to Run

### Requirements

Install dependencies:

```bash
pip install numpy pandas matplotlib seaborn scikit-learn opencv-python
```

### Run the Notebook

1. Open the Jupyter Notebook:

   ```
   10-unsupervised-learning-with-dimensionality-reduction.ipynb
   ```
2. Run all cells step by step.
3. Visualizations will be displayed inline, and OpenCV windows will pop up for cluster views.

---

## Dataset

* **Wine Dataset:** Available in scikit-learn (`load_wine`) or [UCI Repository](https://archive.ics.uci.edu/ml/datasets/wine).
* **MNIST Dataset:** Available in scikit-learn (`load_digits`) or keras datasets.

---

## Evaluation Metric

The **Silhouette Score** is used to measure clustering quality:

* **+1:** Well-separated, compact clusters.
* **0:** Overlapping clusters.
* **–1:** Poor clustering, incorrect assignments.

---

## Key Learnings

* Importance of **feature scaling** before clustering.
* PCA helps in **dimensionality reduction** and **visualization** while preserving variance.
* KMeans + Silhouette Score is an effective pipeline for validating unsupervised clustering.

---

## Author

Manolina Das
