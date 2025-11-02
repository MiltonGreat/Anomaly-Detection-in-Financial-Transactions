# Anomaly-Detection-in-Financial-Transactions
This project implements a multi-tier anomaly detection framework for identifying suspicious financial transactions in the PaySim synthetic financial dataset. The system combines Isolation Forest and Autoencoder approaches with SHAP explainability to provide transparent, AI-powered fraud detection.

#### Key Features:

- Multi-Method Detection: Isolation Forest + Autoencoder ensemble
- Comprehensive Evaluation: ROC curves, Precision-Recall analysis
- Model Explainability: SHAP analysis for feature importance
- Behavioral Clustering: PCA-based transaction pattern analysis
- Business Insights: Actionable recommendations for fraud prevention

### Dataset

**PaySim Synthetic Financial Dataset**
- Source: Kaggle - Synthetic Financial Datasets for Fraud Detection
- Type: Synthetic mobile money transactions
- Size: 100,000 transactions (sampled)
- Fraud Rate: ~0.1% (highly imbalanced)

Dataset Features:

- step: Time unit (1 hour increments)
- type: Transaction type (CASH_OUT, CASH_IN, TRANSFER, etc.)
- amount: Transaction amount
- nameOrig: Origin account
- nameDest: Destination account
- oldbalanceOrg, newbalanceOrig: Origin account balances
- oldbalanceDest, newbalanceDest: Destination account balances
- isFraud: Fraud label (target variable)

## Project Architecture

**Tier 1: Foundational Anomaly Detection**
- Isolation Forest: Tree-based anomaly detection
- Autoencoder: Neural network reconstruction error
- Ensemble Method: Combined scoring approach

**Tier 2: Model Evaluation & Comparison**
- ROC Curve Analysis: Overall discrimination ability
- Precision-Recall Curves: Performance on imbalanced data
- F1-Score Optimization: Balanced metric evaluation

**Tier 3: Model Explainability**
- SHAP Analysis: Feature contribution explanations
- Individual Case Studies: Fraud transaction explanations
- Feature Importance: Key drivers of anomaly detection

**Advanced Analysis**
- Behavioral Clustering: PCA-based pattern discovery
- Fraud Pattern Analysis: Characteristics of detected anomalies
- Performance Summary: Business impact assessment

<img width="898" height="291" alt="screenshot-localhost_8888-2025 11 02-10_04_10" src="https://github.com/user-attachments/assets/5aa52b08-4e8c-4168-b955-f6adebc8761b" />

## Key Findings:

- Best Performance: Autoencoder (F1-Score: 0.086)
- Detection Rate: 5/116 fraud cases detected (4.3%)
- False Positives: 995 normal transactions flagged
- Key Features: Transaction type, balance changes, amount ratios

## Source

[Synthetic Financial Datasets For Fraud Detection](https://www.kaggle.com/datasets/ealaxi/paysim1)
