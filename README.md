# Predicting 10-Year Cancer Survival Rates Using XGBoost

## Data Source

The dataset was obtained from **John Snow Labs Marketplace**:

**Adult Cancer Survival in England (2013–2017)**  
Source: https://www.johnsnowlabs.com/marketplace/adult-cancer-survival-in-england-2013-to-2017/

This dataset contains population-level cancer survival statistics collected in England between 2013 and 2017, including survival rates by cancer type, age group, sex, and patient counts. The data is intended for research and analytical purposes and does not contain individual patient records.

The target variable used in this project is the **10-year survival rate (%)**, derived from the reported survival statistics.

## Objective
The goal of this project is to predict 10-year cancer survival rates using demographic and cancer-related population data. This is a regression task aimed at identifying patterns and trends across cancer types and patient groups, rather than making individual clinical predictions.

## Dataset
The dataset contains population-level cancer statistics, including:
- Cancer type
- Age group
- Sex
- Age-standardized survival rates
- Number of patients

The target variable is the **10-year survival rate (%)**.

## Data Preprocessing
The following preprocessing steps were applied:
- Handling missing values using median imputation for numerical features
- Encoding categorical variables using OneHotEncoder
- Feature scaling where appropriate
- Dataset splitting into training and test sets

A preprocessing pipeline was built using `ColumnTransformer` to ensure consistent transformations.

## Model
An **XGBoost Regressor** was used due to its strong performance on structured tabular data and ability to capture non-linear relationships.

## Evaluation Metrics
Model performance was evaluated using:
- **R² Score ≈ 0.8088**
- **RMSE ≈ 10.4354**

These results indicate that the model explains approximately 80% of the variance in 10-year survival rates, which is strong for population-level clinical data.

## Feature Importance
Feature importance analysis shows that:
- Cancer type
- Age-related variables
- Population metrics

<img width="1102" height="447" alt="image" src="https://github.com/user-attachments/assets/e068e1d0-b2ea-4c3d-9d0e-901333deb0d6" />


contribute most strongly to survival rate predictions. This aligns with known epidemiological trends, suggesting that the model is learning meaningful clinical patterns rather than noise.

## Conclusions
- The model demonstrates strong predictive performance for 10-year survival rates at the population level.
- Predictions are more accurate for mid-range survival values, with higher error at extreme values, likely due to data sparsity and biological variability.
- The model is suitable for trend analysis and comparative studies across cancer groups, but not for individual patient prognosis.

<img width="988" height="789" alt="image" src="https://github.com/user-attachments/assets/6ae4cda4-281f-4083-9e92-1a52e1914720" />


## How to Run
1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/your-repo-name.git
