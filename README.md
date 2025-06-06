# Predicting-Fraud-in-Financial-Payment-Services
In digital age we know that financial fraud is a great threat for individuals as well as institutions. To combat this challenge we need datasets but this type of datasets are rare to find. The one we are using here is one of only four datasets present on kaggle i.e. PaySim (simulated mobile money transaction data). This data gives us an opportunity to find an effective method for the financial fraud detection. But there are some challenges, the data is highly imbalanced. So, the main goal here is to resolve the issues by detailed data exploration and to develop a practical solution for identifying fraud, and make digital finance more secured and safe.

# Data Cleaning & EDA
- Fraud is only present in 'TRANSFER' and 'CASH_OUT' transactions.
- Columns like 'nameOrig', 'nameDest', and 'isFlaggedFraud' were removed due to redundancy or
irrelevance.

# Feature Engineering
Created new features:
- errorBalanceOrig = oldbalanceOrg - amount - newbalanceOrig
- errorBalanceDest = oldbalanceDest + amount - newbalanceDest
These features helped in distinguishing fraud effectively.

# Model Used and Evaluation Metric
Model Used- XGBoost Classifier was chosen for its robustness, ability to handle missing values, and class imbalance.
Evaluation Metric- Used AUPRC (Area Under Precision-Recall Curve) due to high class imbalance in data.

# Result
Achieved AUPRC = 0.991. Model performed excellently in detecting fraud.
