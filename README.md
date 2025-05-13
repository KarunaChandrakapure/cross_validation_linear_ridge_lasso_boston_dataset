
# Cross-Validation in Linear, Ridge, and Lasso Regression

This project demonstrates the concept of **cross-validation (CV)** and how it is applied to **Linear, Ridge, and Lasso Regression** models using the **Boston Housing dataset**.

---

## 📚 What is Cross-Validation?

**Cross-validation** is a technique to:
- **Estimate the performance of a model on unseen data**.
- **Prevent overfitting or underfitting** by validating the model across multiple data splits.
- The most common type is **K-Fold Cross-Validation**, where the data is split into `k` parts and the model is trained `k` times, each time using a different fold as validation.

### Benefits:
- Gives a **robust estimate of model generalization**.
- Helps **select hyperparameters (like alpha in Ridge/Lasso)**.

---

## 📊 Models Used

### 1. Linear Regression
- No regularization.
- Uses **cross-validation to check MSE across folds only** (no tuning).

### 2. Ridge Regression
- Adds **L2 penalty (`alpha`)**.
- Uses **cross-validation to tune `alpha`** and plot **alpha vs MSE curve**.

### 3. Lasso Regression
- Adds **L1 penalty (`alpha`)**.
- Uses **cross-validation to tune `alpha`** and plot **alpha vs MSE curve**.
- Requires careful setting of `max_iter` for solver convergence.

---

## 🗂 Contents

- `house_boston.ipynb` — Notebook demonstrating:
  - Cross-validation in **Linear Regression**.
  - **Alpha tuning with CV** in **Ridge** and **Lasso**.
  - Plotting of **MSE across folds** and **MSE vs Alpha curves**.

---

## 💡 Key Learning Points

| Model            | Regularization | Cross-Validation Use                             | Key Plot                      |
|------------------|----------------|--------------------------------------------------|-------------------------------|
| Linear Regression | None           | Evaluate model stability across folds           | MSE per fold                  |
| Ridge Regression  | L2 (`alpha`)   | Tune `alpha` using CV, avoid overfitting        | Alpha vs MSE                  |
| Lasso Regression  | L1 (`alpha`)   | Tune `alpha` using CV, enforce sparsity         | Alpha vs MSE                  |

---

## 🚀 How to Run

1. Open the notebook `house_boston.ipynb`.
2. Run all cells.
3. Check the CV results and plots for all models.

---

## ✅ Requirements

- Python 3.x
- scikit-learn
- numpy
- matplotlib

Install via:
```bash
pip install scikit-learn numpy matplotlib
```

---

## 📎 References

- [Scikit-Learn Documentation](https://scikit-learn.org/stable/)
- [Cross-Validation Guide](https://scikit-learn.org/stable/modules/cross_validation.html)
- [Ridge Regression](https://scikit-learn.org/stable/modules/generated/sklearn.linear_model.Ridge.html)
- [Lasso Regression](https://scikit-learn.org/stable/modules/generated/sklearn.linear_model.Lasso.html)
