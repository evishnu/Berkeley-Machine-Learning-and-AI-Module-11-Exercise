# Used Car Price Analysis

This project analyzes a dataset of over 400,000 used car listings to identify which factors most influence the price of a used car. The insights help used car dealerships optimize pricing and inventory decisions.

## Objective
Help dealerships understand consumer behavior and vehicle features that drive higher resale value.

## Data Source
- Dataset: `vehicles.csv` (~426K records)
- Source: Kaggle 

## CRISP-DM Framework

### 1. Business Understanding
Uncover the most valuable car attributes for customers (year, brand, mileage, etc.) and how they affect price.

### 2. Data Understanding
Exploratory analysis revealed:
- Price skews right (most cars <$30K)
- Common brands: Ford, Toyota, Chevrolet
- Dominant fuel: Gasoline
- Most listings from 2005–2021

### 3. Data Preparation
- Dropped columns with >30% missing: VIN, size, etc.
- Removed outliers: price > $100K or < $100; odometer > 300K
- Imputed and encoded categorical variables
- Scaled numeric variables

### 4. Modeling
- Trained Linear Regression and Ridge Regression models
- Ridge used GridSearchCV for alpha tuning

### 5. Evaluation
- Models evaluated on RMSE and R Square
- Ridge slightly outperformed linear regression on test set

### 6. Deployment & Recommendations
- Focus on newer vehicles (<10 years old) with lower mileage
- Automatics and hybrids maintain better resale value
- Toyota, Honda, and Ford are strong brand performers

---

## File Structure
Berkeley-Machine-Learning-and-AI-Module-11-Exercise/
│
├── README.md
├── used_car_price_analysis.ipynb
├── data/
│   └── vehicles.csv
├── images/
    └── *.png (EDA plots)


## Next Steps
- Deploy as a pricing recommendation dashboard
