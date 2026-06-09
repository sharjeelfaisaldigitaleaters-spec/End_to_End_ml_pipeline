# 📈 End-to-End ML Pipeline for Customer Churn Prediction

A complete machine learning pipeline built using **Scikit-Learn** to predict customer churn using the Telco Customer Churn dataset.

The project demonstrates production-ready ML workflow including:

* Data preprocessing
* Feature engineering
* Pipeline construction
* Hyperparameter tuning
* Model evaluation
* Model export and deployment preparation

---

## 🚀 Project Overview

Customer churn prediction helps businesses identify customers who are likely to discontinue a service.

This project builds reusable machine learning pipelines using:

* Logistic Regression
* Random Forest

and compares their performance using multiple evaluation metrics.

---

## 📊 Dataset

Dataset: IBM Telco Customer Churn

### Dataset Statistics

* Total Records: 7,043
* Features: 20
* Target Variable: Churn

### Churn Distribution

* No Churn: 5,174
* Churn: 1,869
* Churn Rate: 26.54%

---

## 🛠 Technologies Used

* Python
* Pandas
* NumPy
* Scikit-Learn
* Matplotlib
* Seaborn
* Joblib

---

## ⚙️ Data Preprocessing

### Steps Performed

* Removed customerID
* Converted TotalCharges to numeric format
* Filled missing values using median imputation
* Encoded target variable
* Train-Test Split (80/20)
* One-Hot Encoding for categorical features
* Standard Scaling for numerical features

---

## 🔄 Machine Learning Pipelines

### Logistic Regression Pipeline

```text
ColumnTransformer
    ├── StandardScaler
    └── OneHotEncoder

LogisticRegression
```

### Random Forest Pipeline

```text
ColumnTransformer
    ├── StandardScaler
    └── OneHotEncoder

RandomForestClassifier
```

---

## 🔍 Hyperparameter Tuning

### Logistic Regression

Best Parameters

```python
{
    "C": 1,
    "penalty": "l2",
    "solver": "lbfgs"
}
```

### Random Forest

Best Parameters

```python
{
    "n_estimators": 200,
    "max_depth": 10,
    "min_samples_split": 5
}
```

---

## 📈 Model Performance

| Model               | Accuracy | F1 Score | ROC-AUC |
| ------------------- | -------- | -------- | ------- |
| Logistic Regression | 80.55%   | 0.6040   | 0.8420  |
| Random Forest       | 80.06%   | 0.5800   | 0.8417  |

🏆 Best Model: Logistic Regression

---

## 📊 Visualizations

The project generates:

* Churn Distribution Analysis
* Contract Type vs Churn Analysis
* Confusion Matrices
* ROC Curves
* Feature Importance Plot

---

## 💾 Model Export

All trained pipelines are exported using Joblib.

```bash
lr_churn_pipeline.pkl
rf_churn_pipeline.pkl
best_churn_pipeline.pkl
```

The exported model can be directly loaded for inference.

---

## 📂 Project Structure

```text
├── notebook.ipynb
├── lr_churn_pipeline.pkl
├── rf_churn_pipeline.pkl
├── best_churn_pipeline.pkl
├── eda_plots.png
├── model_evaluation.png
├── feature_importance.png
├── requirements.txt
└── README.md
```

---

## 🎯 Key Learnings

* Building production-ready ML pipelines
* Feature preprocessing with ColumnTransformer
* Hyperparameter optimization using GridSearchCV
* ROC-AUC analysis
* Pipeline serialization using Joblib
* End-to-end machine learning workflow

---

## 👨‍💻 Author

Muhammad Sharjeel Faisal

AI/ML Engineering Internship Project
