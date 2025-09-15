Housing Price Prediction – King County Dataset | hashtag#DataScienceJourney

On today’s episode of my hashtag#DataScience journey, I explored predicting the market price of a house based on its features. Using the King County housing dataset (including Seattle, May 2014 – May 2015), I analyzed attributes like square footage, number of bedrooms and bathrooms, number of floors, waterfront view, grade, and more to understand their impact on house prices.

Dataset Overview
Target variable: price

Key features: sqft_living, bedrooms, bathrooms, floors, waterfront, grade, view, sqft_above, sqft_basement, yr_built, yr_renovated, zipcode

Workflow
1. Data Loading & Cleaning
Imported libraries: pandas, numpy, matplotlib, seaborn, scikit-learn.
Dropped irrelevant columns and handled missing values in bedrooms and bathrooms using mean imputation.

2. Exploratory Data Analysis (EDA)
Visualized distributions and outliers using boxplots – houses with a waterfront view show higher prices and more outliers.
Explored relationships using regression plots; sqft_above is positively correlated with price.
Counted unique values for categorical features (e.g., floors) to understand the distribution.

3. Correlation Analysis
Highest correlation with price: sqft_living (0.70), grade (0.67), sqft_above (0.60), bathrooms (0.53), sqft_living15 (0.58).
Low correlation: zipcode, id

4. Modeling & Prediction
Linear Regression:
Single feature (sqft_living): R² ≈ 0.49
Multi-feature (11 features): R² ≈ 0.66
Polynomial Regression (degree 2): R² ≈ 0.75, capturing nonlinear relationships.
Ridge Regression with regularization: improved model stability, test R² ≈ 0.65–0.78.

Key Insights
Larger homes (sqft_living, sqft_above) and higher-grade houses significantly increase price.
Waterfront properties are premium and often exhibit price outliers.
Bathrooms, bedrooms, and view quality are strong predictors of price.
Polynomial and Ridge regression improve prediction by capturing nonlinear patterns while reducing overfitting.

Conclusion: Data cleaning, EDA, correlation analysis, and appropriate modeling can reveal the main factors influencing housing prices and help build predictive models that generalize well.
