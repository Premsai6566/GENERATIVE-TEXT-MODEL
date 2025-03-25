# GENERATIVE-TEXT-MODEL
COMPANY: CODTECH IT SOLUTIONS

NAME: SITHARAM PREM SAI

INTERN ID: CODHC71

DURATION: 8 WEEKS

MENTOR: NEELA SANTHU

##Description:
 End-to-End Customer Churn Prediction API 
A complete machine learning project that predicts customer churn using a Random Forest model and serves predictions via a FastAPI REST API.
 Features
 Data Preprocessing: Handles missing values, encodes categorical variables, and scales numerical data.
 Model Training: Uses RandomForestClassifier for accurate churn prediction.
 Model Serialization: Saves the trained model with Pickle for reuse.
 FastAPI Endpoint: Serves predictions in real-time via a REST API.
 Docker-Ready: Easily deployable as a microservice.
 Project Structure
 customer-churn-prediction
│── data/                               # Dataset storage
│── model/                              # Trained model storage
│── churn_model.pkl                     # Serialized model file
│── app.py                               # FastAPI application
│── preprocess.py                        # Data preprocessing script
│── requirements.txt                     # Project dependencies
│── README.md                            # Documentation
 Installation & Setup
 Clone the Repository
git clone https://github.com/your-username/customer-churn-prediction.git
cd customer-churn-prediction
 Install Dependencies
pip install -r requirements.txt
 Run the API Server
uvicorn app:app --host 0.0.0.0 --port 8000 --reload
 Model Training
The model is trained using a Random Forest Classifier:
Data is preprocessed (feature encoding, scaling).
The trained model is saved as a pickle file (churn_model.pkl).
The model achieves an accuracy of ~{your_accuracy}%.
To retrain the model:
python app.py
 API Usage
 Predict Churn
Endpoint: /predict
Method: POST
Request Body:
json
{
  "features": [value1, value2, ..., valueN]
}
Response:
json
{
  "Churn Prediction": true/false,
  "Model Accuracy": 0.95
}
 Docker Support
To containerize and run the API using Docker:
docker build -t churn-api .
docker run -p 8000:8000 churn-api
