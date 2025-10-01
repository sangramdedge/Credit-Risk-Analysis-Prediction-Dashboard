<img width="1397" height="788" alt="image" src="https://github.com/user-attachments/assets/7c907871-c816-496a-9747-6851b3c385aa" />
Credit Risk Analysis & Prediction Dashboard
📌 Project Overview

This project focuses on credit risk analysis using SQL, Python, and Power BI.
We built an end-to-end pipeline that starts with raw loan applicant data and ends with an interactive dashboard for stakeholders to monitor loan defaults.

🛠️ Tech Stack

SQL (PostgreSQL, pgAdmin4) → Data cleaning, transformations, feature engineering.

Python (Pandas, Scikit-learn, XGBoost, Random Forest) → ML model training & evaluation.

Power BI → Dashboard for visualization & business insights.

🔑 Steps Implemented
1️⃣ Data Preparation (SQL)

Imported loan applicant dataset into PostgreSQL.

Cleaned missing values (median imputation for numeric, mode for categorical).

Engineered new features:

Loan-to-Income Ratio

Employment Category (Binned Employment Length)

Age Bands, Income Bands, Interest Rate Bands

Verified data distributions and default rates by categories.

2️⃣ Machine Learning (Python)

Encoded categorical variables using OneHotEncoder.

Built pipelines with Random Forest and XGBoost.

Tuned hyperparameters using GridSearchCV.

Achieved strong performance:

Accuracy: ~93%

Recall (Defaults): ~75% after tuning XGBoost.

Extracted feature importances (Top predictors: Loan-to-Income, Income, Interest Rate, Loan Amount).

Generated predictions + default probabilities for new applicants (scalable to 5,000+ at once).

3️⃣ Dashboard (Power BI)

### A. Power BI (Modeling & Visualization)
- Imported Python-cleaned dataset into Power BI.  
- Built DAX measures:  
  - `Default Probability`  
  - `Actual Loss` (observed defaults)  
  - `Expected Loss` = Exposure × PD × LGD  
- Designed an **interactive Credit Risk Dashboard** with slicers for Loan Intent, Loan Grade, and Income Range.

### B. Business Insights
- **Good Loans %:** 78.18%  
- **Default Rate:** 22%  
- **Predicted Defaults:** 21.82%  
- **Expected Loss:** $68.16M  
- **Total Loan Amount at Risk:** $77M  
- Top risky purposes: **Debt Consolidation (29%)**, **Medical (27%)**, **Home Improvement (26%)**  
- Highest risk employment category: **New Employees (0–2 yrs, 30%)**  


📊 Key Insights

Higher Loan Grades (F, G) have default rates > 70%.

Debt Consolidation loans form the largest share of defaults.

Loan-to-Income ratio and Interest Rate are the strongest predictors of default.

Employment Category shows higher defaults among early-career borrowers.

XGBoost model outperformed Random Forest in recall for defaults.

🚀 How to Run

Clone this repo.

Load the SQL scripts in PostgreSQL to clean & prep data.

Run model_training.ipynb in Python to train & evaluate models.

Open the Power BI file (Loan Defaulters Final.pbix) to interact with the dashboard.


📌 Next Steps (Future Improvements)

Deploy ML model as a Flask API for real-time scoring.

Connect API to Power BI for live scoring dashboards.

Add survival analysis for loan tenure risk.

Experiment with Neural Networks (TabNet, AutoML) for further improvement.

✨ This project demonstrates the integration of SQL, ML, and BI to deliver a full-stack analytics solution for credit risk management.
