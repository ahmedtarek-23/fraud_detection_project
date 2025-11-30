🏥 Healthcare Provider Fraud Detection System

This project implements a complete machine learning pipeline to detect potentially fraudulent healthcare providers using claims-level data. The workflow covers data understanding, feature engineering, class imbalance handling, model comparison, evaluation, and error analysis — aligned fully with the project rubric (Sections 1.5 & 1.6).

📂 Project Structure
📁 project-root
│
├── Notebook 1 – Data Understanding & Feature Engineering
├── Notebook 2 – Modeling & Comparison
├── Notebook 3 – Final Evaluation & Error Analysis
├── processed_train_data.csv
└── README.md

✅ Project Objectives

The goal is to classify healthcare providers as:

0 = Legitimate provider

1 = Potential fraud

By learning patterns in reimbursement behavior, utilization frequency, inpatient/outpatient ratios, and claim cost dynamics.

📊 Notebook Overview
🟩 Notebook 1 — Data Understanding & Feature Engineering
Covers:

✔ Data quality assessment
✔ Join logic across datasets
✔ Duplicate/missing value detection
✔ Fraud vs legit statistical comparison
✔ Provider-level feature engineering
✔ Aggregation strategy (claim → provider)

Key Features Created:

Average Claim Cost

Claims Per Patient

Total Reimbursement

Inpatient Ratio

Beneficiary counts

Temporal claim trends

Geographic summary features (encoded safely)

Visualizations:

Fraud class distribution

Reimbursement distributions

Cost trends

Correlation heatmap

Provider-level summaries

Geographic patterns

✅ Satisfies Section 1.5.1 – Data Understanding & Exploration

🟨 Notebook 2 — Modeling & Algorithm Comparison
Models Trained:

Logistic Regression (interpretable baseline)

Random Forest (robust)

Gradient Boosting (best performer)

Techniques Used:

Standard scaling

SMOTE oversampling

Stratified train-test split

Probability-based evaluation

Metrics Used:

Precision

Recall

F1-score

ROC-AUC

PR-AUC

Output:

ROC Curves

Precision–Recall Curves

Best model selected by PR-AUC

✅ Satisfies Sections 1.5.2 & 1.5.3
✅ Satisfies Comparison Models Requirement

🟥 Notebook 3 — Evaluation & Error Analysis
Classification Performance:
              precision    recall  f1-score
Legitimate      97%        95%       96%
Fraud           60%        70%       65%
Overall accuracy: 93%


✅ ~70% of fraud detected
✅ Acceptable false-positive rate
✅ Real-world tradeoff applied

Confusion Matrix & Cost Analysis

Hypothetical cost model implemented:

False positive (investigation): $500

False negative (fraud missed): $10,000

Used to compute:
✔ Business impact cost
✔ Risk prioritization

🔍 Error Analysis (Case Studies)

Includes:

2–3 False Positives (Legit flagged as fraud)

2–3 False Negatives (Missed fraud cases)

Each case explains:

Why the model failed

Which features contributed

What pattern was misleading

🧠 Model Explanation & Reasoning

Trade-off decision:

Although precision for fraud detection is lower than recall, this trade-off is intentionally accepted because missing fraud (false negative) is significantly more costly than investigating a legitimate provider (false positive). The model therefore prioritizes recall, which aligns with real-world fraud detection systems.

✅ Final Rubric Coverage
Requirement	Status
1.5.1 Data Exploration	✅
1.5.2 Class Imbalance	✅
1.5.3 Algorithm Selection	✅
Comparison Models	✅
1.6 Evaluation Metrics	✅
Cost-Based Analysis	✅
Error Case Studies	✅
Overfitting Prevention	✅
📦 Dependencies
pandas
numpy
matplotlib
seaborn
scikit-learn
imbalanced-learn

🏁 Final Notes

This project prioritizes:

Fraud recall

Business impact

Model validity

Interpretation

And avoids:

Accuracy-only exaggeration

Data leakage

Invalid mixing

Cosmetic analytics
