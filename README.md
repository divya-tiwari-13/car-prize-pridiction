# car-prize-pridiction
MyCars Used Car Price Prediction Model
Project Overview
This project develops a machine learning model to predict used car prices for MyCars, leveraging India's rapidly growing used car market (expected to reach 8.3 million units by FY26[Query]). The model aims to optimize pricing strategies using key market drivers like digitalization, financing options, and pandemic-induced demand shifts.

Key Features Influencing Price
The top factors determining used car prices are:

Feature	Impact Description
Age	Older cars depreciate faster, especially post-5 years.
Mileage	Higher mileage reduces value due to wear and tear.
Manufacturer/Brand	Popular brands (e.g., Maruti, Hyundai) retain value better.
Max Power (bhp)	Higher engine power increases resale price.
Region	Location affects demand and supply dynamics.
Additional factors include service history, damage history, and transmission type.

Best-Performing Model
Random Forest Regression achieved the highest accuracy:

93% testing accuracy

13.7% mean annual depreciation error, outperforming linear models.

Handles non-linear relationships between features and price effectively.

Usage
Install dependencies:

bash
pip install pandas scikit-learn numpy  
Train the model:

python
from sklearn.ensemble import RandomForestRegressor  
model = RandomForestRegressor(n_estimators=200, random_state=42)  
model.fit(X_train, y_train)  
Predict prices:

python
predictions = model.predict(X_test)  
Project Structure
text
mycars/  
├── data/                 # Preprocessed datasets  
├── models/              # Saved model weights  
├── notebooks/           # EDA and training scripts  
└── requirements.txt  
Next Steps
Explore fine-tuning with LightGBM or CatBoost for marginal accuracy gains, or integrate regional demand trends for hyperlocal pricing.
