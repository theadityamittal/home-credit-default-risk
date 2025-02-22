# Home Credit Default Risk - Data Science for Business

## Project Overview
This project aims to improve loan default prediction using machine learning models. Many applicants lack formal credit history, leading to high rejection rates. By leveraging alternative data sources and advanced feature engineering, this project enhances credit risk assessment for financial institutions.

## Business Problem
### Objective
Traditional credit scoring models systematically exclude individuals with limited or no formal credit documentation. This project applies predictive modeling techniques to assess loan repayment probabilities, enabling more inclusive lending decisions.

### Target Stakeholders
- **Financial Institutions**: Improve credit risk assessment and minimize loan defaults.
- **Potential Borrowers**: Gain access to formal credit despite limited credit history.
- **FinTech Companies**: Develop data-driven lending solutions.
- **Regulatory Bodies**: Ensure fairness and transparency in lending models.

### Impact
- Enhances financial inclusion by improving access to credit.
- Reduces loan default rates through more accurate risk modeling.
- Optimizes lending strategies for financial institutions.

## Project Structure
```
home-credit-default-risk/
│── data/
│   ├── processed/       # Cleaned and transformed data
│   ├── raw/             # Original datasets from Kaggle
│   ├── application_train.csv  
│   ├── application_test.csv  
│   ├── bureau.csv  
│   ├── bureau_balance.csv  
│   ├── previous_application.csv  
│   ├── credit_card_balance.csv  
│   ├── POS_CASH_balance.csv  
│   ├── installments_payments.csv  
│── notebooks/
│   ├── feature_engineering.ipynb
│   ├── feature_selection.ipynb
│   ├── Team9_baseline_models.ipynb
│   ├── Team9_EDA.ipynb
│   ├── Team9_final_model_evaluation.ipynb
│── submissions/       # Kaggle submission files
│── README.md
│── requirements.txt
```

## Methodology
### 1. Data Understanding and Exploratory Data Analysis (EDA)
- The dataset is sourced from Kaggle's [Home Credit Default Risk](https://www.kaggle.com/competitions/home-credit-default-risk/data).
- The analysis begins with `Team9_EDA.ipynb`, which explores missing values, class distributions, and correlations.

### 2. Feature Engineering
- Features are extracted from loan history, income trends, and repayment behavior.
- Data types are optimized for memory efficiency.
- Implemented in `feature_engineering.ipynb`.

### 3. Feature Selection
- Highly correlated features are removed using a correlation matrix.
- Feature importance is assessed using Random Forest.
- The dataset is reduced to 498 selected features.
- Implemented in `feature_selection.ipynb`.

### 4. Model Development
- Several machine learning models are evaluated in `Team9_baseline_models.ipynb`:
  - Logistic Regression
  - Logistic Regression with L1 (Lasso) and L2 (Ridge) regularization
  - Random Forest
- The final model is trained and validated in `Team9_final_model_evaluation.ipynb` using XGBoost.

## Model Performance
| Model                    | AUC Score |
|--------------------------|----------|
| Logistic Regression      | 0.7339   |
| Random Forest           | 0.7239   |
| XGBoost (Final Model)   | 0.7783   |

XGBoost was selected as the final model due to its superior AUC score, ability to handle missing values, and capability to capture complex relationships in the data.

## Installation and Setup
### Clone the Repository
```bash
git clone https://github.com/your-repo/home-credit-default-risk.git
cd home-credit-default-risk
```

### Install Dependencies
```bash
pip install -r requirements.txt
```

### Download the Dataset
- The dataset can be downloaded from **[Kaggle](https://www.kaggle.com/competitions/home-credit-default-risk/data)**.
- Extract the files into the `data/raw/` directory.

### Run Jupyter Notebooks
```bash
jupyter notebook
```
- **Feature Engineering** (`notebooks/feature_engineering.ipynb`)
- **Feature Selection** (`notebooks/feature_selection.ipynb`)
- **Baseline Models** (`notebooks/Team9_baseline_models.ipynb`)
- **Final Model Evaluation** (`notebooks/Team9_final_model_evaluation.ipynb`)

## Future Work
- Enhance interpretability using SHAP values for feature importance.
- Explore deep learning models for credit risk assessment.
- Incorporate real-time financial data sources to improve predictions.

For further details, refer to the final project report.
