# Home Credit Default Risk Analytics

## Project Overview

This project analyzes customer loan application data from the Home Credit Default Risk dataset to identify borrowers with a high probability of default. The objective is to support data-driven lending decisions through exploratory analysis, feature engineering, predictive modeling, risk segmentation, and dashboard-ready analytics.

## Business Problem

Financial institutions face significant losses due to loan defaults. Accurately identifying high-risk applicants can help:

* Reduce credit losses
* Improve loan approval decisions
* Optimize risk management strategies
* Enhance portfolio performance

This project develops a credit risk analytics pipeline that predicts customer default risk and segments customers into actionable risk categories.

---

## Dataset

**Source:** Home Credit Default Risk Dataset

### Data Summary

* 307,511 customer records
* 210 features after preprocessing
* No missing values
* No duplicate records

---

## Project Workflow

### 1. Exploratory Data Analysis (EDA)

* Analyzed customer demographics and financial characteristics
* Investigated class imbalance in default behavior
* Examined distributions of income, credit amount, annuity, and age
* Identified patterns associated with loan defaults

### 2. Feature Engineering

Created business-focused features including:

* AGE
* AGE_GROUP
* YEARS_EMPLOYED
* EMPLOYMENT_TO_AGE_RATIO
* CREDIT_INCOME_RATIO
* ANNUITY_INCOME_RATIO
* CREDIT_ANNUITY_RATIO
* INCOME_PER_FAMILY_MEMBER
* INCOME_PER_CHILD
* CHILDREN_RATIO
* EXT_SOURCE_MEAN
* EXT_SOURCE_STD
* EXT_SOURCE_MIN
* YEARS_REGISTRATION
* YEARS_ID_PUBLISH
* GOODS_CREDIT_RATIO
* CONTACT_COUNT
* OWNS_CAR
* OWNS_REALTY

### 3. Model Development

Evaluated multiple classification models:

#### Dummy Classifier

* Accuracy: 0.9193
* ROC-AUC: 0.5000

#### Logistic Regression

* Accuracy: 0.6885
* Precision: 0.1614
* Recall: 0.6814
* F1 Score: 0.2610
* ROC-AUC: 0.7503

#### Random Forest

* Accuracy: 0.9194
* Precision: 0.5849
* Recall: 0.0062
* F1 Score: 0.0124
* ROC-AUC: 0.7324

#### XGBoost (Selected Model)

* Accuracy: 0.7199
* Precision: 0.1765
* Recall: 0.6737
* F1 Score: 0.2797
* ROC-AUC: 0.7667

---

## Model Evaluation

Performance comparison included:

* Confusion Matrix
* ROC Curve Analysis
* Precision-Recall Curve Analysis
* Average Precision Comparison
* Feature Importance Analysis

### Average Precision Scores

| Model               | AP Score |
| ------------------- | -------- |
| Logistic Regression | 0.231    |
| Random Forest       | 0.216    |
| XGBoost             | 0.256    |

---

## Risk Segmentation

Customers were segmented into:

* Low Risk
* Medium Risk
* High Risk

This segmentation enables business teams to prioritize loan reviews and improve credit decision-making.

---

## Dashboard Dataset

A dashboard-ready dataset containing 61,503 customer records was created for visualization and reporting.

Included fields:

* Default Probability
* Risk Segment
* Age
* Income
* Credit Amount
* Annuity
* Employment Information
* Financial Ratios
* Customer Attributes

---

## Repository Structure

```text
home-credit-default-risk-analytics/
│
├── data/
│   └── credit_risk_dashboard_data.csv
│
├── notebooks/
│   ├── 01_EDA.ipynb
│   ├── 02_Feature_Engineering.ipynb
│   └── 03_Model_Building.ipynb
│
├── README.md
├── requirements.txt
└── .gitignore
```

## Tools & Technologies

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-Learn
* XGBoost
* Jupyter Notebook
* Power BI

---

## Key Business Insights

* Customers with higher credit-to-income ratios exhibited increased default risk.
* External credit score features were among the strongest predictors of repayment behavior.
* Risk segmentation effectively differentiated low-risk and high-risk borrowers.
* Predictive analytics can assist lenders in improving loan approval strategies and reducing financial risk.

---

## Future Enhancements

* Interactive Power BI dashboard
* Automated reporting pipeline
* Advanced customer segmentation
* Real-time risk monitoring
