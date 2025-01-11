# CustomerChrunClassification-ANN
This project aims to predict whether a customer is likely to churn (leave) based on their personal information and banking behavior using a trained machine learning model.

Features:
User Input Interface: A Streamlit web app where users can input customer data such as:
Geography (France, Germany, Spain)
Gender (Male/Female)
Age, Credit Score, Balance, Estimated Salary, etc.
Prediction: Based on the input data, the app predicts the likelihood of customer churn. If the churn probability is above 50%, the customer is considered likely to churn.
Files:
model.h5: Pre-trained Keras model for churn prediction.
label_encoder_gender.pkl: Pickle file for encoding the Gender feature.
scalar.pkl: Pickle file for scaling input data.
onehot_encoder_geo.pkl: Pickle file for one-hot encoding the Geography feature.
app.py: Streamlit application script to collect user input and predict churn probability.
Setup Instructions:
Clone the Repository:

bash
git clone https://github.com/your-username/customer-churn-prediction.git
Create and Activate Virtual Environment (Optional but Recommended):

bash
python -m venv venv
source venv/bin/activate  # On Windows, use `venv\Scripts\activate`
Install Required Libraries:


pip install -r requirements.txt
Run the Streamlit App:

arduino

streamlit run app.py
Access the Application: The app will open in your default web browser, where you can input data and see the churn prediction.

Requirements:
Python 3.6+
TensorFlow
Pandas
Streamlit
scikit-learn
How it Works:
Model & Preprocessing:
The app loads a pre-trained machine learning model (model.h5) and preprocessing components (scalers, label encoders, and one-hot encoders).
It uses these components to transform the input data into a format suitable for prediction.
Prediction:
The processed data is passed to the model to generate a churn probability, which is displayed to the user.
Result:
Based on the probability, the app will tell the user if the customer is likely to churn (if the probability is greater than 50%) or not.

Example:
Input:
Geography: France
Gender: Female
Age: 26
Credit Score: 800
Balance: 100000
Estimated Salary: 45000
Output:
Churn Probability: 0.23
The customer is not likely to churn.
