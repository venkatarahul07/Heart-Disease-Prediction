# ❤️ Heart Disease Prediction Using Logistic Regression

<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=soft&color=0:0b132b,50:1c4e80,100:0077b6&height=200&section=header&text=HEART%20DISEASE%20PREDICTION&fontSize=40&fontColor=ffffff&animation=fadeIn&fontAlignY=42&desc=Machine%20Learning%20Using%20Logistic%20Regression&descAlignY=64&descSize=18" width="100%" alt="Heart Disease Prediction"/>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Python-3.x-3776AB?style=for-the-badge&logo=python&logoColor=white">
  <img src="https://img.shields.io/badge/Scikit--Learn-Logistic%20Regression-F7931E?style=for-the-badge&logo=scikit-learn&logoColor=white">
  <img src="https://img.shields.io/badge/Pandas-Data%20Analysis-150458?style=for-the-badge&logo=pandas&logoColor=white">
  <img src="https://img.shields.io/badge/Streamlit-Web%20App-FF4B4B?style=for-the-badge&logo=streamlit&logoColor=white">
</p>

<p align="center">
  <strong>Predict the likelihood of heart disease using clinical and demographic health information.</strong>
</p>

---

## 🫀 About The Project

**Heart Disease Prediction Using Logistic Regression** is a machine learning project that predicts whether a patient is likely to have heart disease based on health-related input features.

The project uses **Logistic Regression** for binary classification and a **Streamlit** web application for interactive predictions.

```text
0 → No Heart Disease
1 → Heart Disease
```

> ⚠️ This project is intended for educational and internship purposes and should not be used as a medical diagnosis system.

---

## 🎯 Problem Statement

The objective is to build a binary classification model that estimates the probability of a patient having or developing cardiovascular disease based on clinical and demographic risk factors.

The model uses features such as:

* Age
* Sex
* Chest Pain Type
* Resting Blood Pressure
* Cholesterol
* Fasting Blood Sugar
* Resting ECG
* Maximum Heart Rate
* Exercise-Induced Angina
* ST Depression
* Slope
* Major Vessels
* Thalassemia

---

## ⚙️ How It Works

```text
Patient Data
     ↓
Data Cleaning
     ↓
Feature / Target Separation
     ↓
Train-Test Split
     ↓
Logistic Regression
     ↓
Model Prediction
     ↓
Streamlit Application
     ↓
Heart Disease Result
```

---

## 📊 Dataset

The project uses a CSV dataset containing patient health information.

The target column is:

```text
target
```

```text
0 → No Heart Disease
1 → Heart Disease
```

### Features

| Feature  | Description                       |
| -------- | --------------------------------- |
| age      | Age of patient                    |
| sex      | Gender                            |
| cp       | Chest pain type                   |
| trestbps | Resting blood pressure            |
| chol     | Serum cholesterol                 |
| fbs      | Fasting blood sugar               |
| restecg  | Resting ECG result                |
| thalach  | Maximum heart rate                |
| exang    | Exercise-induced angina           |
| oldpeak  | ST depression                     |
| slope    | Slope of peak exercise ST segment |
| ca       | Number of major vessels           |
| thal     | Thalassemia type                  |
| target   | Heart disease result              |

---

## 🧹 Data Preprocessing

Duplicate records are checked and removed before training.

```python
df = df.drop_duplicates()
```

The input features and target are separated:

```python
x = df.drop(columns='target')
y = df['target']
```

The dataset is divided into training and testing sets:

```python
x_train, x_test, y_train, y_test = train_test_split(
    x, y, test_size=0.2, stratify=y, random_state=0
)
```

```text
80% → Training
20% → Testing
```

---

## 🤖 Machine Learning Model

The project uses **Logistic Regression** from Scikit-Learn.

```python
lr = LogisticRegression()
lr.fit(x_train, y_train)
```

Predictions are generated using:

```python
y_pred = lr.predict(x_test)
```

Logistic Regression is suitable because the target contains two classes:

```text
0 → No Disease
1 → Disease
```

---

## 📈 Model Performance

The original project reports approximately:

```text
91.2% Accuracy
```

For a stronger evaluation, the project can also use:

```text
Accuracy
Precision
Recall
F1-Score
Confusion Matrix
ROC-AUC
```

---

## 🖥️ Streamlit Application

The project includes an interactive Streamlit interface.

### Main Sections

```text
🏠 Home Page
❤️ Heart Disease Prediction
📩 Contact Me
```

Users can enter patient information through the web interface and click:

```text
Predict Disease
```

The trained model then returns the prediction.

---

## 🔄 Prediction Flow

```text
User Input
    ↓
Create DataFrame
    ↓
Trained Logistic Regression Model
    ↓
Prediction
    ↓
0 / 1
    ↓
Display Result
```

---

## 🛠️ Technologies Used

| Technology          | Purpose              |
| ------------------- | -------------------- |
| Python              | Programming          |
| Pandas              | Data Processing      |
| NumPy               | Numerical Operations |
| Scikit-Learn        | Machine Learning     |
| Logistic Regression | Classification Model |
| Streamlit           | Web Application      |
| Git & GitHub        | Version Control      |

---

## 📂 Project Structure

```text
Heart-Disease-Prediction/
│
├── model.py
├── heartdisease.csv
├── requirements.txt
├── README.md
└── .gitignore
```

---

## ⚙️ Installation

Clone the repository:

```bash
git clone https://github.com/venkatarahul07/Heart-Disease-Prediction.git
cd Heart-Disease-Prediction
```

Create a virtual environment:

```bash
python -m venv venv
```

Activate it on Windows:

```bash
venv\Scripts\activate
```

Install dependencies:

```bash
pip install -r requirements.txt
```

---

## ▶️ Run the Application

```bash
streamlit run model.py
```

The application will open in the browser at:

```text
http://localhost:8501
```

---

## ✅ Advantages

* Simple and easy-to-understand classification model
* Fast model training
* Suitable for binary classification
* Interactive Streamlit interface
* Easy to run and demonstrate
* Useful for learning the complete ML workflow

---

## ⚠️ Limitations

* Performance depends on the dataset.
* The model may not represent real-world medical conditions.
* Accuracy alone is not enough to evaluate a medical prediction system.
* The project is not clinically validated.
* It should not be used for medical diagnosis.

---

## 🚀 Future Scope

Future improvements can include:

* Feature scaling and feature selection
* Cross-validation
* Hyperparameter tuning
* Confusion matrix and ROC-AUC visualization
* Comparison with Random Forest, SVM, KNN and other models
* Probability-based predictions
* Improved Streamlit dashboard
* Model deployment
* Explainable AI techniques

---

## 🧪 Testing

The project can be tested using:

```text
✓ Different patient inputs
✓ Valid and invalid values
✓ Boundary values
✓ Model predictions
✓ Streamlit application
✓ Model evaluation metrics
```

---

## 🎓 Learning Outcomes

This project helps in understanding:

```text
Python
   ↓
Data Cleaning
   ↓
Data Preprocessing
   ↓
Supervised Learning
   ↓
Logistic Regression
   ↓
Model Evaluation
   ↓
Streamlit
   ↓
Machine Learning Application
```

---

## 👨‍💻 Author

### VenkataRahul, Varun Reddy

**CSE — Artificial Intelligence**

Machine Learning • Data Science • Python

---

## ⚠️ Disclaimer

This project is developed for **educational and internship purposes**.

The prediction generated by this application should not be considered a medical diagnosis or a substitute for professional medical advice.

---

## 📜 License

This project is intended for educational purposes.
