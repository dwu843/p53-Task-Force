# Predicting p53 Transcriptional Activity

This project examines mutations in the tumor suppressor gene **p53** using a dataset of transcriptional activity measurements paired with biophysical feature descriptors. Through statistical analysis and machine learning modeling, we evaluate how molecular-dynamics–derived features relate to transcriptional outcomes and assess the ability of predictive models to distinguish active from inactive p53 variants.

Our analysis aims to identify meaningful correlations, characterize structural patterns in high-dimensional feature space, and compare the performance of several supervised learning approaches for predicting variant activity.

---

## Data Availability

All required data is included in **data.zip**

After extracting, ensure the following files are in the same directory as the notebook:

- **K9.data** — high-dimensional biophysical feature matrix  
- **K9.def** — transcriptional activity labels (“active” or “inactive”)  
- **K9.instance.tags** — variant identifiers mapped to feature rows  

A preprocessing pipeline merges, cleans, and aligns these data sources automatically.

---

## Project Objectives

- Analyze statistical relationships between molecular-dynamics biophysical features and p53 transcriptional activity.  
- Build supervised machine learning models to classify p53 variants as active or inactive.  
- Apply PCA to uncover structure in high-dimensional features.  
- Compare model performance across logistic regression, SVM, and random forest classifiers.

---

## Key Components

### 1. Data Exploration and Cleaning
- Merging feature, label, and identifier files  
- Removing fully missing rows/columns  
- Median imputation for remaining missing values  
- Inspecting class imbalance and feature distributions  

### 2. Machine Learning Models
- **Logistic Regression** (L2 regularization)  
- **Support Vector Machine** (RBF kernel + PCA)  
- **Random Forest** (PCA-based)  

Models are evaluated on held-out test data.

### 3. Evaluation Metrics
- AUROC  
- AUPRC  
- F1-score  
- Balanced accuracy  
- ROC and Precision–Recall curves  

### 4. Visualizations
- PCA scatterplots of test samples  
- ROC and PR curves comparing model performance  

---

## Tools and Libraries

- **Python** — primary analysis language  
- **numpy**, **pandas** — data handling  
- **scikit-learn** — preprocessing, PCA, modeling, evaluation  
- **matplotlib** — visualizations  

---
