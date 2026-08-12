# Customer Churn Prediction

**Author:** Pentakota Manideep Jagannath

## Overview

This project develops an end-to-end machine learning workflow for customer churn-risk classification using customer demographic and engagement data.

The project covers data analysis, exploratory data analysis, feature engineering, preprocessing, machine learning model development, hyperparameter tuning, model evaluation, and business interpretation.

## Dataset

The dataset contains 243,553 customer records with demographic, telecom partner, location, registration, and customer engagement information.

Key engagement features include:

- Calls made
- SMS sent
- Data used
- Estimated salary
- Age
- Number of dependents

## Project Workflow

1. Data loading and understanding
2. Data quality analysis
3. Exploratory Data Analysis
4. Feature engineering
5. Categorical encoding
6. Train-test split
7. Feature scaling
8. Logistic Regression
9. Random Forest
10. Random Forest hyperparameter tuning using GridSearchCV
11. XGBoost
12. Model comparison
13. Final model selection
14. Business interpretation

## Models Evaluated

- Logistic Regression
- Random Forest
- Tuned Random Forest
- XGBoost

## Model Performance

| Model | Accuracy | Precision | Recall | F1 Score | ROC-AUC |
|---|---:|---:|---:|---:|---:|
| Logistic Regression | 93.57% | 85.63% | 81.53% | 83.53% | 97.98% |
| Random Forest | 92.55% | 91.64% | 69.05% | 78.76% | 97.44% |
| Tuned Random Forest | 93.16% | 89.18% | 74.89% | 81.41% | 97.66% |
| XGBoost | 93.52% | 85.37% | 81.58% | 83.43% | 97.93% |

Logistic Regression was selected as the final model based on its overall balance of accuracy, recall, F1-score, and ROC-AUC.

## Hyperparameter Tuning

GridSearchCV was used to optimize the Random Forest model.

Best parameters:

- `n_estimators`: 200
- `max_depth`: 20
- `min_samples_split`: 5

The tuned Random Forest improved its F1-score from 78.76% to 81.41%.

## Business Application

A churn-risk model can help telecom businesses identify customers who may be more likely to leave and prioritize them for retention strategies such as targeted offers, proactive support, and personalized communication.

## Limitations

The original churn label showed very weak relationships with the available customer features. Therefore, a behavioral churn target was constructed using customer engagement indicators for this modeling exercise.

As a result, the reported performance should be considered a demonstration of the machine learning workflow rather than production-level performance on independently observed real-world churn outcomes.

A real-world implementation would benefit from historical churn outcomes and additional features such as customer tenure, contract type, billing history, complaints, and service interactions.

## Technologies

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- XGBoost
- Jupyter Notebook
- SQL
- MySQL
