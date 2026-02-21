# Telecom Customer Churn Prediction

## 📌 Project Overview

This project aims to predict **customer churn** (customers who stop using the service) in the telecommunications industry using **machine learning techniques**. The notebook provides an end-to-end pipeline including data exploration, preprocessing, feature engineering, visualization, class balancing, model training, and evaluation.

The dataset used in this project is the **Telecom Churn Dataset (`Churn.csv`)**.

---

## 🧰 Technologies & Libraries

The following libraries are used in this project:

* pandas
* numpy
* matplotlib
* seaborn
* scikit-learn
* imbalanced-learn (SMOTE)
* warnings

Make sure all dependencies are installed before running the notebook.

---

## 🔍 Project Workflow

### 1️⃣ Import Libraries

All required libraries for data processing, visualization, and modeling are imported.

---

### 2️⃣ Data Loading & Understanding

* Load the `Churn.csv` dataset
* Inspect dataset shape, columns, and data types
* Identify missing values and inconsistencies

---

### 3️⃣ Data Type Conversion

Some numerical features are stored as strings and are converted into numeric format to enable proper analysis and modeling.

---

### 4️⃣ Feature Engineering

A new feature is created to capture customer behavior:

* **ChargesRatio** = MonthlyCharges / Tenure

This feature helps improve model interpretability and performance.

---

### 5️⃣ Categorical Encoding

Categorical features are transformed into numerical representations using:

* Label Encoding
* One-Hot Encoding

---

### 6️⃣ Exploratory Data Analysis & Visualization

Visual analysis is conducted to understand the relationship between features and churn.

#### a. Target Variable Analysis

* Distribution of churn vs non-churn customers

#### b. Categorical Features vs Churn

Categorical variables are grouped and analyzed, such as:

* Demographic features (gender, SeniorCitizen, Partner, Dependents)
* Service-related features (InternetService, StreamingTV, StreamingMovies, etc.)
* Contract and payment-related features

#### c. Numerical Features

* Tenure
* MonthlyCharges
* TotalCharges

#### d. Numerical vs Categorical Analysis

Visualization of numerical features across categorical groups (e.g., Tenure vs Contract, ChargesRatio vs PaymentMethod).

---

### 7️⃣ Feature Scaling

Numerical features are standardized using **StandardScaler** to ensure balanced feature distributions.

---

### 8️⃣ Feature Selection

#### a. Numerical Feature Selection

Statistical analysis and correlation-based selection are applied.

#### b. Categorical Feature Selection

Only the most relevant categorical features are retained for modeling.

---

### 9️⃣ Handling Class Imbalance

The dataset is imbalanced, so **SMOTE (Synthetic Minority Over-sampling Technique)** is applied to balance the churn and non-churn classes.

---

### 🔟 Modeling & Ensemble Learning

Multiple machine learning models are trained and compared, including:

* Logistic Regression
* Random Forest
* Gradient Boosting
* XGBoost (if available)

#### 🔗 Stacking Ensemble

Several stacking ensemble configurations are implemented to improve predictive performance:

* Stacking with 2 base models
* Stacking with 2 base models + Random Forest
* Stacking with 3 base models
* Stacking with 3 base models + Random Forest
* Stacking with 4 base models
* Stacking with 4 base models + Random Forest
* Stacking with 5 base models

---

## 📊 Model Evaluation

Models are evaluated using the following metrics:

* Accuracy
* Precision
* Recall
* F1-score

Evaluation results are used to identify the best-performing model.

---

## ▶️ How to Run the Project

1. Ensure Python version ≥ 3.8
2. Install dependencies:

   ```bash
   pip install pandas numpy matplotlib seaborn scikit-learn imbalanced-learn
   ```
3. Place `Churn.csv` in the same directory as the notebook
4. Run the notebook:

   ```bash
   jupyter notebook TelecomChurnPrediction.ipynb
   ```

---

## 🎯 Conclusion

This project demonstrates a complete **end-to-end machine learning workflow** for customer churn prediction, combining feature engineering, data balancing, and ensemble modeling techniques to achieve robust predictive performance. The approach can be extended to other customer retention and business analytics use cases.

---

## 👩‍💻 Author

Nikita Amelia Valencia  
Machine Learning & Data Science Enthusiast

---

## 📜 License

This project is for educational and portfolio purposes.
