**Project Overview**

This project is about building an AI-based Restaurant Recommendation System using a real-world Swiggy dataset containing over 1.4 lakh restaurants.
The system suggests similar restaurants or gives personalized recommendations based on:
>City
>Cuisine
>Rating
>Cost
The final system includes data cleaning, feature encoding, similarity calculation, and an interactive Streamlit app for easy user access.

**Tech Stack Used**
Component	Tool / Library
Language	Python 3.x
Libraries	pandas, numpy, scikit-learn, joblib, streamlit
IDE / Environment	VS Code / Google Colab
Data Storage	CSV Files
Version Control	GitHub

**Data Preprocessing Steps**
1️⃣ Cleaned Dataset – cleaned_data.csv

Removed duplicate rows.
Handled missing values for both categorical and numerical columns.
Standardized text columns like city and cuisine.
Capped outliers in cost and rating_count using the IQR method.
Saved the clean version as cleaned_data.csv.

2️⃣ Encoded Dataset – encoded_data.csv

Applied One-Hot Encoding for categorical columns like city and cuisine.
Used RobustScaler to scale numeric columns (rating, cost, rating_count).
Combined all columns into one complete numeric dataset.
Saved encoded features in both CSV and NPZ (sparse matrix) formats.

3️⃣ Encoder Bundle – encoder.pkl

A single file containing:
OneHotEncoder model
Scaler
LabelEncoder for restaurant names
Column metadata for reuse
This helps the Streamlit app use the same encoding for new user inputs.

**Recommendation System**
Method Used: Cosine Similarity

Measured how close or similar two restaurants are based on their features.

Two types of recommendations:

>Item-to-Item: Finds restaurants similar to a selected one.

>User-Preference: Suggests restaurants based on chosen city, cuisine, rating, and cost range.

Mapping Results

The recommended restaurant IDs are mapped back to cleaned_data.csv to show details like name, city, cuisine, rating, and cost.

**Streamlit Web Application**
App Features

Easy to use two-tab interface:

Search by Restaurant: Select one restaurant and get similar ones.

Search by Preference: Choose city, cuisine, and price range for suggestions.

Displays the output neatly in a table with:

Name, City, Cuisine, Rating, Cost, and Similarity Score.

Uses encoder.pkl, cleaned_data.csv, and X.npz for backend processing.

File	Description
cleaned_data.csv	Final cleaned dataset
encoded_data.csv	Encoded numerical dataset
encoder.pkl	Encoders and scalers
X.npz	Sparse matrix for similarity
app.py	Streamlit application

**Results and Insights**
Evaluation Area	Result
Recommendation Quality	Accurate and diverse suggestions for different cuisines
App Usability	Smooth, interactive, and user-friendly
Data Consistency	Verified index alignment between cleaned and encoded files

**Insights**

Different cities have unique cuisine preferences.

The cost column was highly skewed and corrected using IQR.

The recommendation model helps users explore relevant restaurants faster.

**Project Evaluation Metrics**
Metric	Description
Recommendation Quality	Checked relevance and diversity of suggestions
User Experience	Tested smooth functioning of Streamlit app
Data Alignment	Ensured no mismatch between datasets

**Project Workflow**
Data Understanding

Missing Value Handling

Outlier Detection (IQR Method)

Encoding & Feature Scaling

Cosine Similarity Recommendation

**Streamlit Deployment**

Business Use Cases

Personalized Food Discovery: Suggests restaurants that match user taste.

Improved Customer Experience: Reduces effort to search for restaurants.

Marketing Insights: Helps identify trending cuisines and cities.

Restaurant Strategy: Supports price and cuisine-based optimization.

**Conclusion**
This project shows the complete process of building a recommendation engine — from cleaning raw data to deploying a web app.
It helps users find the right restaurant faster while giving businesses insights about user preferences and market trends.

**Deliverables**

✅ Cleaned Dataset – cleaned_data.csv
✅ Encoded Dataset – encoded_data.csv / X.npz
✅ Encoder Bundle – encoder.pkl
✅ Streamlit Application – app.py
✅ Project Report / README
✅ PowerPoint Presentation
