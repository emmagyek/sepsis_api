### Sepsis Prediction API Project
This project develops a Machine Learning (ML) API that predicts the risk of sepsis for ICU patients. The API is designed for scalability and high performance, utilizing Docker for containerization and seamless deployment.
 
### Table of Contents
Introduction
Features
Dataset Overview
Attribute Descriptions
Hypothesis
Sepsis Target
Business Questions
Technologies Used
Setup Instructions
Machine Learning Models
Installation Requirements
API Endpoints
Troubleshooting
Authorship
Donor Acknowledgement
License
 
 
License
 
### Introduction
Sepsis is a life-threatening condition caused by the body's response to infection damaging its tissues and organs. Early sepsis prediction is essential for timely intervention and better patient outcomes. This project offers a reliable Machine Learning-based API that predicts sepsis risk using patient medical data.
 
### Features
- Predict sepsis risk using patient medical records.  
- Scalable, containerized application with Docker.  
- RESTful API endpoints for seamless integration with healthcare systems or applications.  
- Accurate predictions driven by pre-trained machine learning models.
 
### Dataset Overview
The dataset for this project includes medical records of ICU patients. The main objective is to predict the *Sepsis* target variable, indicating a patient's likelihood of developing sepsis. 
 
 
### Column Name Attribute/Target    Description
ID  N/A Unique number to represent patient ID
PRG Attribute 1 Plasma glucose
PL  Attribute 2 Blood Work Result-1 (mu U/ml)
PR  Attribute 3 Blood Pressure (mm Hg)
SK  Attribute 4 Blood Work Result-2 (mm)
TS  Attribute 5 Blood Work Result-3 (mu U/ml)
M11 Attribute 6 Body Mass Index (BMI): weight in kg/(height in m)^2
BD2 Attribute 7 Blood Work Result-4 (mu U/ml)
Age Attribute 8 Patient's age (years)
Insurance   N/A Indicates if a patient holds a valid insurance card
 
### Sepssis Target:
Patient in ICU will develop sepsis; Negative: Otherwise
 
### Technologies Used:
- **FastAPI**: Used for developing the RESTful API.  
- **Scikit-learn**: Utilized for creating the machine learning model.  
- **Python**: The primary programming language for the model and API.  
- **NumPy and Pandas**: Employed for data processing and analysis.  
- **Docker**: Facilitates containerization and deployment.  
 
### Setup
### Sepsis Prediction API  
This FastAPI-based Sepsis Prediction API enables users to upload a CSV file to predict sepsis risk using a selected machine learning model. The results, including the original data and predictions, are returned in JSON format. 

### Machine Learning Models
**Multiple Models**: Select from various pre-trained models for making predictions.

"DecisionTree"
"RandomForest"
"LogisticRegression"
"KNN"
CSV File Upload: Upload a CSV file with the necessary features for prediction.
 
Prediction Output: Get a JSON response containing the original data along with the predictions for each row in a new column labeled Prediction.
 
### Installation Requirements
Python 3.7 or higher
FastAPI
Uvicorn
Pandas
Scikit-learn
 
Step 1: Clone the repository
bash
Copy code
git clone <repository-url>
cd <repository-directory>
 
Step 2: Install dependencies
Create a virtual environment and install the required dependencies using pip:
 
### bash
Copy code
python -m venv venv
source venv/bin/activate  # On Windows, use `venv\Scripts\activate`
pip install -r requirements.txt

Step 3: Run the FastAPI server
To start the FastAPI application, run the following command:
 
### bash
Copy code
uvicorn.run("src.mlapi:app", reload=True)
This will start the FastAPI app locally at http://127.0.0.1:8000.
Copy URL and paste it in a new browser and add /docs eg. http://127.0.0.1:8000/docs to  access the API.
 
### API Usage
Endpoint: /predict
Method: POST
This endpoint allows you to make predictions using a specified model.
 
Type in the name of the model you want to use for prediction.
![Screenshot 2024-12-11 170201](https://github.com/user-attachments/assets/de7f4c9a-db50-4c1e-871e-01e1988eda19)

model (str) – The name of the model you wish to use for prediction. Available models:
"DecisionTree"
"RandomForest"
"LogisticRegression"
"KNN"
 
Upload File:
Navigate to the "Upload File" section and select a CSV file.
![Screenshot 2024-12-11 170201m](https://github.com/user-attachments/assets/0704853a-8ec7-41f0-b0a1-edbe2c5ca569)

 
file (file) – A CSV file with the necessary features for prediction. The file should contain the following columns:
"PRG", "PL", "PR", "SK", "TS", "M11", "BD2", "Age", "Insurance"
 
### Response:
A JSON response containing the predictions for each row in a new column labeled "Prediction".
 
![Screenshot 2024-12-11 170210](https://github.com/user-attachments/assets/90aed621-06fd-40e4-b4c8-d5a2a73dbe70)
 
 
### Troubleshooting
1. **Incorrect Number of Features**  
If the number of features in the uploaded CSV file does not match the model's expected input, the API will return an error. Please ensure the file has the correct number of columns.

2. **Model Not Found**  
If an invalid model is selected, the API will return a 400 error indicating that the model could not be found.

3. **Invalid File Format**  
If the uploaded file is not in CSV format, the API will return a 400 error.
 
 
 
### About the Author
This FastAPI application was developed by Emmanuel Agyekum, a passionate data analyst and machine learning enthusiast with expertise in data analysis and artificial intelligence. Emmanuel is dedicated to using machine learning models to provide actionable insights and accurate predictions.

In this project, Emmanuel integrated a machine learning model to predict medical conditions, creating a user-friendly API that enables seamless data uploads and predictions. The main objective is to simplify the interaction between complex machine learning models and end-users, making advanced technologies more accessible and practical.

Emmanuel is committed to developing scalable, efficient, and impactful machine learning solutions applicable across various industries, including healthcare and business analytics. 

 
### Donor of database:
                          The Johns Hopkins University
                          Johns Hopkins Road
                          Laurel, MD 20707
                          (301) 953-6231
 
 
 
### License
This project is licensed under the MIT License. See the LICENSE file for details.
 
has context menu
