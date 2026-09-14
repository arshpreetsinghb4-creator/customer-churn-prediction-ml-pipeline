Customer Churn Prediction ML Pipeline

An end-to-end machine learning pipeline for predicting customer churn using data preprocessing, outlier treatment, feature selection, feature standardisation, and Logistic Regression.

📌 Overview

Customer churn is an important business problem for retail and e-commerce companies. Identifying customers who are likely to churn can help retention teams take action before customers leave.

This project demonstrates a complete machine learning workflow using a deliberately messy customer dataset containing missing values, duplicate records, invalid entries, and outliers.

The pipeline takes the data from raw input to a final customer churn risk report.

🎯 Business Objective

The objective is to predict which customers are likely to churn so that a business can prioritise them for retention activities such as:

Customer follow-ups
Retention offers
Personalised communication
Loyalty incentives
Promotional campaigns
🔄 Machine Learning Pipeline
Raw Customer Data
        ↓
Data Collection
        ↓
Data Understanding
        ↓
Data Cleaning
        ↓
Outlier Detection & Treatment
        ↓
Feature Selection
        ↓
Target Variable Definition
        ↓
Target Encoding
        ↓
Train-Test Split
        ↓
Feature Standardisation
        ↓
Logistic Regression
        ↓
Prediction
        ↓
Model Evaluation
        ↓
Model Interpretation
        ↓
Churn Risk Report
📊 Dataset

The project uses:

SmartKart_dirty_100_rows.csv

The original dataset contains 100 customer records and 5 columns:

Column	Description
Customer_ID	Unique customer identifier
Age	Customer age
Monthly_Spend	Customer monthly spending
Complaints	Number of customer complaints
Churn	Customer churn indicator

The dataset intentionally contains data-quality issues such as:

Missing values
Duplicate records
Incorrect data types
Invalid age values
Negative spending values
Extreme outliers
🧹 Data Preprocessing

The project performs several preprocessing steps before model training.

Data Cleaning
Removes duplicate records
Removes unnecessary whitespace
Converts Age into numeric format
Corrects invalid text values
Handles invalid age values
Converts negative spending values to missing values
Fills missing values using the median

After cleaning, the dataset is reduced from 100 to 95 rows, with missing values handled.

Outlier Treatment

The project uses the IQR (Interquartile Range) method to identify extreme values.

Instead of deleting affected customer records, outliers are capped to reduce their influence on the Logistic Regression model.

The notebook identifies outliers in:

Monthly_Spend
Complaints




🤖 Machine Learning Model
Logistic Regression

The project uses Logistic Regression as the classification model.

The target variable is:

Churn

where:

0 = No Churn
1 = Churn

Logistic Regression is suitable for this binary classification problem and also provides interpretable model coefficients.

📈 Model Evaluation

The model is evaluated using classification metrics including:

Accuracy
Precision
Recall
F1-Score
Confusion Matrix
Classification Report

These metrics help assess how effectively the model identifies customers who are likely to churn.

💼 Business Output

The final stage of the pipeline produces a customer churn risk report.

The report can be used to identify and prioritise customers according to their predicted churn risk.

Customer Data
      ↓
Churn Prediction
      ↓
Churn Probability
      ↓
Risk Ranking
      ↓
Retention Action
🛠️ Technologies Used
Python
Pandas
NumPy
Matplotlib
Seaborn
Scikit-learn
Google Colab
Jupyter Notebook
📁 Project Structure
customer-churn-prediction-ml-pipeline/
│
├── SmartKart_Churn_Prediction_ML_Pipeline.ipynb
├── SmartKart_dirty_100_rows.csv
├── smartkart_churn_risk_report.csv
└── README.md
🚀 How to Run
Google Colab
Open SmartKart_Churn_Prediction_ML_Pipeline.ipynb in Google Colab.
Upload SmartKart_dirty_100_rows.csv when prompted.
Run the notebook from top to bottom.
Review the preprocessing and model evaluation results.
Generate the final churn-risk report.

The notebook is designed to be executed sequentially, with explanations provided throughout the pipeline.

Local Environment

Install the required libraries:

pip install pandas numpy matplotlib seaborn scikit-learn jupyter

Launch Jupyter Notebook:

jupyter notebook

Then open:

SmartKart_Churn_Prediction_ML_Pipeline.ipynb
🔍 Key Concepts Demonstrated

This project demonstrates practical implementation of:

Data quality assessment
Data cleaning
Missing-value handling
Duplicate removal
Data type conversion
Invalid-value treatment
IQR-based outlier treatment
Feature selection
Binary classification
Train-test splitting
Feature standardisation
Logistic Regression
Churn prediction
Model evaluation
Model interpretation
Business-oriented ML reporting
📌 Project Limitations

The dataset contains only a small number of customer records and a limited set of predictive features.

For a production-level churn prediction system, additional customer behaviour and transaction features would be required.

Potential improvements include:

Customer tenure
Purchase frequency
Recency of last purchase
Average order value
Customer engagement
Product categories
Discount usage
Customer service interactions
Website or application activity
🔮 Future Improvements
Feature engineering
Cross-validation
Hyperparameter tuning
Comparison with other classification models
ROC-AUC analysis
Precision-Recall analysis
Handling class imbalance
Explainable AI
Interactive Streamlit dashboard
Automated prediction pipeline
Customer segmentation
Automated retention recommendations
Model monitoring and retraining
👨‍💻 Project Purpose

This project demonstrates how machine learning can be applied to a practical customer analytics and retention problem, starting from raw and imperfect data and ending with an actionable churn-risk output.

Domain: Customer Analytics | Retail | E-commerce
Machine Learning Task: Binary Classification
Model: Logistic Regression
Output: Customer Churn Risk Report
