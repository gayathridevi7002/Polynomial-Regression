# 📈 Polynomial Regression — ML Web Project

> A web-based interactive machine learning project demonstrating **Polynomial Regression** — built as a single HTML file with no frameworks or installations required.

---

## 📌 Project Overview

This project is submitted as part of the **Category 2: Machine Learning** web-based assignment. It covers the complete study of Polynomial Regression — from concept explanation to interactive visualization — all within a single self-contained HTML file.

**Topic:** Polynomial Regression  
**Category:** Machine Learning (Category 2)  
**Tech Stack:** HTML · CSS · Vanilla JavaScript · Chart.js  

---

## 📂 Project Structure

```
polynomial-regression/
│
├── polynomial_regression.html    ← Main project file (open this in a browser)
└── README.md                     ← This file
```

> The entire project lives in **one HTML file**. No installations, no servers, no dependencies to install — just open it in any browser.

---

## ✅ Features

### 1. Concept Description
- Clear definition of Polynomial Regression
- Step-by-step explanation of how the algorithm works
- Formula breakdown with all variables explained
- Table of important parameters (degree, coefficients, R², MSE, overfitting)
- Real-world applications (engineering, medicine, finance, automotive)

### 2. Worked Example (By Hand)
- Manual step-by-step walkthrough using a 5-point dataset
- Shows: Design Matrix → Normal Equations → Coefficients → Predictions
- Degree-2 polynomial solved from scratch

### 3. Video Explanation
- Embedded YouTube video: *StatQuest — Polynomial Regression* by Josh Starmer

### 4. Interactive Playground
- **Three input modes:**
  - ✏️ Manual entry (type x, y pairs)
  - 📂 CSV file upload (two-column CSV)
  - 🎲 Preset datasets (quadratic, cubic, sine, exponential-like)
- **Controls:** Choose polynomial degree (1–6) and train/test split percentage
- **Step-by-step execution log** showing all 7 algorithm steps
- **Live chart** with training points, test points, and fitted curve
- **Metrics panel:** R², MSE, RMSE for both train and test sets

### 5. References
- Textbook references with direct links
- Official documentation and educational websites

---

## 🚀 How to Run

1. Download `polynomial_regression.html`
2. Open it in any modern browser (Chrome, Firefox, Edge, Safari)
3. No internet connection needed for the interactive section *(video requires internet)*

---

## 🗃️ Recommended Datasets

You can use any two-column CSV (x values, y values) in the Upload tab.

| Dataset | Source | Good for Degree |
|---|---|---|
| Position vs Salary | [Download](https://raw.githubusercontent.com/dsrscientist/dataset1/master/Position_Salaries.csv) | 3 |
| Salary vs Experience | [Download](https://raw.githubusercontent.com/dsrscientist/dataset1/master/Salary_Data.csv) | 2 |
| Boston Housing | [Kaggle](https://www.kaggle.com/datasets/schirmerchad/bostonhoustingmlnd) | 2–3 |

**CSV format expected:**
```
1, 45000
2, 50000
3, 60000
...
```
*(First column = x, Second column = y. Header row is optional and will be skipped if non-numeric.)*

---

## 📐 Algorithm Used

**Ordinary Least Squares (OLS) via Normal Equations**

```
β = (XᵀX)⁻¹ Xᵀy
```

The design matrix X is constructed by expanding each input x into polynomial features:

```
X = [1,  x,  x²,  x³,  ...,  xⁿ]
```

The system of normal equations is solved using **Gaussian elimination with partial pivoting** — implemented from scratch in vanilla JavaScript (no ML libraries used).

---

## 📊 Evaluation Metrics

| Metric | Formula | Meaning |
|---|---|---|
| **MSE** | Σ(y − ŷ)² / n | Mean squared error |
| **RMSE** | √MSE | Root mean squared error (same units as y) |
| **R²** | 1 − SSres/SStot | Proportion of variance explained (1 = perfect) |

---

## 📚 References

| Type | Reference |
|---|---|
| 📘 Textbook | Aurélien Géron — *Hands-On Machine Learning*, Ch. 4 → [O'Reilly](https://www.oreilly.com/library/view/hands-on-machine-learning/9781492032632/ch04.html) |
| 📗 Textbook | James et al. — *Introduction to Statistical Learning*, Ch. 7 → [statlearning.com](https://www.statlearning.com/) |
| 🌐 Docs | Scikit-Learn PolynomialFeatures → [scikit-learn.org](https://scikit-learn.org/stable/modules/generated/sklearn.preprocessing.PolynomialFeatures.html) |
| 🎓 Course | Andrew Ng — Machine Learning Specialization → [Coursera](https://www.coursera.org/learn/machine-learning) |
| 📄 Tutorial | GeeksforGeeks → [Polynomial Regression in Python](https://www.geeksforgeeks.org/python-implementation-of-polynomial-regression/) |
| ▶️ Video | StatQuest — Polynomial Regression → [YouTube](https://www.youtube.com/watch?v=Q81RR3yKn30) |

---

## 🧠 Key Concepts Covered

- What is Polynomial Regression and why it's used over Linear Regression
- Feature transformation: converting x → [1, x, x², …, xⁿ]
- Normal equations and OLS derivation
- Overfitting vs underfitting with degree selection
- Train/test split and model evaluation
- Visualization of curve fitting

---

## ⚠️ Notes

- Degrees above 5 may cause overfitting on small datasets — the app will warn you
- For very noisy data, lower degrees (2–3) often generalise better
- The algorithm is implemented in pure JavaScript — no Python or external ML libraries are used

---

*Polynomial Regression · Machine Learning Web Project*
