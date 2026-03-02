# Heart Disease Prediction

## Overview
This project builds a binary classification model to predict whether a patient is at risk of heart disease based on clinical health data. I used the Heart Disease UCI Dataset (available on Kaggle) and compared two models — Logistic Regression and Decision Tree — to see which performs better.

---

## Dataset
**Heart Disease UCI Dataset**
- 303 patient records, 13 clinical features
- Target: 0 = No heart disease, 1 = Heart disease present
- Features include age, sex, chest pain type, resting blood pressure, cholesterol, max heart rate, and more

---

## Models Applied
- **Logistic Regression** – a linear classifier well-suited for binary medical outcomes
- **Decision Tree (max depth = 5)** – a tree-based model that also provides interpretable feature importance scores

---

## Results and Findings

| Metric | Logistic Regression | Decision Tree |
|--------|-------------------|--------------|
| Accuracy | ~85% | ~80% |
| ROC-AUC | ~0.91 | ~0.84 |

Logistic Regression was the stronger performer overall, achieving better accuracy and a higher AUC score.

**Most important features affecting prediction:**
- `cp` (chest pain type) — strongest predictor
- `thalach` (max heart rate achieved) — patients with higher max HR more likely to have disease
- `exang` (exercise-induced angina) — significant risk indicator
- `oldpeak` (ST depression) — higher values associated with disease presence

The dataset was mostly clean, with a few missing values handled using median imputation. No severe class imbalance was found.

---

## How to Run
```bash
pip install pandas numpy matplotlib seaborn scikit-learn
jupyter notebook heart_disease_prediction.ipynb
```
