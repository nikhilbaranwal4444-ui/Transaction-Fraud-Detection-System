## Dataset Access
The dataset used in this project is too large to be hosted on GitHub.

You can download it from:
https://drive.google.com/file/d/1fL43e1xica6jlf2hPl6NrnoTgdgPGB_-/view?usp=drive_link

Project Overview

This project focuses on detecting fraudulent transactions in a large-scale mobile money dataset using rule-based fraud detection techniques and feature engineering. The dataset simulates real-world financial transactions with highly imbalanced fraud cases.
The goal is to understand fraud behavior, build a strong baseline system, and prepare the pipeline for machine learning models.

📂 Dataset
Simulated mobile money transactions (PaySim-based)
Over 6 million transactions
Fraud cases represent < 1% of the data

Key Features:
Transaction type (TRANSFER, CASH_OUT, PAYMENT, etc.)
Sender and receiver balances before and after transactions
Fraud and flagged fraud indicators

Fraud Patterns Observed
Fraud is highly concentrated in TRANSFER and CASH_OUT transactions
Fraudsters often empty the origin account
Balance inconsistencies are common in fraudulent transactions
Many fraud cases are not flagged by rule-based thresholds

🛠 Feature Engineering
The following features were created:
orig_balance_diff – Difference between sender’s old and new balance
dest_balance_diff – Difference between receiver’s balances
high_risk_type – Indicator for TRANSFER or CASH_OUT
account_emptied – Detects complete balance drain
balance_mismatch – Flags inconsistencies between amount and balance change
large_txn – Identifies high-value transactions

🚨 Rule-Based Fraud Scoring
A fraud score was assigned to each transaction:
| Rule                       | Score |
| -------------------------- | ----- |
| High-risk transaction type | +2    |
| Large transaction amount   | +2    |
| Account emptied            | +3    |
| Balance mismatch           | +2    |
Transactions with a fraud score ≥ 5 are classified as fraudulent.

📊 Model Evaluation
Performance was evaluated using:
Confusion Matrix
Precision, Recall, F1-score
Special focus was placed on recall, as missing fraud cases is costlier than false alarms.

🧠 Key Learning Outcomes
Handling highly imbalanced datasets
Translating business rules into data-driven features
Understanding limitations of rule-based fraud detection
Building ML-ready fraud pipelines

📬 Contact
Author: Nikhil kumar
📧 Email: nikhilbaranwal4444@gmail.com
🔗 LinkedIn: www.linkedin.com/in/nikhil-kumar-015359175
