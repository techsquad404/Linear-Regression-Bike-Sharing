# Bike Sharing Demand Prediction

This project aims to build a linear regression model to predict bike-sharing demand using historical data. The dataset contains various features such as weather conditions, seasonal information, and calendar data.

## Project Overview

The main objectives of this project are:

1. **Data Understanding and Preparation**
   - Perform data quality checks.
   - Handle categorical variables appropriately.
   - Create dummy variables where applicable.
   - Derive new metrics if necessary.
   - Convert the data into a clean format suitable for analysis.

2. **Model Building and Evaluation**
   - Tune model parameters.
   - Use correct variable selection techniques.
   - Attempt different models and choose the best one based on key performance metrics.
   - Perform residual analysis after model building.
   - Validate model assumptions.
   - Evaluate the model using appropriate metrics.

## Data Understanding and Preparation

### Data Quality Checks
- The dataset was checked for missing values, duplicates, and inconsistencies.
- No significant data quality issues were found.

### Handling Categorical Variables
- Categorical variables such as `season`, `weathersit`, `mnth`, and `weekday` were converted to dummy variables using one-hot encoding.

### Dummy Variables
- Dummy variables were created for categorical features, ensuring that the first category was dropped to avoid multicollinearity.

### New Metrics
- A new metric `temp_celsius` was derived from the `temp` variable to represent temperature in Celsius. This is not required for this analysis

### Data Cleaning
- The dataset was cleaned and prepared for analysis by dropping unnecessary columns and handling multicollinearity.

## Model Building and Evaluation

### Variable Selection
- Variance Inflation Factor (VIF) was used to check for multicollinearity.
- Variables with high VIF values (e.g., `temp` and `atemp`) were dropped to improve the model.
- Used RFE to decide the feature selection

### Model Training
- The data was split into training and testing sets using an 80-20 split.
- An Ordinary Least Squares (OLS) regression model was trained using the training data.

### Model Evaluation
- The model was evaluated on the test data.
- Key performance metrics such as RMSE, R-squared, and adjusted R-squared were calculated.
- Residual analysis was performed to validate the model assumptions.

### Residual Analysis
- Residuals were calculated as the difference between the actual and predicted values.
- The distribution of residuals was visualized using a histogram.
- A scatter plot was used to visualize the predicted values against the actual values.

## Results
- The final model had an standard R-squared value and an adjusted R-squared value.
- The model performed well in predicting bike-sharing demand based on the available features.

