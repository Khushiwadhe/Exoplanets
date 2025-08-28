# Exoplanets

Exoplanet Confirmation Prediction
This project aims to build and evaluate machine learning models to predict the confirmation status of exoplanet candidates using data from the Kepler space telescope.

Project Overview
The project follows a typical data science workflow, including:

Data Loading and Merging: Loading and combining exoplanet candidate data with stellar data.
Data Cleaning and Preprocessing: Handling missing values, removing duplicates, and preparing the data for modeling.
Exploratory Data Analysis (EDA): Visualizing data distributions and relationships between features.
Feature Engineering: Creating new features to potentially improve model performance.
Model Training and Evaluation: Training and evaluating different classification models (Logistic Regression, Random Forest, XGBoost).
Feature Importance Analysis: Identifying key features influencing model predictions.
Habitable Zone Analysis: Identifying potentially habitable confirmed planets.
Prediction Function: Developing a function to predict the confirmation status of new exoplanet candidates.

Data
The project uses two datasets from the Kepler mission:

koi_table.csv: Contains information about Kepler Objects of Interest (KOIs), which are exoplanet candidates.
kepler_stellar.csv: Contains stellar data for the stars observed by Kepler.
These datasets were merged based on the Kepler ID (kepid).

Cleaning and Preprocessing
The data cleaning process involved:

Removing duplicate entries.
Dropping columns with a high percentage of missing values.
Imputing remaining missing values in numeric columns with the median and in categorical columns with the mode.
Relevant features were selected for modeling, and the target variable (koi_disposition) was encoded into a binary format (Confirmed vs. Not Confirmed). The features were then scaled using StandardScaler.

Exploratory Data Analysis
Initial data exploration included visualizing the distributions of planet radius and stellar temperature. A correlation heatmap was generated to understand the relationships between numeric features. Scatter plots were used to visualize the relationship between planet radius and stellar temperature, and stellar radius and planet radius, colored by the confirmation status.

Modeling
Three classification models were trained and evaluated:

Logistic Regression: A baseline model.
Random Forest: An ensemble method known for its robustness.
XGBoost: A gradient boosting model known for its high performance.

Evaluation
The models were evaluated using standard classification metrics:
Accuracy
Precision, Recall, F1-score (presented in a classification report)
Confusion Matrix
ROC Curve and AUC (Area Under the Curve)
The evaluation revealed that both Random Forest and XGBoost achieved very high accuracy on the test set, which may indicate potential overfitting.

Feature Importance
The feature importance from the Random Forest model was analyzed to understand which features contributed most to the prediction.

Potentially Habitable Planets
The project also identified potentially habitable confirmed planets based on their relative insolation compared to Earth.

Prediction Function
A Python function was created to allow for easy prediction of the confirmation status and probability for new exoplanet candidates based on their characteristics.

How to Use
To run this project:

Clone the GitHub repository.
Ensure you have the necessary Python libraries installed (pandas, scikit-learn, matplotlib, seaborn, xgboost).
Run the Jupyter Notebook or Python script provided.

Future Work
Potential areas for future improvement include:

Addressing potential overfitting through techniques like cross-validation, hyperparameter tuning, and regularization.
Exploring additional feature engineering possibilities.
Investigating other advanced machine learning models.

