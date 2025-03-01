# Risk-management-Loan-Defaulters-prediction-model-
This project builds a **loan default prediction model** using the **Prosper Loan Dataset**. We tested **Logistic Regression, Random Forest, and XGBoost**, selecting **XGBoost (threshold = 0.38)** for its **high recall (69.96%)** in detecting defaulters. This model helps improve **loan risk assessment** and **financial decision-making**. 
Model Summary Report: Loan Default Prediction

1. Project Objective

The primary goal of this project was to build a loan default prediction model using the Prosper Loan Dataset. The objective was to help financial institutions identify high-risk borrowers before issuing loans, minimizing financial losses and improving credit risk management.

2. Data Overview & Key Features

The dataset contained 113,937 loan records with 81 features. After thorough exploratory data analysis (EDA), missing values were handled, irrelevant columns were removed, and key predictive features were retained. These included:

Borrower APR & Interest Rate (loan pricing factors)

Loan Original Amount (amount borrowed)

Debt-to-Income Ratio (borrower’s financial health)

Prosper Score & Credit Ratings (historical risk assessment)

Employment Status & Income Range (borrower’s repayment ability)

CreditScoreRangeLower  (Credit Score Lower Range)

CreditScoreRangeUpper  (Credit Score Upper Range)

Term    (Loan Term (36 or 60 months))

CurrentDelinquencies  (Current Delinquencies)

DelinquenciesLast7Years (Delinquencies in the past 7 years)

LoanStatus (Target Variable (Will be converted to Default_Status))



3. Model Selection & Training

Several machine learning models were tested, including:
✔ Logistic Regression (Baseline Model) – Recall: 72.46%, Precision: 34.02%✔ Random Forest (Optimized) – Recall: 43.80%, Precision: 41.98%✔ XGBoost (Best Performing Model) – Recall: 56.50%, Precision: 40.69%

After tuning hyperparameters, XGBoost emerged as the best model for our objective.

4. Choosing the Best Threshold for Risk Management

Rather than using the default 0.5 probability threshold, we adjusted it to 0.38, prioritizing recall (catching more defaulters). The reasoning:

Threshold 0.38 → Recall: 69.96%, Precision: 36.76%

Threshold 0.40 → Recall: 67.31%, Precision: 37.10%

Threshold 0.42 → Recall: 64.96%, Precision: 37.75%

Final Decision: We chose Threshold = 0.38 to maximize recall, ensuring that most defaulters are detected, even at the cost of some false positives.

5. Final Model Performance (Threshold = 0.38)

✅ Accuracy: 77.55%✅ Precision: 36.76%✅ Recall: 69.96%✅ ROC-AUC Score: 82.61%

This means that nearly 70% of actual defaulters were correctly identified, making the model a strong tool for credit risk assessment.

6. Model Deployment & Next Steps

The final model has been saved as ‘final_default_prediction_model.pkl’ and can be deployed in production systems. Future improvements can include:
✔ Further fine-tuning with cost-sensitive learning to reduce false positives.✔ Incorporating more recent data to improve model generalization.✔ Exploring deep learning methods for enhanced risk modeling.

🔹 Conclusion: This model provides a solid foundation for predicting loan defaults, helping lenders make more informed, data-driven lending decisions. 🚀

