# Logistic Regression via IRLS (R) — Unregularized vs L2 Regularized

A simple, from-scratch implementation of **logistic regression** using the **Iteratively Reweighted Least Squares (IRLS)** algorithm in **R**, comparing **unregularized** and **L2-regularized** models across multiple data scenarios (perfectly separable, outliers, overlapping, class imbalance, and train–test evaluation).

---

## 🔍 Project Overview

- Build IRLS **from scratch** in R (no `glm()`).
- Compare **Unregularized** vs **L2 Regularized** logistic regression.
- Study the effect of **separability**, **outliers**, **overlap**, **dataset size**, and **class balance**.
- Keep code **simple** and easy to run; works for **any number of predictors `m`**.

---

## 🧠 Key Findings (Short)

- On **perfectly separable** data, both models reach **100% accuracy**, but **unregularized β diverges**; L2 keeps β **small and stable**.
- With **outliers** and **overlap**, L2 **reduces sensitivity** and improves **stability/generalization**; unregularized can **explode**.
- With **imbalanced** or different **sizes**, accuracy may look similar, but L2 yields **more reliable coefficients**.

---

## 📁 Repository Structure (suggested)

├─ R/ # R scripts
│ ├─ irls_utils.R # IRLS functions (unreg + L2), helpers
│ └─ run_all_steps.R # Main script: reproduces all steps and prints results
├─ figures/ # Saved plots (optional)
├─ report/ # LaTeX report (abstract, objectives, intro, etc.)
│ └─ main.tex
└─ README.md

---

## ⚙️ Setup

1. Install R (≥ 4.0)
2. (Optional) Install helpful packages for plotting:
   ```r
   install.packages(c("ggplot2"))
