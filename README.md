# House-Price-Prediction


# House Price Prediction 🏠

An end-to-end data science and machine learning project built for Week 1 of the Internship. This project analyzes real estate metrics and uses regression algorithms to predict house prices based on physical property features such as surface area, rooms, location, and air conditioning.

## 🎯 Problem Statement
Real estate buyers and sellers often rely on guesswork or outdated comparisons to estimate a property's fair value. This project aims to clean, explore, and build a predictive regression model using a real-world housing dataset to identify which features most strongly influence a home's price.

## 📦 Dataset
The dataset utilized is the **Housing Prices Dataset** sourced from Kaggle.
* **Source Link:** [Kaggle Housing Prices Dataset](https://www.kaggle.com/datasets/yasserh/housing-prices-dataset)
* **File Used:** `Housing.csv`
* **Features Include:** Area, Bedrooms, Bathrooms, Stories, Mainroad access, Guestrooms, Basement, Hot water heating, Air conditioning, Parking spaces, Preferred area status, and Furnishing status.

## 🛠️ Tools & Libraries Used
* **Python 3.x** - Main programming language
* **Jupyter Notebook** - Interactive development environment
* **Pandas & NumPy** - Data cleaning, preparation, and manipulation
* **Scikit-Learn** - Machine learning modeling and metric evaluations
* **Matplotlib & Seaborn** - Data visualization and plotting

## 📂 Project Structure
Your repository should look like this:
├── charts/
│   ├── chart1_price_distribution.png
│   ├── chart2_correlation_heatmap.png
│   └── chart3_actual_vs_predicted.png
├── Housing.csv
├── analysis.ipynb
├── summary.pdf (or summary.docx)
└── README.md


🚀 Tasks Completed
Task 1 — Data Loading & Exploration
Loaded the dataset into a Pandas DataFrame and inspected the structural dimensions (545 rows, 13 columns).

Displayed the first 10 observations to analyze feature distributions and identified price as the continuous target variable.

Verified that the dataset contains zero null/missing entries.

Task 2 — Data Cleaning
Ensured data integrity by checking and handling any missing or duplicated rows.

Handled structural variations and transformed text-based categorical variables (e.g., yes/no fields, furnishing types) into numerical variables using One-Hot Encoding (pd.get_dummies).

Task 3 — Model Building & Evaluation
Split the encoded data into an 80% training set and a 20% testing set. Evaluated two separate algorithms to compare baseline linear predictions against ensemble methods:

Metric	Linear Regression	Random Forest Regressor
MAE	$970,043.40	$1,005,529.21
RMSE	$1,324,506.96	$1,403,260.67
R² Score (Accuracy)	0.6529 (65.3%)	0.6104 (61.0%)
The Linear Regression model outperformed the Random Forest model on this specific testing set split, capturing roughly 65.3% of the variation in housing prices.

Task 4 — Visualizations (Saved in charts/)
Chart 1: Price Distribution Histogram - Captures the positive skewness of home pricing across the dataset.

Chart 2: Correlation Heatmap - Illustrates the statistical linear dependencies between features and house prices.

Chart 3: Actual vs. Predicted Scatter Plot - Maps the validation data targets against model outputs alongside a perfect-fit baseline to illustrate prediction accuracy.

📈 Key Insights & Recommendations
Top Drivers: Property surface area, bathroom count, and central air conditioning infrastructure demonstrate the strongest positive correlations with the final sale price.

Surprising Trait: Features like expanding the raw bedroom count or having a structural basement do not boost real estate evaluation margins nearly as much as adding fully-functional, finished bathrooms or central cooling units.

Business Recommendation: For real estate investment or house-flipping firms looking to maximize profit margins, priority capital should be directed toward modernizing bathroom layouts and installing central air units over expanding room spaces.

