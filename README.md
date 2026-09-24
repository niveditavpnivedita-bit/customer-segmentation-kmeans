# Customer Segmentation Using K-Means Clustering

## 📌 Project Overview

This project focuses on segmenting retail store customers using the
**K-Means Clustering** algorithm, an unsupervised machine learning technique.

Customers are grouped based on their **Annual Income** and **Spending Score**.
The purpose of this project is to identify different customer segments
based on their purchasing behavior.

---

## 🎯 Objective

The main objective of this project is to:

- Analyze customer purchasing data.
- Identify groups of customers with similar characteristics.
- Apply the K-Means clustering algorithm.
- Determine the appropriate number of clusters using the Elbow Method.
- Visualize and analyze the resulting customer segments.

---

## 📊 Dataset

The project uses the **Mall Customer Segmentation** dataset.

The dataset contains **200 customers** and the following columns:

| Column | Description |
|---|---|
| CustomerID | Unique ID assigned to each customer |
| Gender | Gender of the customer |
| Age | Age of the customer |
| Annual Income (k$) | Annual income of the customer |
| Spending Score (1-100) | Spending score assigned to the customer |

---

## 🛠️ Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Google Colab
- Jupyter Notebook

---

## 🔍 Project Workflow

The project follows these steps:

1. Import required Python libraries.
2. Load the customer dataset.
3. Explore the dataset.
4. Check for missing values.
5. Perform exploratory data analysis.
6. Select Annual Income and Spending Score as clustering features.
7. Visualize the customer data.
8. Use the Elbow Method to determine the number of clusters.
9. Apply the K-Means clustering algorithm.
10. Assign customers to clusters.
11. Visualize the customer segments.
12. Analyze the characteristics of each cluster.

---

## 📈 Elbow Method

The **Elbow Method** is used to determine a suitable value of K
(number of clusters).

The method evaluates the Within-Cluster Sum of Squares (WCSS) for
different values of K.

For this project, **5 clusters** were selected based on the Elbow Method.

---

## 🤖 K-Means Clustering

K-Means clustering divides the customers into groups based on similarity
in their annual income and spending score.

The model was implemented using Scikit-learn:

```python
from sklearn.cluster import KMeans

kmeans = KMeans(
    n_clusters=5,
    random_state=42,
    n_init=10
)

y_kmeans = kmeans.fit_predict(X)
