# Predicting Lung Disease Recovery

**Author:** Logan Hahn  
**Course:** COMP 4448 - Data Science Tools 2  
**Institution:** University of Denver

## Overview

This project explores the use of machine learning classification models to predict whether a patient diagnosed with a lung disease will recover. The analysis compares three different algorithms—Logistic Regression, Random Forest, and XGBoost—to determine which performs best in terms of predictive accuracy and overall classification metrics.

The goal is to assess the potential of using clinical and demographic data to support early intervention and resource allocation decisions in healthcare.

---

## Table of Contents

- [Project Objective](#project-objective)
- [Dataset](#dataset)
- [Approach](#approach)
- [Results Summary](#results-summary)
- [Project Structure](#project-structure)
- [Conclusions](#conclusions)

---

## Project Objective

To determine which classification model—Logistic Regression, Random Forest, or XGBoost—is most effective in predicting recovery outcomes of lung disease patients based on:

- Demographic features (e.g., age, gender)
- Lifestyle factors (e.g., smoking status)
- Clinical indicators (e.g., lung capacity, hospital visits)

---

## Dataset

- **Source:** [Kaggle - Lungs Diseases Dataset](https://www.kaggle.com/datasets/samikshadalvi/lungs-diseases-dataset)
- **Size:** 5,200 rows × 8 columns
- **Target Variable:** `Recovered` (binary: Yes / No)
- **Features:**
  - Age (Numerical)
  - Gender (Categorical)
  - Smoking Status (Categorical)
  - Lung Capacity (Numerical)
  - Disease Type (Categorical)
  - Treatment Type (Categorical)
  - Hospital Visits (Numerical)

---

## Approach

1. **Data Inspection and Cleaning**
   - Handled missing values via KNN imputation
   - Removed duplicates
   - Encoded categorical variables (OneHotEncoder)
   - Scaled numerical variables (StandardScaler)

2. **Exploratory Data Analysis (EDA)**
   - Visualized feature distributions
   - Examined relationships with target variable
   - Assessed correlations and potential multicollinearity

3. **Model Development**
   - Logistic Regression (Linear)
   - Random Forest (Ensemble Tree-Based)
   - XGBoost (Gradient Boosted Trees)

4. **Evaluation Metrics**
   - Accuracy
   - Precision, Recall, F1-Score
   - Cross-Validation

5. **Hyperparameter Tuning**
   - Used GridSearchCV to optimize each model

---

## Results Summary

| Model              | Accuracy | F1-Score | Recall |
|-------------------|----------|----------|--------|
| Logistic Regression | ~52%    | 55.8%    | 54.3%  |
| Random Forest      | ~54%    | 61.3%    | 65.4%  |
| XGBoost            | ~54%    | **65.8%**| **78.8%** |

- **Best Performing Model:** XGBoost
- **Most Balanced Recall & Precision:** XGBoost
- All models showed limited predictive power, suggesting dataset limitations.

---

## Conclusions

- **XGBoost** outperformed the other models based on F1-Score and Recall, particularly in identifying patients likely to recover.
- All models struggled to achieve strong predictive accuracy, pointing to limited feature quality or lack of clinical depth in the dataset.
- Future work should explore enriched datasets, additional clinical variables, or time-series features to improve predictability.
