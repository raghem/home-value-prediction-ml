# Home Value Prediction Using Multiple Linear Regression

## Author
**Raghe Mahamud**  
Course: D600 – Task 1  
Instructor: Eric Straw 
---

## Project Overview
This project analyzes how **square footage** and **crime rate** affect **home prices** using multiple linear regression. The goal is to quantify how changes in these variables impact housing value and assess the model’s predictive performance.

---

## Research Question
**Do square footage and crime rate affect a home’s value, and by how much?**

Specifically:
- How much does increasing square footage increase home value?
- How much does an increase in crime rate decrease home value?

---

## Objective
The goal is to estimate home prices using square footage and crime rate. In a real-world real estate context, this model could help:
- Estimate prices of unlisted or future homes
- Support land-use and investment decisions
- Identify high-value development opportunities

---

## Data & Variables

### Dependent Variable
- **Home Price**

### Independent Variables
- **Square Footage**
- **Crime Rate**

These variables are quantitative and commonly used in real estate valuation.

---

## Exploratory Data Analysis

### Descriptive Statistics
Summary statistics were generated for price, square footage, and crime rate.

### Visualizations
- Univariate plots for each variable
- Bivariate plots:
  - Price vs. Square Footage (positive relationship)
  - Price vs. Crime Rate (negative relationship)

---

## Model Development

### Data Split
- **80% training / 20% testing**
- Used `train_test_split` from scikit-learn

### Optimization Method
**Backward Elimination**
- Removed predictors with p-values > 0.05
- Evaluated model using:
  - Adjusted R²
  - F-statistics
  - Coefficients
  - p-values

---

## Model Performance

### Mean Squared Error (MSE)
- **Before optimization:**  
  RMSE ≈ \$126,197.69
- **After optimization:**  
  RMSE ≈ \$123,173.41

**Improvement:**  
Backward elimination reduced error by **\$3,024.28**

---

## Model Assumptions Verification

- **Multicollinearity:**  
  VIF ≈ 1 for both predictors → no collinearity
- **Sample Size:**  
  ~7,000 rows (well above minimum requirement)
- **Linearity:**  
  Linear trends observed in scatterplots
- **Normality of Residuals:**  
  Histogram and Q-Q plot showed normal distribution
- **Homoscedasticity:**  
  Residuals showed constant variance
- **Independence of Errors:**  
  No patterns in residual order plot

---

## Final Model Equation

\[
Price = 111{,}500 + 195.74(\text{Square Footage}) - 296.44(\text{Crime Rate}) + \epsilon
\]

### Interpretation
- Each additional square foot **increases price by \$195.74**
- Each unit increase in crime rate **decreases price by \$296.44**
- Average prediction error ≈ **\$122,000**

---

## Model Metrics
- **R²:** 0.306  
- **Adjusted R²:** 0.306  

The model explains **30.6%** of the variance in home prices, indicating other variables also play a significant role.

---

## Results & Recommendations
- Larger homes are associated with higher prices
- Higher crime rates reduce home value
- The model is informative but incomplete

### Recommended Next Steps
- Add more predictors (location, age, amenities, schools)
- Re-run regression for improved accuracy
- Focus development on **low-crime areas with larger homes**

---

## Tools & Libraries
- **Pandas** – data handling
- **Seaborn** – visualization
- **Matplotlib** – plotting
- **Scikit-learn** – regression, metrics, data split
- **Statsmodels** – statistical modeling

---

## Sources
No external sources were used beyond official WGU materials.


## Related Projects
- [Home Value Prediction (Regression)](https://github.com/yourusername/home-value-prediction-ml)
- [Luxury Home Classification (Logistic Regression)](https://github.com/yourusername/luxury-home-classification-ml)

