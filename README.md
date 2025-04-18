# Loan Prediction Project

---

## 🔥 Project Overview

In this project, we worked with a **Loan Prediction** dataset to predict whether a loan application will be **approved** or **not approved**.

The pipeline includes:
- Exploratory Data Analysis (EDA)
- Data Cleaning (missing value handling, feature encoding)
- Feature Engineering
- Building Machine Learning Models:
  - Support Vector Machine (Linear and RBF)
  - Decision Tree
  - Random Forest
  - K-Nearest Neighbors (KNN)
- Model Evaluation using Accuracy, Confusion Matrix, and Classification Reports.

---

## 📊 Exploratory Data Analysis (EDA) Insights

| Chart | Insight |
|:---|:---|
| **Correlation Matrix (Numerical Features)** | ApplicantIncome and LoanAmount have a moderate correlation (0.57). Loan Status is positively correlated with Credit History (0.54), indicating a good credit history improves loan approval chances. |
| **Correlation Matrix (Categorical Features)** | No very strong relationships among categorical features; minor relations between Dependents, Married status, and Loan Status. |

---

## 🛠️ Data Preprocessing

- **Loan_ID** was dropped as it is not useful for prediction.
- **Loan_Status** was label encoded ('Y' → 1, 'N' → 0).
- Missing values in both numerical and categorical features were handled:
  - Numerical columns → filled with **median**.
  - Categorical columns → filled with **most frequent (mode)**.
- **One-hot encoding** was applied to categorical features.
- **Feature scaling** was performed using `StandardScaler`.

---

## ⚙️ Machine Learning Models and Results

| Model | Accuracy | Key Observations |
|:---|:---|:---|
| **SVM (Linear Kernel)** | **77.27%** | Performs decently, with good recall on approved loans. |
| **SVM (RBF Kernel)** | **78.57%** | Slightly better performance than linear kernel. |
| **Decision Tree** | **66.23%** | Overfits a bit; lower performance. |
| **Random Forest** | **75.97%** | Stable and good performance with simple tuning (n_estimators=10). |
| **K-Nearest Neighbors (KNN)** | **76.62%** | Performs similarly to SVM models, but with slight trade-off in precision and recall. |

👉 **SVM (RBF Kernel)** performed best in this case.

---

## 📋 Final Test Set Prediction

- Final model (SVM RBF) was used to generate predictions on the test dataset after applying the same cleaning, encoding, and scaling steps.

---

## 📦 Project Folder Structure

```
Loan_Prediction_Project/
|
├── train_loan_prediction.csv     # Training dataset
├── test_loan_prediction.csv      # Testing dataset
├── Loan_Predictions.ipynb   # Final Clean Jupyter Notebook
└── README.md                     # Project Summary (this file)
```

---

## 📚 Conclusion

- **Credit History** is the most influential feature in predicting loan approvals.
- **Income** and **Loan Amount** have less direct influence than expected.
- **SVM models** were able to predict loan status with around **78% accuracy**.
- Careful **data preprocessing**, especially missing value treatment and feature engineering, greatly impacts the model performance.

🔁 This project demonstrates the full machine learning pipeline: **EDA → Cleaning → Modeling → Evaluation → Final Predictions**.

---

# 👋 Thank you for visiting the project!
