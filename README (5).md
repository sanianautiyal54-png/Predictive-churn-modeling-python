# Predictive Churn Modeling with Python

## Project Overview

This project focuses on predicting customer churn using Python and a basic machine learning classification model.

The **Telco Customer Churn** dataset is used to understand customer behavior, build a churn prediction model, evaluate its performance, and identify the main factors associated with customer churn.

## Objectives

- Clean and prepare the customer churn data
- Explore the distribution of churn
- Build a Logistic Regression classification model
- Split the data into training and testing sets
- Evaluate the model using Accuracy, Precision, and Recall
- Handle class imbalance using a balanced Logistic Regression model
- Create a confusion matrix
- Identify the top 5 churn drivers
- Explain the findings in simple business terms

## Dataset

The project uses the Telco Customer Churn dataset.

The dataset contains customer information such as:

- Customer tenure
- Contract type
- Internet services
- Online security
- Technical support
- Payment method
- Monthly charges
- Total charges
- Churn status

## Tools and Technologies

- Python
- Pandas
- Scikit-learn
- Matplotlib
- Seaborn
- Google Colab

## Project Workflow

### 1. Data Loading and Cleaning

The dataset was loaded using Pandas. Missing values and data types were checked and cleaned before building the model.

### 2. Data Preparation

The target variable is **Churn**.

Categorical variables were converted into numerical dummy variables so they could be used by the Logistic Regression model.

The `customerID` column was removed because it is an identifier and does not provide useful predictive information.

### 3. Train-Test Split

The data was divided into training and testing sets.

- 80% Training Data
- 20% Testing Data

Stratified splitting was used to maintain the churn/non-churn proportion in both sets.

### 4. Logistic Regression

A Logistic Regression model was used as the classification algorithm.

A second Logistic Regression model was trained with `class_weight="balanced"` to address the class imbalance in the dataset.

### 5. Model Evaluation

The models were evaluated using:

- Accuracy
- Precision
- Recall
- Confusion Matrix

The balanced model was also compared with the original model to understand the effect of handling class imbalance.

## Top 5 Churn Drivers

The balanced Logistic Regression model identified the following features among the top 5 drivers based on the absolute value of their model coefficients:

1. **Two-Year Contract** – associated with lower churn.
2. **One-Year Contract** – associated with lower churn.
3. **No Phone Service** – associated with higher churn.
4. **Online Security** – associated with lower churn.
5. **Technical Support** – associated with lower churn.

These are model associations, not proof that these factors directly cause churn.

## Business Recommendations

Based on the analysis, the business can consider:

- Encouraging customers to choose longer-term contracts.
- Promoting Online Security and Technical Support services.
- Investigating customers without phone service to understand their higher churn association.
- Using the churn model to identify customers who may be at higher risk and taking retention actions early.
- Monitoring churn patterns regularly.

## Project Files

```text
Predictive-Churn-Modeling/
│
├── Predictive_Churn_Modeling.ipynb
├── Business_Recommendations_Customer_Churn.docx
└── README.md
```

## Conclusion

This project demonstrates how Python and a basic classification model can be used to analyze customer churn and identify factors associated with customer retention.

The project also shows the importance of checking class imbalance and using appropriate evaluation metrics such as precision and recall instead of relying only on accuracy.
