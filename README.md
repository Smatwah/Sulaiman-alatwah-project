# Sulaiman-alatwah-project
🏙️ NYC Real Estate Dataset – Project Summary
This machine learning project aimed to build predictive models for identifying high-value real estate transactions across the five boroughs of New York City using public property sales data.

📊 1. Dataset Description
The dataset includes hundreds of thousands of real estate sales across NYC. Each row represents a single property sale record, with features such as:


Feature	Description
borough	Code for one of the five NYC boroughs (Manhattan, Brooklyn, etc.)
lot & block	Parcel-level geographic identifiers
year_built	Year the property was constructed
tax_class_at_time_of_sale	Property tax class during sale
building_class_category	General classification (residential, commercial, etc.)
land_square_feet & gross_square_feet	Lot size and total building area
sale_price	Final sale amount in USD
🧼 After cleaning:
Rows with invalid sale prices or missing data were removed.

Categorical features were encoded numerically.

A binary target was created:
high_value = 1 if sale price > median (~$510,000), else 0.

🤖 2. Model Training and Evaluation
We trained three supervised models for binary classification:

✅ Logistic Regression
A linear model good for baseline comparisons.

Accuracy: ~81%

F1-Score (High Value Class): ~82%

Shows acceptable performance but lacks non-linear learning capacity.

🌲 Random Forest Classifier
An ensemble of decision trees.

Accuracy: ~88%

F1-Score (High Value): ~89%

Great at capturing feature interactions and non-linear patterns.

⚡ XGBoost Classifier
Gradient boosting technique, optimized for structured data.

Accuracy: ~89%

F1-Score (High Value): ~90%

Offers the best generalization and performance, handling imbalances and complex patterns well.

Model | Accuracy | Precision (High) | Recall (High) | F1-Score (High)
Logistic Regression | ~81% | ~82% | ~80% | ~81%
Random Forest | ~88% | ~89% | ~87% | ~88%
XGBoost (GPU/CPU) | ~89% | ~90% | ~88% | ~89%


📈 3. Interpretation and Insights
Gross Square Feet and Land Square Feet were consistently strong predictors of property value.

Building Class Category also contributed significantly, likely due to differences between residential vs commercial value.

Models were particularly good at identifying high-value transactions (class 1), which is crucial for applications in:

Real estate investment

Risk assessment

Property tax forecasting

Urban planning & zoning analysis


