# Data_Mining_7_Project_Census

This repository contains the final project submission for a supervised learning classification task using R. The objective was to explore and evaluate multiple classification models learned during the course. The workflow includes Exploratory Data Analysis (EDA), data preprocessing, and training six classification models to identify the best-performing algorithm based on accuracy and interpretability.

---

### 🧩 Business Problem

This project uses the UCI Adult Income Dataset, which includes demographic and employment-related data on over 32,000 individuals. The aim is to predict whether a person earns more than $50K per year — a binary classification task with a categorical target variable (y).

Several models from the original list (e.g., LinearRegression, M5P, SimpleKMeans(), and Apriori()) were excluded because they are not designed for classification tasks with categorical targets. The final focus was placed on models that are suitable for classification.

---

### 📦 Dataset Overview

The dataset contains **32,561 observations** and **15 variables**. The target variable is `y`, which represents income class:

- `y`: **<=50K** or **>50K**

Key features include:

- **Demographics**: `age`, `sex`, `race`, `native.country`, `education`, `marital.status`
- **Employment**: `workclass`, `occupation`, `hours.per.week`, `capital.gain`, `capital.loss`
- **Others**: `education.num`, `fnlwgt`, `relationship`

This dataset presents common real-world challenges, including missing values, categorical encoding, and class imbalance.

---

### 🎯 Project Objective

This project was designed to:

- Conduct EDA to understand distributions, correlations, and class imbalance.
- Preprocess the data for modeling (scaling, encoding, imputing missing values).
- Apply and compare **six supervised classification models**:
  1. **C5.0 Decision Tree**
  2. **Naïve Bayes**
  3. **Rpart Decision Tree**
  4. **Neural Networks (`make_Weka_classifier`)**
  5. **Support Vector Machine (`ksvm`)**
  6. **K-Nearest Neighbors (KNN - `IBk`)**
- Evaluate performance using **accuracy**, **confusion matrices**, and cross-validation.
- Identify the most suitable model based on results and interpretability.

---

### 🛠️ Solution Approach

The end-to-end machine learning workflow included:

- **EDA**:
  - Analyzed class imbalance and variable importance.
  - Explored correlations between demographic and income features.
- **Data Preprocessing**:
  - Encoded categorical variables and imputed missing values.
  - Scaled numeric variables where necessary (especially for KNN and SVM).
- **Model Development**:
  - Trained all six classifiers using their respective R packages (`RWeka`, `e1071`, `nnet`, `kernlab`, etc.).
  - Tuned hyperparameters and used k-fold cross-validation for evaluation.
- **Model Evaluation**:
  - Compared performance using confusion matrices and accuracy scores.
  - Selected the best-performing model based on generalization ability and interpretability.

---

### 💡 Business Value

This project reflects a typical real-world scenario in HR analytics or government income modeling:

- **Predictive Capability**: Enables institutions to identify at-risk or high-income individuals based on demographics.
- **Model Comparison**: Helps in selecting appropriate classifiers based on business needs (accuracy vs. explainability).
- **Reusability**: The framework can be applied to any binary classification problem involving categorical and numeric data.

---

### 🚧 Challenges Encountered

- **Encoding and Scaling**: Different models required specific preprocessing (e.g., scaling for SVM and KNN).
- **Model Complexity**: Neural networks and SVMs required careful tuning to avoid overfitting.
- **Class Imbalance**: The dataset had more individuals earning <=50K, impacting some metrics like recall.

---
