# **Student Exam Performance Prediction System**

This project is an end-to-end machine learning application that predicts a student's math score based on various demographic and academic inputs. It provides a web-based interface for users to input details and receive predictions, making it accessible to a wide audience.

---

## **Table of Contents**
- [Overview](#overview)
- [Features](#features)
- [Technologies Used](#technologies-used)
- [Data Pipeline](#data-pipeline)
- [Model Training](#model-training)
- [Web Interface](#web-interface)
- [How to Run the Project](#how-to-run-the-project)
- [Project Structure](#project-structure)
- [Future Enhancements](#future-enhancements)
- [Contributors](#contributors)

---

## **Overview**
The **Student Exam Performance Prediction System** predicts a student's math score based on the following inputs:
- Gender
- Ethnicity
- Parental level of education
- Lunch type
- Test preparation course
- Reading score
- Writing score

The project integrates a machine learning model with a web application to provide a user-friendly prediction tool.

---

## **Features**
- Predicts a student's math score using a trained machine learning model.
- Provides a responsive and visually appealing web interface.
- Handles missing or incomplete input data gracefully.
- Modular design for easy updates to the pipeline or model.

---

## **Technologies Used**
- **Backend:**
  - Python
  - Flask (for web framework)
- **Frontend:**
  - HTML
  - CSS
- **Machine Learning:**
  - Scikit-learn
  - Pandas
  - Numpy
- **Other Tools:**
  - Joblib (for serialization)
  - Logging (for tracking processes)

---

## **Data Pipeline**
The data preprocessing pipeline includes:
1. **Imputation:** Handled missing values in numerical and categorical columns.
2. **Scaling:** Standardized numerical features for consistent model training.
3. **Encoding:** Converted categorical features into numerical format using One-Hot Encoding.
4. **Serialization:** Saved the preprocessing object (`preprocessor.pkl`) for consistent prediction preprocessing.

---

## **Model Training**
1. **Target Variable:** `Math Score`
2. **Input Features:**
   - Gender
   - Ethnicity
   - Parental level of education
   - Lunch type
   - Test preparation course
   - Reading score
   - Writing score
3. **Regression Model:** Trained using algorithms like `RandomForestRegressor` or similar.
4. **Evaluation Metrics:**
   - Mean Squared Error (MSE)
   - R-squared (R²)
5. **Artifacts Saved:**
   - Preprocessor: `preprocessor.pkl`
   - Model: `model.pkl`

---

## **Web Interface**
- A simple, responsive form for users to input their details.
- Dropdown menus for categorical data.
- Number input fields for reading and writing scores.
- Submit button to generate the predicted math score.
- Displays the result directly on the webpage.

---

## **How to Run the Project**

### Prerequisites:
1. Python 3.x installed on your system.
2. Required Python packages installed (`Flask`, `Scikit-learn`, etc.).

### **Project Structure**


```plaintext

student-performance-prediction/
│
├── app.py                     # Main Flask app
├── templates/
│   └── index.html              # Web interface HTML file
├── artifacts/
│   ├── model.pkl              # Trained machine learning model
│   └── preprocessor.pkl       # Preprocessing pipeline
├── src/
│   ├── utils.py               # Utility functions
│   ├── logger.py              # Logging setup
│   ├── Exception.py           # Custom exception handling
│   ├── components/
│   │   ├── data_ingestion.py  # Data ingestion logic
│   │   ├── data_transformation.py  # Data preprocessing
│   │   └── model_training.py  # Model training logic
│   └── Pipeline/
│       └── predict_pipeline.py # Prediction pipeline
├── requirements.txt           # Python dependencies
└── README.md                  # Project documentation

```




### **Future Enhancements**

- Add more features like parental income or attendance percentage.
- Incorporate more advanced machine learning algorithms like XGBoost or CatBoost.
- Deploy the application on a cloud platform (e.g., AWS, Heroku).
- Enhance the UI with additional styling and animations.

### **Contributors**
- Nilanjan Sarkar (You!): Full-stack development, machine learning pipeline, and deployment.
- Dexx (ChatGPT): Assisting in debugging, optimization, and documentation.
