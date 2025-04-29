# 🚢 Titanic Survival Prediction

## 📌 Objective
Build a machine learning classification model to predict whether a passenger survived the Titanic disaster based on features like age, gender, ticket class, fare, and more.

---

## 📊 Dataset Summary

- **Records**: 418 passengers
- **Target Variable**: `Survived` (0 = No, 1 = Yes)
- **Features**:
  - `Pclass`: Ticket class (1 = 1st, 2 = 2nd, 3 = 3rd)
  - `Sex`: Gender
  - `Age`: Age of passenger
  - `SibSp`: # of siblings/spouses aboard
  - `Parch`: # of parents/children aboard
  - `Fare`: Passenger fare
  - `Embarked`: Port of Embarkation (C = Cherbourg, Q = Queenstown, S = Southampton)

---

## ⚙️ Preprocessing Steps

- Dropped irrelevant features: `PassengerId`, `Name`, `Ticket`, `Cabin`
- Imputed missing values:
  - `Age` → median
  - `Fare` → median
- Encoded categorical variables:
  - `Sex`: Male/Female → 1/0
  - `Embarked`: Categorical ports → numerical codes
- Normalized numerical features using `StandardScaler`

---

## 🧠 Model Selection

- **Algorithm**: Random Forest Classifier (`sklearn.ensemble.RandomForestClassifier`)
- **Split**: 80% training, 20% testing
- **Performance Metrics**:
  - Accuracy
  - Precision
  - Recall
  - F1 Score
  - Confusion Matrix

---

## 🧪 Results

The model demonstrated strong performance across all evaluation metrics.

### Feature Importance

| Feature     | Importance Score |
|-------------|------------------|
| Sex         | High             |
| Fare        | Medium           |
| Age         | Medium           |
| Pclass      | Medium           |
| SibSp/Parch | Lower            |

Most important predictor: **Sex**

---

## 🚀 How to Run

### 1. Clone the Repository
```bash
git clone https://github.com/your-username/titanic-prediction.git
cd titanic-prediction
