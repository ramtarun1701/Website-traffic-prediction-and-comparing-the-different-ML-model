The dataset contains 2000 entries with 7 columns:

Page Views (int)
Session Duration (float)
Bounce Rate (float)
Traffic Source (object, categorical)
Time on Page (float)
Previous Visits (int)
Conversion Rate (float, target variable)
There are no missing values in the dataset. Next, we have to check for outliers and then proceed with encoding the categorical variable "Traffic Source" using one-hot encoding

The boxplots reveal potential outliers in some columns, particularly in "Session Duration" and "Bounce Rate." I'll investigate these columns further to determine if any values are extreme outliers that may need handling.

There are 112 outliers in "Session Duration" and 13 in "Bounce Rate." Since the outliers in "Session Duration" represent a relatively larger portion of the data, we can decide to either remove or cap them to reduce their impact on the model. We’ll proceed by capping the outliers at the upper and lower bounds for these two columns.




Key Metrics to Compare:
Mean Absolute Error (MAE): Lower MAE indicates fewer absolute prediction errors.
Mean Squared Error (MSE) and Root Mean Squared Error (RMSE): Lower values show the model has smaller squared errors, which penalizes larger deviations.
R-squared (R²): Measures how well the model explains the variability of the target variable. Higher values indicate better model fit.
Adjusted R-squared: Adjusts R² based on the number of predictors, penalizing excessive complexity.
Interpreting Results
If Polynomial Regression has higher R² and Adjusted R² values and lower MAE/RMSE compared to Multiple Linear Regression, it suggests that Polynomial Regression captures nonlinear patterns better, leading to improved performance.
Conversely, if the Multiple Linear Regression performs similarly or better in terms of MAE, RMSE, and Adjusted R² with simpler interpretation, it may be the preferred model due to lower complexity.
Residual Analysis
Residual plots: Check if residuals are randomly dispersed around zero. Patterns in residuals can indicate model misspecification or the presence of nonlinear relationships that the model fails to capture.
Conclusion
If Polynomial Regression shows better performance: It suggests that the relationship between predictors and the conversion rate includes nonlinear patterns. You might choose Polynomial Regression to capture this complexity more accurately. However, check for overfitting, especially with higher degrees of polynomial terms.

If Multiple Linear Regression performs similarly: It may be preferable for its simplicity, especially if the performance difference is marginal. This choice would be supported by straightforward interpretation and lower risk of overfitting.
