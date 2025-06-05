# RECELL-Linear Regression Model
**Overview**

This project demonstrates the application of a linear regression model to predict the normalized used price of products based on various features. The dataset comprises 3,454 samples with 48 predictor variables. The model was developed using Python's statsmodels library and evaluated using several performance metrics.

**Exploratory Data Analysis (EDA)**

Exploratory Data Analysis (EDA) is a crucial first step in data analysis, allowing us to understand the dataset's structure, detect anomalies, and uncover underlying patterns. In this project, EDA was performed to assess data quality and inform subsequent modeling decisions.

**Key EDA Steps:**

- Data Inspection: Loaded the dataset and examined its dimensions, column names, and data types.

- Missing Values: Identified and handled missing data appropriately to ensure model accuracy.

- Statistical Summary: Generated summary statistics to understand the distribution and central tendencies of numerical features.

- Visualizations: Created histograms, box plots, and scatter plots to visualize data distributions and relationships between variables.

- Correlation Analysis: Computed correlation matrices to identify potential multicollinearity among features.
**Linear Regression Model Development**
  
Following EDA, a Multiple Linear Regression (MLR) model was developed to predict the target variable, normalized_used_price, based on various predictors.

**Modeling Steps:**

- Data Preparation: Defined predictors (X) and target (y), and added a constant to the predictors.

- Data Splitting: Divided the dataset into training (70%) and testing (30%) sets.

- Model Fitting: Trained the model using Ordinary Least Squares (OLS) regression.

- Feature Selection: Performed stepwise regression to select significant features, removing those with high p-values.

- Multicollinearity Check: Assessed Variance Inflation Factors (VIF) to detect and address multicollinearity.

**Model Evaluation**

Performance metrics on the test set are as follows:

- RMSE: 0.240541

- MAE: 0.189391

- R-squared: 0.830093

- Adjusted R-squared: 0.827596

- MAPE: 4.541333%

- MSE: 0.05786

These metrics suggest a strong fit of the model to the data.

**Assumption Checks**

Assumptions of linear regression were validated:

- **Linearity:** Assessed via residual plots.

- **Normality:** Residuals approximately follow a normal distribution (Shapiro-Wilk test p-value < 0.05).

- **Homoscedasticity:** No evidence of heteroscedasticity (Goldfeld-Quandt test p-value > 0.05).

- **Multicollinearity**
Variance Inflation Factor (VIF) analysis identified multicollinearity among certain predictors. Features with high VIF values were removed iteratively, leading to a refined model.

**Final Model**

After addressing multicollinearity and selecting significant predictors, the final model was retrained. Performance metrics remained consistent with the initial evaluation.

**Conclusion**

The linear regression model effectively predicts the normalized used price, with strong performance metrics and validated assumptions. Future work may explore regularization techniques to further enhance model robustness.

