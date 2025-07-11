# 🎯 Recommender System Evaluation: Performance of Five Algorithms

This project evaluates and compares five recommender system algorithms using collaborative filtering techniques on the MovieLens dataset. The work was completed as part of the **Practical Data Science with Python** course in the **Master of Data Science** program at RMIT University.

---

## 📘 Overview

The following five methods were implemented and compared:

|  Method |                Description             |  Personalization | Fallback Strategy |
|---------|----------------------------------------|------------------|-------------------|
|   M1    |               User Average             |        ❌        |        -          |
|   M2    |               Item Average             |        ❌        |        -          |
|   M3    | User-based KNN Collaborative Filtering |        ✅        |   User average    |
|   M4    | Item-based KNN Collaborative Filtering |        ✅        |   Item average    |
|   M5    |          Hybrid (User + Item KNN)      |        ✅        |   User average    |

Each method aims to predict user ratings for unseen items and is evaluated using **Mean Absolute Error (MAE)** and **Root Mean Squared Error (RMSE)**.

---

## 🧠 Key Highlights

- **User-based and Item-based collaborative filtering** use cosine similarity to identify top-K similar users or items.
- **Hybrid approach** (Method 5) blends predictions from user- and item-based models for better robustness.
- Evaluated performance across **K = [3, 5, 7, 10]** for personalized models (M3–M5).

---

## 📊 Results Summary

### MAE (Lower is better)

| K | M3 (User-KNN) | M4 (Item-KNN) | M5 (Hybrid) |
|---|---------------|---------------|-------------|
| 3 | 0.8593        | 0.7783        | 0.7478      |
| 5 | 0.8247        | 0.7570        | 0.7329      |
| 7 | 0.8074        | 0.7499        | 0.7272      |
|10 | 0.7950        | 0.7443        | **0.7234**  |

### RMSE (Lower is better)

| K | M3 (User-KNN) | M4 (Item-KNN) | M5 (Hybrid) |
|---|---------------|---------------|-------------|
| 3 | 1.0953        | 1.0249        | 0.9574      |
| 5 | 1.0431        | 0.9845        | 0.9362      |
| 7 | 1.0207        | 0.9691        | 0.9281      |
|10 | 1.0040        | 0.9612        | **0.9237**  |

📌 The **Hybrid model (M5)** consistently achieved the **lowest MAE and RMSE**, making it the most accurate and robust among the tested methods.

---

## 📁 Files in This Repository

|             File                   |                                     Description                                                     |
|------------------------------------|-----------------------------------------------------------------------------------------------------|
| `Assignment3_framework_2025.ipynb` | Jupyter notebook with full implementation of the five algorithms, evaluation, and performance plots |
|          `Slides.pdf`              |       Visual report summarizing the methodology, optimizations, and result interpretations          |
|        `requirements.txt`          |                       Python dependencies for running the notebook                                  |

---

## 📊 Visualizations

The notebook includes MAE and RMSE line plots for:
- Method 3 (User-KNN)
- Method 4 (Item-KNN)
- Method 5 (Hybrid)

These plots clearly illustrate how prediction accuracy improves with increasing values of K.

---

## 🧾 How to Run

### 1. Clone the repository
```bash
git clone https://github.com/YOUR_USERNAME/recommender-systems-evaluation.git
cd recommender-systems-evaluation
