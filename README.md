# Customer Churn Prediction
A machine learning project that predicts whether a telecom customer will churn, developed as part of the Machine Learning course at Umm Al-Qura University.

## Dataset

[Telco Customer Churn](https://www.kaggle.com/datasets/blastchar/telco-customer-churn) (Kaggle): 7,043 customers and 21 columns. Approximately 27% of customers churned.

## Approach

- **Data Cleaning:** Removed `customerID`, converted `TotalCharges` to numeric, and imputed 11 missing values using the median.
- **Preprocessing:** Applied one-hot encoding and feature scaling (for Logistic Regression).
- **Models:** Compared Logistic Regression and Random Forest using balanced class weights.
- **Evaluation:** Used accuracy, precision, recall, F1-score, ROC-AUC, and confusion matrices.
- **Threshold Tuning:** Adjusted the decision threshold to improve churn detection.

## Results

| Model | Accuracy | Precision | Recall | F1 | ROC-AUC |
|---|---|---|---|---|---|
| Logistic Regression | 81.97% | 0.68 | 0.60 | 0.64 | 0.862 |
| Random Forest (0.5) | 79.56% | 0.60 | 0.71 | 0.65 | 0.859 |
| **Random Forest (0.4) – Final** | **76.58%** | **0.54** | **0.84** | **0.66** | **0.859** |

The final model detects 84% of churning customers. Key churn drivers include tenure, TotalCharges, MonthlyCharges, and contract type.

## Limitations & Future Work

The results are based on a single 80/20 train-test split. Future improvements could include stratified cross-validation, hyperparameter tuning, and gradient boosting.

## Tools & Technologies

- Python
- Pandas & NumPy
- Scikit-learn
- Matplotlib & Seaborn
- Jupyter Notebook

## Documentation
- [Project Report](docs/Churn_Prediction_Report.pdf)
- [Presentation](docs/Churn_Prediction_Presentation.pdf)
  
