# Logistic Regression Analyzer

A Jupyter notebook to analyze logistic regression models, calculate p-values for coefficients, and compute R-squared and adjusted R-squared.

## Installation

Clone the repository and install the required packages:

```bash
git clone https://github.com/yourusername/LogisticRegressionAnalyzer.git
cd LogisticRegressionAnalyzer
pip install -r requirements.txt
```

## Usage

Place your data in the `data` directory and adjust the example usage in `LogisticRegressionAnalyzer.ipynb` as needed.

Run the notebook:

```bash
jupyter notebook LogisticRegressionAnalyzer.ipynb
```

## How P-Values, R-Squared, and Adjusted R-Squared are Calculated

### P-Values

P-values in logistic regression are used to determine the significance of each predictor variable. The steps to calculate p-values are as follows:

1. **Predicted Probabilities**: Calculate the predicted probabilities for each observation using the logistic regression model.
2. **Variance-Covariance Matrix**: Construct the variance-covariance matrix of the predictors using the predicted probabilities.
3. **Standard Errors**: Extract the standard errors of the coefficients from the variance-covariance matrix.
4. **Wald Statistics**: Compute the Wald statistics by dividing the coefficients by their standard errors.
5. **P-Values**: Calculate the p-values using the chi-squared distribution applied to the squared Wald statistics.

### R-Squared (McFadden's R-Squared)

McFadden's R-squared is a measure of model fit for logistic regression models. It is calculated as follows:

1. **Log-Likelihood of the Fitted Model**: Calculate the log-likelihood of the logistic regression model with the predictors.
2. **Log-Likelihood of the Null Model**: Calculate the log-likelihood of the null model (a model with only an intercept).
3. **McFadden's R-Squared**: Compute R-squared using the formula:

![alt text](images\image-1.png)

### Adjusted R-Squared

Adjusted R-squared adjusts the R-squared value based on the number of predictors and observations, providing a more accurate measure of model fit. It is calculated as follows:

1. **Number of Observations (n)**: Total number of data points.
2. **Number of Predictors (p)**: Number of predictor variables.
3. **Adjusted R-Squared**: Compute adjusted R-squared using the formula:

![alt text](images\image-2.png)

### Example

The provided notebook demonstrates how to use the `LogisticRegressionAnalyzer` class to fit a logistic regression model, calculate p-values, R-squared, and adjusted R-squared. Simply replace the data loading section with your dataset, and run the notebook to see the results.
