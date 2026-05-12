## Article Source
https://machinelearningmastery.com/interpreting-coefficients-in-linear-regression-models/

## Summary 
This article explains how to interpret coefficients in Linear Regression models using the Ames Housing dataset.

The article mainly focuses on:
* Numerical feature interpretation
* Categorical feature interpretation
* Combining multiple features in one model

It demonstrates how coefficients help us understand the relationship between input features and target predictions.

The article also explains:
* One Hot Encoding
* Baseline category
* K-Fold Cross Validation
* R² Score
* Feature interactions

## Formulas
**Linear Regression Formula**
Basic regression equation :
y=b0 + b1x
where : 
* y = predicted output
* b0 = intercept
* b1 = coefficient
* x = input feature

**Multiple Linear Regression**
When multiple features are used :
y=b0+b1x1+b2x2+...+bnxn
where :
* x1,x2,...,xn = multiple features
* b1,b2,...,bn = feature coefficients

**House Price Prediction Formula**
SalePrice = b0 + b1(GrLivArea)

**Combined Feature Formula**
SalePrice = b0 + b1(GrLivArea) + b2(Neighborhood)

**R² Score Formula**
Used for model evaluation:
<img width="332" height="262" alt="image" src="https://github.com/user-attachments/assets/e0e3384d-dca3-4e2c-8694-745c3e6640f2" />

**Mean Calculation Formula**
Uesd in K - Fold Cross Validation :
<img width="223" height="238" alt="image" src="https://github.com/user-attachments/assets/cfed21b9-eb3c-48fe-a9d2-af28c2742689" />

## Examples
**Example 1 — Numerical Feature Interpretation**

Linear Regression Equation:
y = b0 + b1x
Suppose:
- b0 = 50000
- b1 = 110.52
- x = 1000 sq ft
Prediction:
SalePrice = 50000 + (110.52 × 1000)
SalePrice = 160520

Meaning:
A house with 1000 sq ft living area is predicted to cost about $160,520.

**Example 2 — Coefficient Meaning**

Coefficient = 110.52

Interpretation:
Every additional square foot increases house price by approximately $110.52.

If living area increases by 100 sq ft:
100 × 110.52 = 11052
House price increases by about $11,052.

**Example 3 — Baseline Category**

Baseline category:
MeadowV
Suppose:
NoRidge coefficient = 229423

Interpretation:
Houses in NoRidge are predicted to cost about $229,423 more than houses in MeadowV.

**Example 4 — One Hot Encoding**

Original Data:
Neighborhood = NoRidge
After One Hot Encoding:
Neighborhood_NoRidge = 1
Neighborhood_MeadowV = 0

This converts categorical data into numerical format.

**Example 5 — R² Score Interpretation**

Model 1:
R² = 0.51
Model 2:
R² = 0.73

Interpretation:
Model 2 explains more variation in house prices and performs better.

**Example 6 — Multiple Feature Regression**

Equation:
SalePrice = b0 + b1(GrLivArea) + b2(Neighborhood)
Meaning:
House price depends on:
- living area
- neighborhood

Both features together improve prediction accuracy.
