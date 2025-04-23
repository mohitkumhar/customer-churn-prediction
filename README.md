# 📉 Customer Churn Prediction App

A simple and interactive web application built with **Streamlit** that predicts whether a customer is at risk of churning using a pre-trained **TensorFlow model**. This app is ideal for telecom or subscription-based services looking to identify and retain customers likely to leave.

---

## 🔍 Overview

This project helps businesses analyze customer data and predict churn based on various factors like service usage, contract type, tenure, and payment methods.

---

## 🧠 Model Architecture

The model is a fully connected deep neural network built with TensorFlow Keras, designed to minimize overfitting with regularization and dropout:

```python
Input: 45 features (encoded and numeric)

Dense(128, activation='relu', kernel_regularizer=L2)
→ BatchNormalization
→ Dropout(0.5)

Dense(64, activation='relu', kernel_regularizer=L2)
→ BatchNormalization
→ Dropout(0.5)

Dense(32, activation='relu')
→ BatchNormalization
→ Dropout(0.3)

Dense(1, activation='sigmoid')  # Output layer for binary classification
```

### Key Techniques Used:
- **L2 Regularization** to reduce overfitting
- **Batch Normalization** for faster and more stable training
- **Dropout** to prevent co-adaptation of neurons
- **Sigmoid Output** for binary churn classification (`Yes`/`No`)

---

## 🖥️ Demo

Try the app on your local machine:

![image](https://github.com/user-attachments/assets/e9e2d47f-c227-482e-adbe-c2ecd75ed369)


---

## 🚀 Getting Started

### 📦 Prerequisites

Make sure you have the following installed:

- Python 3.8+
- `streamlit`
- `tensorflow`
- `pandas`
- `scikit-learn`

Install dependencies using:

```bash
pip install -r requirements.txt
```

### ▶️ Run the App

```bash
streamlit run app.py
```

---

## 📁 Files Included

| File | Description |
|------|-------------|
| `app.py` | Main Streamlit app |
| `model.h5` | Trained TensorFlow model |
| `ohe.pkl` | OneHotEncoder for categorical features |
| `le.pkl` | LabelEncoder for output classes |

---

## 📝 Input Fields

- Gender, Senior Citizen, Partner, Dependents
- Tenure, Phone Service, Internet Service, etc.
- Monthly & Total Charges
- Contract and Payment Method

---

## 📊 Output

- **Prediction Label**: `Yes` or `No`
- **Churn Probability**: Displayed as percentage
- **Risk Message**: High or Low Risk

---

## ✨ Future Improvements

- Upload CSV to predict churn for multiple customers
- Visualize churn patterns with charts
- Deploy on Streamlit Cloud or Hugging Face Spaces

---

## 🤝 Contributing

Pull requests are welcome! For major changes, please open an issue first to discuss what you would like to change.

---

## 👨‍💻 Author

**Mohit Kumhar**  
🔗 [GitHub](https://github.com/mohitkumhar)
