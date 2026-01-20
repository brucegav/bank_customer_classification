# Bank Customer Churn Classification

This repository contains a machine learning project aimed at predicting customer churn for a retail bank. The project involves end-to-end data processing, feature engineering, and a comparative analysis between Logistic Regression and Random Forest models.

## Project Overview
The objective is to identify customers at high risk of leaving the bank. Given the business cost of churn, the models were optimized to prioritize **Recall** (identifying as many churners as possible) and **AUC-ROC** (overall separation power).

## Key Features
* **Exploratory Data Analysis (EDA):** Visualized demographic and financial drivers of churn.
* **Feature Engineering:** Developed custom ratios, including income_v_products and balance_to_income, to capture non-linear relationships.
* **Class Imbalance Handling:** Utilized class_weight='balanced' to address the 20% churn minority.
* **Hyperparameter Tuning:** Employed GridSearchCV with Cross-Validation to optimize the Random Forest ensemble.

## Results Summary
| Model | AUC Score | Key Takeaway |
| :--- | :--- | :--- |
| **Logistic Regression** | 0.79 | Strong baseline; prioritized high recall for churners. |
| **Random Forest** | **0.87** | Superior performance; significantly reduced false positives. |

### Major Findings
* **Top Predictors:** Age and Number of Products were the strongest indicators of churn.
* **Engineered Impact:** The custom income_v_products feature ranked as a top-4 predictor in the final model.

## Installation & Usage
1. Clone the repository:
   git clone https://github.com/brucegav/bank_customer_classification.git
2. Install dependencies:
   pip install -r requirements.txt
3. Run the notebook:
   jupyter notebook bank_customer_classification.ipynb
