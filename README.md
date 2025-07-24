# Personalized Healthcare Recommendation System

A machine learning project that analyzes blood donation data to provide personalized healthcare recommendations — built for research, awareness, and proactive healthcare support.

---

## 📌 Project Overview

The **Personalized Healthcare Recommendation System** uses historical blood donation data to predict whether a person is likely to donate again. Based on these predictions, it offers actionable suggestions such as encouraging donation or flagging the need for further engagement.

This project simulates a healthcare scenario where data-driven decisions can guide public health campaigns, improve blood donation drives, and enhance patient care through personalized insights.

---

## 📊 Dataset Description

The dataset consists of anonymized blood donation records. Each entry represents a donor and includes the following attributes:

| Feature     | Description                                                  |
|-------------|--------------------------------------------------------------|
| `Recency`   | Months since the last blood donation                         |
| `Frequency` | Total number of donations made by the individual             |
| `Monetary`  | Total blood donated in c.c. (calculated from frequency × 250)|
| `Time`      | Months since the first blood donation                        |
| `Class`     | Target variable — whether the person donated in March 2007 (`1` = yes, `0` = no) |

---

## ⚙️ Tech Stack

- **Python**
- **Pandas**, **NumPy** – Data handling
- **Matplotlib**, **Seaborn** – Visualization
- **Scikit-learn** – Preprocessing, modeling, and evaluation
- **Jupyter Notebook** – Interactive experimentation and development

---

## 🧠 Machine Learning Workflow

### 1. **Data Exploration & Visualization**
- Loaded the dataset using `pandas`
- Visualized distributions and class imbalance using `seaborn` and `matplotlib`
- Explored relationships between variables

### 2. **Data Preprocessing**
- Scaled features using `StandardScaler`
- Split the dataset into training and testing sets (80/20)

### 3. **Model Selection & Training**
- Chose `RandomForestClassifier` for balanced accuracy and robustness
- Trained on the preprocessed dataset

### 4. **Model Evaluation**
- Evaluated using:
  - Accuracy
  - Precision, Recall, F1-score
  - ROC-AUC score and ROC Curve
- Plotted Confusion Matrix and ROC Curve

### 5. **Personalized Recommendation System**
- Accepts user input for Recency, Frequency, Monetary, and Time
- Predicts donation likelihood
- Returns a human-readable recommendation message

---
## 🚀 How to Run the Notebook

1. **Clone or Download the Project Folder**
   - Make sure you have the project files including:
     - `blood.csv` (dataset)
     - `personalizedHealthCareRecommendationSystem.ipynb` (notebook file)

2. **Ensure the Dataset File is Named Exactly:**
```blood.csv```

3. **Open the Notebook File**
- Use **Jupyter Notebook**, **VS Code (with Python extension)**, or **Google Colab**
- Open:  
  ```
  personalizedHealthCareRecommendationSystem.ipynb
  ```
4. **Run All Cells**
- This will:
  - Load and explore the dataset
  - Train a machine learning model
  - Visualize insights and performance
  - Prompt you for real-time user input
  - Provide personalized healthcare recommendations based on prediction

---

## 🔍 Sample Prediction (User Input)

```python
# Sample input (high likelihood of donation)
Recency: 2
Frequency: 20
Monetary: 5000
Time: 60
