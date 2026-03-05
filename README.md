# 🌙 DBSCAN Clustering on Iris and Non-Linear Dataset

---

# 📌 Project Overview

This project demonstrates the use of **DBSCAN (Density-Based Spatial Clustering of Applications with Noise)**, an unsupervised machine learning algorithm used to identify clusters based on the density of data points.

Unlike traditional clustering methods that assume clusters are spherical, DBSCAN is capable of discovering **clusters of arbitrary shapes** and also identifying **noise or outliers** in the dataset.

In this project, DBSCAN is applied to:

- The **Iris dataset**
- A **non-linear dataset generated using `make_moons`**

The objective is to understand how DBSCAN groups data points based on density and how it performs on both structured and complex datasets.

---

# 📂 Dataset

## 🌸 Iris Dataset

The **Iris dataset** is a well-known dataset used for machine learning experiments.

Dataset characteristics:

- **150 samples**
- **3 species of iris flowers**
  - Setosa
  - Versicolor
  - Virginica

Each sample contains four numerical features:

- Sepal Length
- Sepal Width
- Petal Length
- Petal Width

Although labels are available in the dataset, they are **not used during clustering**, since clustering is an **unsupervised learning method**.

---

## 🌙 Non-Linear Dataset (`make_moons`)

To evaluate DBSCAN on complex cluster shapes, a **synthetic non-linear dataset** was generated using the `make_moons` function.

Dataset characteristics:

- Two **interleaving crescent-shaped clusters**
- Non-linear structure
- Possible noise points

This dataset is commonly used to test clustering algorithms that need to identify **non-linear patterns**.

---

# ⚙️ DBSCAN Algorithm

DBSCAN is a **density-based clustering algorithm** that groups together points that are closely packed while marking points that lie alone as noise.

Instead of relying on centroids, DBSCAN focuses on **density regions**.

The algorithm requires two important parameters:

### ε (Epsilon)

The maximum distance between two points for them to be considered neighbors.

### MinPts (Minimum Points)

The minimum number of points required within the epsilon radius to form a dense region.

---

# 🔍 Types of Points in DBSCAN

DBSCAN classifies data points into three categories:

### Core Point

A point that has at least **MinPts neighbors within the epsilon distance**.

### Border Point

A point that has fewer neighbors than MinPts but lies within the neighborhood of a core point.

### Noise Point

A point that does not belong to any cluster and is considered an **outlier**.

---

# 📊 Experiments

## 1️⃣ DBSCAN on Iris Dataset

Steps performed:

- Data preprocessing
- Parameter selection for epsilon and MinPts
- Applying DBSCAN clustering
- Visualizing resulting clusters

Observation:

Some clusters are successfully detected, while certain points may be labeled as **noise depending on the parameter values**.

---

## 2️⃣ DBSCAN on Non-Linear Dataset (`make_moons`)

The `make_moons` dataset contains curved cluster structures.

Observation:

- DBSCAN correctly identifies the **two moon-shaped clusters**
- The algorithm follows the **natural shape of the data**
- Noise points can be detected automatically

This demonstrates the advantage of DBSCAN when working with **non-linear datasets**.

---

# 📈 Key Observations

| Dataset | Result |
|--------|--------|
| Iris Dataset | DBSCAN detects clusters but results depend on parameter selection |
| make_moons Dataset | DBSCAN successfully detects curved clusters |

Important insights:

- DBSCAN performs well on **arbitrary-shaped clusters**.
- It automatically identifies **noise points**.
- It does **not require specifying the number of clusters beforehand**.

---

# 🛠 Technologies Used

- Python  
- NumPy  
- Pandas  
- Matplotlib  
- Scikit-learn  

---

# 📊 Output

The project generates visualizations such as:

- Cluster plots for the **Iris dataset**
- Cluster visualization for the **non-linear `make_moons` dataset**

These visualizations help illustrate how DBSCAN groups data points based on density.

---

# 🎯 Conclusion

DBSCAN is a powerful clustering algorithm for detecting patterns in datasets where clusters may not follow simple geometric shapes.

Key takeaways from this project:

- DBSCAN clusters points based on **density rather than distance to centroids**.
- It is effective for **non-linear and irregular cluster structures**.
- The algorithm can automatically detect **noise and outliers**.

Understanding DBSCAN helps in solving real-world problems where cluster shapes are **complex and unpredictable**.

---

## 👩‍💻 Author
**Vaishnavi Rathi**
