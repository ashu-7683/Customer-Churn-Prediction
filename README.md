# Customer Churn Prediction Analysis

## Project Overview
This project analyzes customer churn data and builds predictive models to identify customers at risk of churning. The analysis includes data preprocessing, feature engineering, and machine learning model development to predict customer churn behavior.

## Dataset
- **File**: `data/customer_churn.csv`
- **Rows**: 900 customers
- **Features**: Age, Monthly Charges, Account Manager, Tenure, Number of Sites, Location, etc.
- **Target**: Churn (1 = churned, 0 = retained)

## Data Preprocessing Steps
1. **Data Loading**: Loaded the dataset using pandas
2. **Feature Selection**: Removed irrelevant columns (Names, Company)
3. **Date Processing**: 
   - Converted date strings to datetime objects
   - Extracted year from dates as a new feature
4. **Categorical Encoding**: One-hot encoded Location column
5. **Missing Values**: Handled null values by dropping rows with NaN
6. **Data Splitting**: Split data into training (70%) and testing (30%) sets

## Feature Engineering
- Created `date_year` feature from the original date column
- One-hot encoded categorical Location data
- Normalized numerical features using StandardScaler

## Modeling Approach
- **Algorithm Used**: Logistic Regression
- **Validation**: Train-test split with random_state=42
- **Metrics**: Accuracy score and classification report
