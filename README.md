# Bank Customer Churn Prediction

## Overview

This project aims to predict whether a bank customer will leave the bank (churn) or continue as a customer, using machine learning classification techniques. The analysis is performed on a real-world bank dataset and follows a typical data science workflow, including data preprocessing, exploratory data analysis, feature engineering, model building, evaluation, and interpretation.

## Business Problem

Banks lose significant revenue when customers close their accounts. Early identification of customers likely to churn enables the bank to take proactive retention actions.  
**Goal:**  
Build a predictive model that classifies customers as "churned" or "retained" based on their demographic and transactional features.

## Dataset

The dataset contains 10,000 bank customers and the following features:

| Column           | Description                                                                 |
|------------------|-----------------------------------------------------------------------------|
| RowNumber        | Row number (1 to 10,000)                                                    |
| CustomerId       | Unique identifier for each customer                                         |
| Surname          | Customer's last name                                                        |
| CreditScore      | Customer's credit score                                                     |
| Geography        | Country of the customer                                                     |
| Gender           | Male or Female                                                              |
| Age              | Customer's age                                                              |
| Tenure           | Number of years the customer has been with the bank                         |
| Balance          | Customer's bank balance                                                     |
| NumOfProducts    | Number of bank products the customer uses                                   |
| HasCrCard        | 1 if the customer has a credit card, 0 otherwise                            |
| IsActiveMember   | 1 if the customer is an active member, 0 otherwise                          |
| EstimatedSalary  | Estimated salary of the customer (in Dollars)                               |
| Exited           | 1 if the customer closed their account (churned), 0 if retained (target)    |

## Project Pipeline

### 1. Data Loading & Initial Exploration

- Load the dataset and inspect its structure.
- Check for missing values, data types, and basic statistics.

### 2. Exploratory Data Analysis (EDA)

- Analyze the distribution of the target variable (`Exited`).
- Visualize feature distributions and relationships (e.g., churn rate by country, age, balance).
- Identify potential outliers and data quality issues.

### 3. Data Preprocessing

- Handle missing or anomalous values if any.
- Encode categorical variables (`Geography`, `Gender`) using label encoding or one-hot encoding.
- Scale numerical features (e.g., `CreditScore`, `Age`, `Balance`, `EstimatedSalary`) for model compatibility.
- Split the data into training and test sets.

### 4. Feature Engineering

- Create new features if beneficial (e.g., balance-to-salary ratio, age groups).
- Analyze feature importance and remove irrelevant or redundant features.

### 5. Model Building

- Train multiple classification models (e.g., Logistic Regression, Random Forest, XGBoost, LightGBM).
- Use cross-validation and hyperparameter tuning (e.g., GridSearchCV) to optimize model performance.
- Evaluate models using appropriate metrics.

### 6. Model Evaluation

- Use metrics such as Accuracy, Precision, Recall, F1-Score, ROC-AUC.
- Analyze the confusion matrix and classification report.
- Compare model performances and select the best one.

### 7. Interpretation & Insights

- Interpret feature importances and model decisions.
- Provide actionable business insights (e.g., which customer segments are at higher risk of churn).

### 8. Prediction

- Use the final model to predict churn on new or unseen customer data.

## How to Run

1. **Clone the repository:**
    ```bash
    git clone https://github.com/yourusername/bank-churn-prediction.git
    cd bank-churn-prediction
    ```

2. **Install dependencies:**
    - Python 3.8+
    - pandas, numpy, matplotlib, seaborn, scikit-learn, xgboost, lightgbm (if used), jupyter

    ```bash
    pip install -r requirements.txt
    ```

3. **Run the notebook:**
    - Open `02_classification_churn_10K.ipynb` in Jupyter Notebook or JupyterLab.
    - Follow the cells sequentially to reproduce the analysis and results.

## Results

- The best performing model achieved an ROC-AUC of **X.XX** and an accuracy of **XX%** on the test set.
- Key drivers of churn include: `Geography`, `Age`, `Balance`, `IsActiveMember`, and `NumOfProducts`.
- Customers from certain countries, older age groups, and those with higher balances but low activity are more likely to churn.

## Project Structure
├── 02_classification_churn_10K.ipynb # Main analysis notebook
├── data/ # (Optional) Data files
├── requirements.txt # Python dependencies
└── README.md # Project documentation


## Contributing

1. Fork the repository.
2. Create a new branch (`git checkout -b feature/your-feature`).
3. Commit your changes (`git commit -am 'Add new feature'`).
4. Push to the branch (`git push origin feature/your-feature`).
5. Open a Pull Request.

## License

This project is licensed under the MIT License.

---

**Note:** This project is for educational and demonstration purposes. For production use, further validation, monitoring, and data privacy considerations are recommended.



