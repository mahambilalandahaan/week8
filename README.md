# K-Means Deep Dive 🧠

This project provides an in-depth exploration of the **K-Means Clustering Algorithm** using both the **Elbow Method** and the **Silhouette Method** to determine the optimal number of clusters.  
It demonstrates key unsupervised learning concepts with visualizations and metric-based evaluation.

---

## 📘 Project Overview

Clustering is a core unsupervised machine learning technique that groups similar data points together.  
In this notebook, we:
- Generate a synthetic dataset using `make_blobs`
- Apply the **Elbow Method** to analyze inertia and identify the "knee point"
- Apply the **Silhouette Method** to evaluate cluster quality
- Visualize both methods for comparison

---

## 🧩 Technologies Used

- **Python 3**
- **Matplotlib** — for plotting curves
- **Scikit-learn (sklearn)** — for clustering and evaluation metrics

---

## 📂 File Description

| File | Description |
|------|--------------|
| `kmeans_deepdive.ipynb` | Jupyter Notebook containing the complete implementation of K-Means clustering with Elbow and Silhouette methods. |

---

## ⚙️ How It Works

### 1. Generate Dataset
A synthetic dataset of 300 samples and 4 centers is created using:
```python
from sklearn.datasets import make_blobs
x, y = make_blobs(n_samples=300, centers=4, cluster_std=1.2, random_state=42)
### 2. Elbow Method

Iterates over k values (1–24) to record inertia and plot the Elbow Curve.

### 3. Silhouette Method

Iterates over k values (2–24) to calculate silhouette scores and plot the Silhouette Curve.

### 4. Visual Insights

Both curves are visualized using Matplotlib for comparison and cluster analysis.

## 📊 Example Outputs

Elbow Curve: Shows the reduction in inertia with increasing k.
![Elbow Curve](elbow_curve(1).png)

Silhouette Curve: Indicates how well-defined the clusters are for each k.

![Silhouette Curve](silhouette_curve(1).png)

### 🚀 How to Run

Clone this repository:

git clone https://github.com/mahambilalandahaan/week8.git


Open the notebook:

jupyter notebook kmeans_deepdive.ipynb


Run all cells to visualize results.

** 🧠 Insights

The Elbow Method helps estimate where adding more clusters yields diminishing returns.

The Silhouette Method provides a more reliable measure by evaluating how well-separated the clusters are.

In this dataset, both methods suggest k = 4 as the optimal number of clusters.
