# used_mobile_price_prediction
A complete Machine Learning project that predicts the resale price of used smartphones based on specifications such as brand, model, RAM, storage, condition, battery health, age, and original price. The project uses RandomForestRegressor for prediction and provides a Streamlit-based Web UI for user interaction.
________________________________________
🚀 Project Overview
Many people want to sell or buy used phones but don’t know the right resale value.
This project solves that problem by training a machine learning model on a dataset of used phones and predicting the fair resale price.
The workflow includes:
1.	Data Cleaning & Preprocessing
2.	Label Encoding of categorical columns
3.	Feature selection (X, y)
4.	Train-Test Split
5.	Training RandomForestRegressor model
6.	Evaluating the model using R² Score
7.	Saving the model using pickle
8.	Creating a Streamlit interface for real-time prediction
________________________________________
🧠 Technologies & Tools Used
1. Python
2. Pandas Data handling & preprocessing
3. scikit-learn for ML model training, Label Encoding
4. RandomForestRegressor
5. pickle for saving & loading ML model
6. Streamlit for Web App
________________________________________
📊 Dataset Description
The dataset used_phone.csv contains columns such as:
1. brand
2. model
3. ram_gb
4. storage_gb
5. condition
6. battery_health
7. age_years
8. original_price
9. resale_price
________________________________________
🛠 How The Model Works (Step-By-Step)
1. Load Dataset
   - df = pd.read_csv("used_phone.csv")
2. Data Cleaning
   •	Check missing values
   •	Remove duplicates
3. Label Encoding
   Categorical columns (brand, model, condition) are converted into numeric values using:     LabelEncoder()
4. Prepare Features (X) and Target (y)
   x = df.drop(columns='resale_price')
   y = df['resale_price']
5. Split Dataset
   train_test_split(x, y, test_size=0.2, random_state=42)
6. Train RandomForestRegressor
   model = RandomForestRegressor(n_estimators=100)
   model.fit(x_train, y_train)
7. Evalute Performance
   Using R² Score:
   r2_score(y_pred, y_test)
8. Save Model Using Pickle
   pickle.dump(model, open("used_phone.pkl", "wb"))
________________________________________
⭐ Conclusion
This project demonstrates how machine learning + Streamlit can predict used mobile phone prices efficiently.
It includes a full pipeline: dataset → preprocessing → training → saving → deployment UI.
