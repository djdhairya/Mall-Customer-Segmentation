# Mall Customer Segmentation

## Overview
This project focuses on customer segmentation using the Mall Customers dataset. The goal is to cluster customers based on their spending behavior and annual income using K-Means clustering.

## Dataset
The dataset used is `Mall_Customers.csv`, which contains the following columns:
- **CustomerID**: Unique identifier for each customer.
- **Gender**: Gender of the customer (Male/Female).
- **Age**: Age of the customer.
- **Annual Income (k$)**: Annual income of the customer in thousand dollars.
- **Spending Score (1-100)**: Score assigned by the mall based on customer spending behavior.

## Dependencies
Ensure you have the following Python libraries installed:
```python
pip install pandas numpy matplotlib seaborn scikit-learn
```

## Implementation Steps

### 1. Import Libraries
```python
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns
from sklearn.cluster import KMeans
%matplotlib inline
```

### 2. Load Data
```python
df = pd.read_csv("data/Mall_Customers.csv")
df.info()
df.describe()
```

### 3. Data Cleaning & Analysis
- Checking for missing values.
- Analyzing the distribution of `Annual Income`, `Age`, and `Spending Score` using histograms.
- Visualizing gender distribution.

### 4. K-Means Clustering
#### 4.1 Clustering using Annual Income & Spending Score
- Finding the optimal number of clusters using the Elbow method.
- Applying K-Means clustering and visualizing the clusters.

#### 4.2 Clustering using Age, Annual Income & Spending Score
- Finding the optimal number of clusters using the Elbow method.
- Applying K-Means clustering in 3D space and visualizing using `mpl_toolkits.mplot3d`.

### 5. Results
Customers are segmented into 5 groups based on their spending behavior:
- **Cluster 1**: High income, high spending.
- **Cluster 2**: High income, low spending.
- **Cluster 3**: Average income, average spending.
- **Cluster 4**: Low income, high spending.
- **Cluster 5**: Low income, low spending.

### 6. Visualizations
- Histograms for feature distributions.
- Scatter plots for 2D clusters.
- 3D scatter plot for Age, Annual Income, and Spending Score segmentation.

## Conclusion
This project demonstrates how clustering techniques like K-Means can be used to segment customers based on their purchasing behavior. The insights gained can help businesses personalize marketing strategies and improve customer experience.

## Author
Dhairya Hindoriya

## License
This project is open-source and available for use under the MIT License.

