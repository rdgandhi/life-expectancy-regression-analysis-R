# Life Expectancy Analysis: Predicting Key Influencing Factors

## Overview
This project identifies the most significant factors influencing life expectancy across countries and regions using a dataset from the World Health Organization (WHO) and United Nations. The analysis employs **multiple linear regression** to explore relationships between life expectancy and health, socio-economic, and demographic indicators. The goal is to provide actionable insights for policymakers to improve global health outcomes.

**Key Questions Addressed**:
- What are the strongest predictors of life expectancy?
- How do immunization rates, GDP, and education correlate with life expectancy?
- Are there regional differences in predictors of life expectancy?

## Key Features
- **Data Source**: Publicly available dataset from Kaggle ([Life Expectancy (WHO)](https://www.kaggle.com/datasets/lashagoch/life-expectancy-who-updated)) with 193 countries and 15 years (2000–2015).
- **Variables Analyzed**: 20+ predictors, including infant mortality, adult mortality, GDP, vaccination rates, BMI, and schooling.
- **Techniques Used**:
  - Multicollinearity detection using Variance Inflation Factor (VIF).
  - Stepwise regression for model selection (AIC, BIC, Mallows' Cp).
  - Higher-order and interaction terms to capture non-linear relationships.
  - Residual diagnostics (normality, homoscedasticity, independence).
- **Tools**: R, ggplot2, GGally, and statistical modeling packages.

## Methodology
1. **Data Preprocessing**:
   - Replaced country-level data with regional aggregates to reduce complexity.
   - Removed collinear variables (e.g., under-five deaths, diphtheria vaccination).
   
2. **Model Building**:
   - Initial first-order model refined using stepwise regression.
   - Tested interaction and higher-order terms to improve fit.
   - Final model selected based on adjusted R², AIC, and BIC.

3. **Validation**:
   - Checked residual assumptions (linearity, normality, homoscedasticity).
   - Addressed heteroscedasticity with Box-Cox transformation (partial success).
   - Identified key predictors using F-tests and t-tests.

## Results
- **Top Predictors**:
  - **Infant Mortality** (negative impact: β = -0.1189, *p* < 0.001).
  - **Adult Mortality** (negative impact: β = -0.06159, *p* < 0.001).
  - **Economic Status** (developed countries: +2.08 years, *p* < 0.001).
  - **Schooling** (+0.11 years per additional year, *p* < 0.001).

- **Regional Differences**:
  - Central America & Caribbean: +2.13 years vs. baseline (Africa).
  - Oceania: -0.45 years vs. baseline.

- **Model Performance**:
  - Adjusted R²: 0.9846.
  - RMSE: 1.167 years.

## Conclusion
- Economic development, healthcare access, and education are critical drivers of life expectancy.
- Regional disparities highlight the need for targeted interventions.
- **Policy Implications**: Prioritize reducing infant mortality, improving vaccination coverage, and investing in education.

## Skills Demonstrated
- **Statistical Analysis**: Regression modeling, hypothesis testing, multicollinearity handling.
- **Data Visualization**: Residual plots, correlation matrices, regional comparisons.
- **Tools**: R, ggplot2, stepwise regression, model diagnostics.
- **Collaboration**: Team-based workflow with roles in data cleaning, modeling, and visualization.

## References
- Dataset: [Life Expectancy (WHO)](https://www.kaggle.com/datasets/lashagoch/life-expectancy-who-updated) (CC0: Public Domain).
