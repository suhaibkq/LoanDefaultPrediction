# 🏦 Loan Delinquency Prediction — AI/ML Case Study

## 📌 Problem Statement

**DRS Bank** is facing rising levels of Non-Performing Assets (NPAs), largely due to loan delinquencies by individual borrowers. To address this, the Chief Risk Officer initiated a data science-driven project aimed at identifying key patterns and risk indicators from historical data.

## 🎯 Objective

Develop a machine learning model that:
- Predicts whether a borrower is likely to default (become delinquent)
- Identifies key features driving loan delinquency
- Helps refine the loan approval process with data-backed decisions

## 📊 Dataset

- **File**: `Loan_Delinquent_Dataset.csv`
- **Target Variable**: `loan_condition_cat`
  - Values: `'Delinquent'` vs `'Non-Delinquent'`

- **Features Include**:
  - `loan_limit`, `loan_status`, `gender`, `approv_in_adv`, `loan_type`, `property_type`
  - `loan_purpose`, `occupancy`, `loan_amount`, `interest_rate`, `credit_score`
  - `debt_to_income_ratio`, `borrower_income`, `property_value`, `loan_to_value`, etc.

## 📁 Repository Structure

```
├── W2_Additional_CaseStudy_Loan_Delinquent_AIML.ipynb   # Main notebook
├── Loan_Delinquent_Dataset.csv                          # Dataset file
├── README.md                                            # Project documentation
```

## 🧪 Project Workflow

1. **Data Preprocessing**
   - Handled categorical variables using label and one-hot encoding
   - Removed features with low variance or high nulls
   - Imputed missing values and created derived metrics like `loan_to_income`

2. **Exploratory Data Analysis**
   - Correlation heatmaps and visualizations
   - Identified strong predictors like `credit_score`, `interest_rate`, `loan_to_value`

3. **Model Building**
   - Models Trained:
     - Logistic Regression
     - Decision Tree Classifier
     - Random Forest Classifier
   - Used GridSearchCV for hyperparameter tuning

4. **Evaluation Metrics**
   - Accuracy, Precision, Recall, F1 Score
   - Confusion Matrix and ROC-AUC Curve

## 🏆 Results

- **Best Model**: Random Forest Classifier
- **Accuracy**: ~90%+
- **Key Predictors**:
  - High interest rates and low credit scores strongly correlate with delinquency
  - Loan-to-value ratio and debt-to-income are key risk indicators

## 🔍 Insights

- Customers with high debt-to-income and low credit scores are most likely to default
- Borrower’s income and interest rates are major factors in loan risk assessment
- Early-stage approval indicators (e.g., `approv_in_adv`) also contribute to risk

## 🚀 Future Enhancements

- Deploy the model in a Flask API for integration with loan processing systems
- Introduce time-series features (e.g., payment history trends)
- Evaluate using ensemble models like XGBoost for potential gains

## 👨‍💻 Author

**Suhaib Khalid**  
AI/ML Practitioner 
