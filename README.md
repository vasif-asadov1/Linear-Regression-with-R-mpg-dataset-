# Linear Regression with R

**Author:** Vasif Asadov

This project presents a complete end-to-end implementation of a linear regression modeling pipeline in R using the built-in `mpg` dataset from the `ggplot2` package. The primary objective is to predict **city fuel efficiency (city MPG)** based on vehicle characteristics while maintaining statistical rigor, interpretability, and generalization performance.

The project emphasizes proper data preprocessing, multicollinearity control, feature significance testing, and robust model evaluation rather than relying solely on predictive accuracy.

## Project Links

HTML Report (GitHub Pages):  
https://vasif-asadov1.github.io/Linear-Regression-with-R-mpg-dataset-/

GitHub Repository:  
https://github.com/vasif-asadov1/Linear-Regression-with-R-mpg-dataset-

## Project Objective

The goal of this project is to build an interpretable linear regression model to estimate city fuel efficiency using vehicle attributes such as engine displacement, number of cylinders, transmission type, drive type, fuel type, highway MPG, and vehicle class. The target variable of interest is **city_mpg**.

The project focuses on understanding feature relationships, eliminating redundancy, and ensuring that the final model satisfies statistical assumptions commonly required in classical linear modeling.

## Data Processing and Cleaning

The workflow begins with exploratory analysis of the `mpg` dataset to inspect feature structure, data types, and distributions. Variable names are standardized for clarity and readability. Duplicate observations are identified and removed, and the dataset is verified to contain no missing values. Outlier inspection using box plots confirms that no extreme values require treatment.

## Feature Engineering and Preprocessing

Categorical variables are transformed using One-Hot Encoding to allow compatibility with linear modeling. Numerical features are scaled to ensure comparable magnitudes and stable coefficient estimation. Encoded categorical variables, scaled numerical features, and the target variable are combined into a single modeling dataset.

## Multicollinearity Analysis

A Generalized Linear Model (GLM) is constructed to evaluate multicollinearity using Variance Inflation Factor (VIF). Perfectly collinear features are detected and removed. High-VIF features are iteratively eliminated until all remaining predictors satisfy acceptable multicollinearity thresholds. This step ensures coefficient stability and interpretability.

## Model Training

The cleaned dataset is converted into H2O’s optimized data format. The data is split into training and testing subsets using an 80/20 ratio. A linear regression model is trained using H2O’s GLM implementation with 10-fold cross-validation. Statistical significance of predictors is evaluated using p-values, and insignificant features are iteratively removed from the model.

## Model Evaluation

Model performance is evaluated using Root Mean Squared Error (RMSE), R², and Adjusted R². Metrics are computed on both training and test sets to assess generalization. Comparable Adjusted R² values across training and testing indicate that the model does not suffer from overfitting or underfitting.

## Visualization and Diagnostics

Interactive visualizations are generated to compare predicted and observed city MPG values for both training and test datasets. These plots provide clear diagnostic insight into model fit and residual behavior and help validate linear regression assumptions.

## Conclusion

This project demonstrates that linear regression remains a powerful and interpretable modeling technique when supported by rigorous preprocessing, multicollinearity control, and statistical feature selection. The final model achieves strong explanatory power while maintaining stability and generalization performance, making it suitable for both academic evaluation and practical analysis.

## Notes

The HTML report is fully self-contained and interactive. All accompanying `_files` directories are required for correct rendering on GitHub Pages. This project is suitable for coursework submission, portfolio presentation, or demonstration of applied statistical modeling skills in R.







