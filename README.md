# Prediction of Cross-Selling Opportunities in Health Insurance

## Description
This project explores the cross-selling potential of vehicle insurance to health insurance customers using machine learning to predict customer interest.

## Summary
This project aims to leverage machine learning to predict whether health insurance policyholders from the past year will also be interested in purchasing vehicle insurance. By addressing the current inefficiencies in customer outreach, the developed model will enable the insurance company to optimize its communication strategy, business model, and revenue. Key business questions addressed include the influence of vehicle age on insurance response, strategies to attract different generations, factors affecting disinterest in vehicle insurance, and identifying the best machine learning model for cross-selling vehicle insurance.

## Feature Engineering & Selection For Machine Learning Process
Encoding all the categorical features
Checking correlation between dependent and independent variable
Feature Selection

## Model Building
Splitting data into Training and Testing
Apllying the SMOTE (Synthetic Minority Oversampling Technique) to the minority target since the data is imbalance
Creating base model of classification algorithm ( Logistic Regression, Random Forest Clasifier)
Check The Evaluation matrix for all the base model
HyperParameter tuning
Checking Evaluation Matrix for tuned Model
Choose which model has the best recall score for this case

## Conclusion
Starting from loading our dataset, we initially checked for null values and duplicates. Since there were none, no treatment was necessary.

Through Exploratory Data Analysis (EDA), we observed the following:
- Customers in the younger age group are more interested in vehicle insurance.
- Young people below 30 are not interested in vehicle insurance.
- Customers with vehicles older than 2 years are more likely to be interested in vehicle insurance.
- Customers with damaged vehicles are more likely to be interested in vehicle insurance.

Key variables affecting the target variable include Age, Previously_Insured, and Annual_Premium. For feature selection, we applied the Mutual Information technique and found that Previously_Insured is the most important feature with the highest impact on the target variable, with no correlation between them.

We observed that the target variable was highly imbalanced. To address this, we used the Random Over Sample resampling technique. We also applied feature scaling techniques to normalize our data, ensuring all features were on the same scale, making it easier to process by machine learning algorithms.

We then applied various Machine Learning algorithms to predict customer interest in vehicle insurance. The results are as follows:

- **Logistic Regression:** 
  - Accuracy = 78.56%
  - Recall = 97.61%
  - Precision = 70.72%
  - F1 Score = 82.02%
  - ROC_AUC = 83.42%
  
- **Random Forest:** 
  - Accuracy = 91.48%
  - Recall = 98.50%
  - Precision = 86.39%
  - F1 Score = 92.05%
  - ROC_AUC = 92.32%
  
- **XGBClassifier:** 
  - Accuracy = 80.72%
  - Recall = 93.65%
  - Precision = 74.44%
  - F1 Score = 82.95%
  - ROC_AUC = 82.92%

From these results, we can conclude that the Random Forest model performs the best, with the highest accuracy of approximately 91% and an ROC_AUC score of 92%. Therefore, Random Forest is the most effective model compared to the others.

