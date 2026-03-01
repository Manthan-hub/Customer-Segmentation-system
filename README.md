# Customer Segmentation System (K-Means Clustering)

This project performs **customer segmentation** using the classic *Mall Customers* dataset. It follows a practical analytics workflow: **EDA → feature selection → scaling → K-Means clustering → cluster visualization → segment profiling**.

The goal is to identify distinct customer groups (segments) based on behavior and demographics, which can be used for **targeted marketing**, **personalized offers**, and **customer strategy**.

---

## Dataset

- File: `Mall_Customers.csv`
- Common fields in this dataset:
  - `Gender`
  - `Age`
  - `Annual Income (k$)`
  - `Spending Score (1-100)`

---

## What This Project Does

### 1) Exploratory Data Analysis (EDA)
- Basic dataset inspection (shape, missing values, summary stats)
- Distribution plots for key features (Age, Income, Spending Score)
- Quick category insights (e.g., Gender distribution)

### 2) Customer Segmentation (K-Means)
- Scales numeric features (so clustering is not biased by units)
- Uses K-Means clustering to segment customers
- Supports selecting **optimal K** using an elbow-style approach (and/or silhouette depending on your implementation)

### 3) Visualizations
- Cluster visualization using 2D projection (PCA)
- Clear plots to understand separation between segments

### 4) Segment Profiling (Business Interpretation)
After clustering, the project creates a **cluster profile** to make the results useful for business decisions.  
For each segment (cluster), it summarizes:

- **Cluster size** (number of customers)
- **Average Age**
- **Average Annual Income**
- **Average Spending Score**

This helps convert “clusters” into interpretable groups such as:
- High income + high spending (premium customers)
- High income + low spending (potential upsell targets)
- Low income + high spending (value seekers / promotions-sensitive)
- Low income + low spending (low-engagement customers)

> The exact segment labels depend on the cluster centers produced by the model.

---

## How to Run

### 1) Install dependencies
```bash
pip install -r requirements.txt
