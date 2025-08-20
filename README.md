What Drives the Price of a Car?
Module-11 : Practical Application – 2
Executive Summary

This project applies the CRISP-DM framework (Cross-Industry Standard Process for Data Mining) to analyze a large used-car dataset and determine the key factors influencing car prices. The dataset, sourced from Kaggle, includes 426,000+ vehicle listings with attributes such as year, mileage, manufacturer, fuel type, condition, and more.

The ultimate objective is to provide actionable recommendations to car dealerships—helping them identify which vehicles hold value better, how depreciation relates to usage and age, and what inventory strategies maximize profitability.

Through data cleaning, exploratory analysis, and predictive modeling using regression methods, we discovered that age, mileage, brand, and fuel type are the strongest drivers of price. Advanced models such as Random Forest Regression outperform simpler models, capturing non-linear relationships and complex interactions.

1. Business Understanding
Objective

Assist used car dealerships in understanding the key features that drive car resale values, enabling them to:

Optimize acquisition decisions (which vehicles to stock).

Set competitive prices.

Improve marketing strategies based on consumer preferences.

Key Business Questions

Which features (mileage, brand, year, fuel type, transmission) are most correlated with price?

Which makes/models retain their value better over time?

How do age and mileage contribute to depreciation patterns?

What undervalued segments could dealerships strategically target?

2. Data Understanding
Dataset Description

The dataset consists of 426,880 car listings, each with 18 attributes, including:

price (target variable)

make, model, year

mileage (odometer)

fuel_type

transmission

location

engine_size, horsepower, doors, color, and more

Initial Observations

Missing or unrealistic values were found (e.g., price = 0, mileage > 500K).

Key gaps in attributes such as year, manufacturer, odometer, fuel, condition, and transmission.

Potential for data leakage (e.g., unusual values predicting price too directly).

Strong expected correlations: price vs. year, mileage vs. depreciation.

3. Data Preparation
Cleaning and Preprocessing

Removed rows with missing price, year, manufacturer, model, odometer.

Dropped sparse or sensitive columns such as VIN.

Standardized categorical values (grouped rare manufacturers into “Other”).

Applied one-hot encoding for categorical variables (e.g., fuel_type, transmission).

Normalized numerical variables where needed.

Result after cleaning:

Final entries: 364,359 cars

Columns reduced to 15 features

4. Modeling
Models Applied

Linear Regression

Ridge Regression (regularization for collinearity)

Random Forest Regression (non-linear interactions)

Evaluation Metrics

R² (coefficient of determination)

RMSE (Root Mean Squared Error)

Cross-validation for robustness

Feature Importance Analysis

The most influential predictors were identified to explain variance in pricing.

5. Model Validation

Key results:

Random Forest achieved the lowest RMSE, outperforming linear models.

Residual analysis revealed underperformance on luxury brands, where pricing is less predictable due to external factors (e.g., exclusivity, condition, rarity).

High-Impact Predictors

Brand (e.g., BMW, Lexus retain higher prices)

Mileage (inverse relationship with price)

Car Age (older cars depreciate faster)

Fuel Type (electric/hybrids command premium)

Moderate Impact

Transmission (automatics slightly more valued)

Number of Doors (minor but noticeable)

Geographic Location (AWD/SUVs more desirable in certain climates)

6. Deployment & Recommendations
Key Findings for Dealership Strategy

Stock newer, low-mileage cars: Value retention is highest before 100,000 miles and within the first 10 years.

Prioritize resilient brands: Toyota, Subaru, Honda, and Lexus maintain stronger resale value.

Leverage fuel efficiency: Electric and hybrid vehicles fetch premiums, especially in urban/eco-conscious markets.

Cater to regional needs: AWD/4WD in snowy areas, trucks in rural regions.

Focus on condition: Clean titles and well-maintained vehicles yield faster sales and higher margins.

Transmission preference: Automatics generally command higher resale across most brands.

Dataset Characteristics

Total entries (raw): 426,880

Final cleaned dataset: 364,359

Final features: 15 (including derived features such as car_age)

Visual Analysis
A. RMSE Comparison Across Models

B. Model Performance Comparisons






C. Heatmap – Top 20 Features

D. Histogram – Top 15 Features

E. Actual vs Predicted Prices

F. Predicted Prices vs Residuals

G. Random Forest Feature Analysis

H. 3D Scatter Plots – Manufacturing Year vs Odometer vs Predicted Price




Findings & Recommendations
For Dealerships:

Stock newer, lower-mileage vehicles with clean titles.

Focus on automatic transmission + fuel-efficient cars.

Adjust inventory based on regional demands (SUVs/AWD in snowy regions, trucks in rural areas).

Avoid vehicles with high mileage, poor condition, or salvage titles unless steeply discounted.

Incorporate predictive pricing models into dealership strategy for competitive advantage.

Evaluation

Metrics Used: R² and RMSE

Interpretation: Higher R² and lower RMSE indicate stronger predictive performance.

Outcome: Random Forest demonstrated superior performance in capturing non-linear pricing trends.

Conclusion

In summary:

Newer cars, fewer miles, automatic transmission, and clean condition are the most reliable value drivers.

Hybrid/electric cars are increasingly valuable, especially in urban contexts.

Dealerships can maximize profits by aligning stock with market demand and leveraging predictive models for dynamic pricing.

Next Steps

Market Adaptation: Continuously track market trends (e.g., EV adoption, regional shifts).

Model Expansion: Incorporate deep learning models for even greater predictive accuracy.

Deployment: Integrate models into dealership decision systems for automated valuation.

External Data Integration: Add macroeconomic factors (fuel prices, regional economy, consumer sentiment) for improved forecasting.