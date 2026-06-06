# Student Placement Prediction System

## Project Overview

This project is an end-to-end Machine Learning solution developed to predict whether a student is likely to be placed based on academic and behavioral factors. The project follows the complete Machine Learning lifecycle, including data preprocessing, exploratory data analysis (EDA), model training, pipeline integration, and Streamlit deployment.

---

## Problem Statement

Educational institutions often need to identify students who are likely to secure placements. This project uses Machine Learning techniques to predict student placement status based on various performance indicators such as academic performance, attendance, and study habits.

---

## Dataset Features

The dataset contains the following features:

- Study Hours
- Attendance
- Sleep Hours
- Internet Usage
- Assignments Completed
- Previous Score
- Exam Score

### Target Variable

- Placement Status

---

## Project Workflow

### Phase 1: Data Science Workflow

- Problem Definition
- Data Collection & Ingestion
- Exploratory Data Analysis (EDA)
- Data Cleaning & Preprocessing
- Feature Engineering
- Model Training & Evaluation

### Models Evaluated

- Logistic Regression
- Decision Tree Classifier
- Random Forest Classifier

### Winning Model

**Random Forest Classifier**

The Random Forest model achieved the highest performance among all evaluated models and was selected as the final model for deployment.

---

## Phase 2: Pipeline Integration

To automate preprocessing and prediction, a Scikit-Learn Pipeline was created that combines:

- StandardScaler
- ColumnTransformer
- Random Forest Classifier

The complete workflow was integrated into a single pipeline to ensure consistency, prevent data leakage, and simplify deployment.

### Pipeline Export

```python
joblib.dump(pipeline, "student_placement_pipeline.pkl")
```

The exported pipeline file contains:

- Data preprocessing steps
- Feature scaling
- Trained Random Forest model

---

## Phase 3: Streamlit Deployment

A Streamlit web application was developed to provide real-time placement predictions.

### User Inputs

- Study Hours
- Attendance
- Sleep Hours
- Internet Usage
- Assignments Completed
- Previous Score
- Exam Score

### Prediction Flow

User Input → Streamlit Interface → Pipeline → Random Forest Model → Placement Prediction

The application accepts raw user inputs, automatically performs preprocessing through the saved pipeline, and instantly predicts the placement status.

---

## Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-Learn
- Joblib
- Streamlit

---

## Project Structure

```
student-placement-prediction/
│
├── Students_Classification.ipynb
├── app.py
├── student_placement_pipeline.pkl
├── dataset.csv
├── requirements.txt
└── README.md
```

---

## Installation

Clone the repository:

```bash
git clone https://github.com/yourusername/student-placement-prediction.git
```

Navigate to the project directory:

```bash
cd student-placement-prediction
```

Install dependencies:

```bash
pip install -r requirements.txt
```

---

## Run the Application

```bash
streamlit run app.py
```

---

## Results

- Successfully built and evaluated multiple classification models.
- Random Forest achieved the best predictive performance.
- Automated preprocessing using a Scikit-Learn Pipeline.
- Exported the complete pipeline using Joblib.
- Developed an interactive Streamlit application for real-time predictions.

---

## Future Enhancements

- Hyperparameter Optimization
- Feature Importance Analysis
- Cloud Deployment
- Integration with Educational Management Systems
- Enhanced User Interface Design

---

## Conclusion

This project successfully developed a Machine Learning-based Student Placement Prediction System to predict whether a student is likely to be placed based on academic and behavioral factors. The project began with data collection and exploratory data analysis (EDA) to understand the dataset, identify patterns, and evaluate relationships between features and the target variable.

Multiple machine learning algorithms, including Logistic Regression, Decision Tree, and Random Forest, were trained and evaluated. After comparison, Random Forest was selected as the final model due to its superior performance and strong predictive capability.

To ensure an industry-standard workflow, all preprocessing steps and the trained model were integrated into a single Scikit-Learn Pipeline. This automated pipeline minimizes manual intervention, prevents data leakage, and ensures consistent predictions on new data. The pipeline was then exported using Joblib for deployment purposes.

Finally, the model was deployed using Streamlit, allowing users to input student details and receive real-time placement predictions through an interactive web interface. This project demonstrates the complete Machine Learning lifecycle, from problem definition and model development to pipeline automation and deployment, providing a practical solution for predicting student placement outcomes.

---

## Author

**Shifana**

Machine Learning & Data Analytics Enthusiast
