# ❤️ Heart Disease Prediction App

A machine learning web app that predicts the risk of heart disease based on a patient's clinical parameters, built with **scikit-learn** and deployed using **Streamlit**.

🔗 **Live Demo:** _[add your Streamlit Cloud link here after deployment]_

---

## 📌 Overview

This project uses the [Heart Failure Prediction Dataset](https://www.kaggle.com/datasets/fedesoriano/heart-failure-prediction) to train a classification model that predicts whether a person is at high or low risk of heart disease, based on 11 clinical features such as age, chest pain type, resting blood pressure, cholesterol, and more.

The workflow includes:
- Exploratory Data Analysis (EDA)
- Data cleaning & preprocessing (handling zero-value anomalies in `Cholesterol` and `RestingBP`)
- Feature encoding (one-hot encoding for categorical variables)
- Feature scaling (StandardScaler)
- Model comparison across Logistic Regression, KNN, Naive Bayes, Decision Tree, and SVC
- Final model: **K-Nearest Neighbors (KNN)**
- Deployment via an interactive **Streamlit** web app

---

## 🧠 Tech Stack

- **Python**
- **Pandas / NumPy** – data manipulation
- **Scikit-learn** – model training & preprocessing
- **Matplotlib / Seaborn** – EDA & visualization
- **Streamlit** – web app frontend
- **Joblib** – model serialization

---

## 📂 Project Structure

```
heart-disease-prediction/
│
├── app.py                       # Streamlit frontend app
├── heart_disease_prediction.ipynb  # Full EDA + model training notebook
├── KNN-heart.pkl                 # Trained KNN model
├── scaler.pkl                    # Fitted StandardScaler
├── columns.pkl                   # Expected feature columns (for encoding alignment)
├── requirements.txt              # Python dependencies
└── README.md
```

---

## ⚙️ How to Run Locally

1. Clone the repository
   ```bash
   git clone https://github.com/<your-username>/heart-disease-prediction.git
   cd heart-disease-prediction
   ```

2. Create a virtual environment (optional but recommended)
   ```bash
   python -m venv venv
   venv\Scripts\activate      # Windows
   source venv/bin/activate   # macOS/Linux
   ```

3. Install dependencies
   ```bash
   pip install -r requirements.txt
   ```

4. Run the app
   ```bash
   streamlit run app.py
   ```

5. Open the URL shown in the terminal (usually `http://localhost:8501`)

---

## 🖥️ How It Works

The user enters clinical details (age, sex, chest pain type, blood pressure, cholesterol, etc.) through the Streamlit UI. These inputs are:
1. Converted into the one-hot encoded format the model expects (aligned with `columns.pkl`)
2. Scaled using the saved `scaler.pkl`
3. Passed to the trained `KNN-heart.pkl` model for prediction

The app then displays whether the person is at **High Risk** or **Low Risk** of heart disease.

---

## 📊 Dataset

The dataset used is the [Heart Failure Prediction Dataset](https://www.kaggle.com/datasets/fedesoriano/heart-failure-prediction) (`heart.csv`), containing 918 patient records with 11 features and a binary target (`HeartDisease`).

> Note: `heart.csv` is not included in this repo. Download it from Kaggle if you want to re-run the notebook.

---

## ⚠️ Disclaimer

This project is for **educational purposes only** and is not intended for real medical diagnosis. Please consult a certified medical professional for health-related concerns.

---

## 🙋 Author

Made with ❤️ by **spiddyy**
