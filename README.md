#  Credit Card Fraud Detection using Mahalanobis-SMOTE 

## Overview

Financial fraud detection is a high-impact risk modeling problem where class imbalance severely affects model performance. This project presents an advanced fraud detection pipeline designed to accurately identify fraudulent credit card transactions while minimizing false negatives — a critical factor in financial risk mitigation.

The system integrates:

- Custom Mahalanobis-distance based SMOTE  
- ENN (Edited Nearest Neighbors) cleaning  
- Multiple supervised learning models  
- Robust evaluation metrics aligned with financial risk priorities  
- ROC-based performance comparison  

This project simulates a real-world fraud analytics system suitable for banking and financial institutions.

---

##  Problem Statement

Credit card fraud datasets are highly imbalanced (fraud < 1%). Traditional classifiers tend to bias toward the majority class, leading to high accuracy but poor fraud detection.

### Goal:

- Improve recall for fraudulent transactions  
- Maintain strong precision to avoid excessive customer friction  
- Evaluate models using risk-aware metrics rather than accuracy alone  

---

##  Dataset

- European credit card transaction dataset  
- PCA-transformed features (V1–V28)  
- Time and Amount features normalized  
- Binary classification:  
  - `0` → Legitimate  
  - `1` → Fraud  

Class imbalance handled using a custom oversampling technique.

---

##  Methodology

### 1️ Data Preprocessing

- Standardized Amount and Time features  
- Removed original scale bias  
- Checked missing values and data integrity  

---

### 2️ Custom Mahalanobis-SMOTE

Instead of using vanilla SMOTE, this project introduces:

- ✔ Mahalanobis distance-based neighbor selection  
- ✔ Covariance-aware synthetic sample generation  
- ✔ Improved minority class boundary learning  

This approach generates more statistically coherent synthetic fraud samples.

---

### 3️ ENN Cleaning

After oversampling:

- Applied Edited Nearest Neighbors (ENN)  
- Removed noisy or ambiguous samples  
- Reduced overfitting risk  

---

### 4️ Models Implemented

- Logistic Regression  
- K-Nearest Neighbors  
- Random Forest  
- Naive Bayes  
- AdaBoost  
- XGBoost (Delta Addition Model)  

Each model was evaluated and compared under identical training conditions.

---

##  Evaluation Metrics

To align with financial risk modeling priorities, the following metrics were used:

- Accuracy  
- Precision  
- Recall (critical for fraud detection)  
- F1 Score  
- ROC-AUC  
- Matthews Correlation Coefficient (MCC)  
- Confusion Matrix  
- ROC Curve comparison  

Accuracy alone is not sufficient for imbalanced financial datasets — recall and AUC are prioritized to reduce missed fraud cases.

---

## Key Results

- Achieved ROC-AUC ≈ 0.999+  
- High Recall while maintaining strong Precision  
- XGBoost and Random Forest demonstrated superior fraud detection capability  
- Balanced class distribution significantly improved minority detection performance  

---

## Visualization

- Class distribution before & after resampling  
- Model comparison bar charts  
- ROC Curve comparison  
- Confusion matrices for each classifier  

---

##  Tech Stack

- Python  
- NumPy  
- Pandas  
- scikit-learn  
- XGBoost  
- Matplotlib  
- Seaborn  

---

## Team

**Artificial Intelligence Team Project Onsite at IIITV-ICD**
