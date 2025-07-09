# Customer-Segmentation-using-KMeans-Clustering
# 👥 Customer Segmentation using KMeans Clustering

A machine learning project that segments customers into meaningful clusters based on their demographics and spending behavior. Built for marketing and business intelligence use cases using Python, scikit-learn, and Plotly.

---

## 📌 Project Overview

Retail and service companies need to personalize campaigns. This project enables:

* Understanding customer types via clustering
* Segmenting based on age, income, spending
* Visualizing clusters in 2D and 3D

---

## 🛠️ Tech Stack

* **Python** – ML logic
* **scikit-learn** – KMeans algorithm
* **Pandas** – Data wrangling
* **Plotly / Seaborn** – Cluster visualization

---

## 📁 Folder Layout

```
CustomerSegmentation/
├── data/
│   └── customers.csv
├── model/
│   └── cluster_model.pkl
├── segment.py
├── visuals.py
└── README.md
```

---

## 💻 Features

* 🧠 Applies KMeans clustering
* 📊 Elbow method to choose K
* 🖼️ 2D scatter + 3D cluster plots
* 📤 Export clustered CSV

---

## 🧠 Theory

* KMeans minimizes intra-cluster variance
* Normalizes input before clustering
* Finds cluster centers and labels customers

---

## 🔣 Sample Code

```python
from sklearn.cluster import KMeans
import pandas as pd
import matplotlib.pyplot as plt

# Load & scale
df = pd.read_csv('data/customers.csv')
x = df[['Age', 'Income', 'SpendingScore']]

# Elbow method
inertia = []
for k in range(1, 11):
    model = KMeans(n_clusters=k).fit(x)
    inertia.append(model.inertia_)

plt.plot(range(1, 11), inertia)
plt.title('Elbow Curve')
plt.xlabel('K')
plt.ylabel('Inertia')
plt.show()
```

---

## 📈 Business Use Cases

* 🎯 Targeted marketing by segment
* 🛍️ Loyalty programs for high-spenders
* 📈 Behavioral clustering for growth

---

## 👨‍💻 Author Info

**Pranjal Gurjar**
MCA Final Year – Data Science Project
📧 [gurjarpranjal.work@gmail.com](mailto:gurjarpranjal.work@gmail.com)
