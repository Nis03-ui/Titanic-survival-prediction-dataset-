# Titanic Survival Prediction

**Machine Learning Project using Random Forest Classifier**

---

## 📖 Project Overview
The Titanic dataset contains information about passengers aboard the Titanic.  
The goal is to **predict whether a passenger survived** based on features like age, gender, class, and family size.

---

## 🧰 Features Used
- `Pclass` : Passenger class (1,2,3)  
- `Sex` : Encoded gender (0=female, 1=male)  
- `Age` : Standardized age  
- `Fare` : Standardized fare  
- `TotalFamily` : SibSp + Parch + 1  
- `AgeGroup` : Categorized age  
- `Title` : Extracted from Name (Mr, Miss, Mrs, etc.)  

---

## 🔍 Model
- **Algorithm:** Random Forest Classifier  
- **Hyperparameters:**
  - n_estimators = 400  
  - max_depth = 12  
  - min_samples_leaf = 2  
  - class_weight = 'balanced'  
  - random_state = 42  

- **Cross-validation:** 5-fold CV for stability

---

## 📊 Performance
| Metric | Score |
|--------|-------|
| Accuracy | 82–85% |
| Precision (Survived) | 0.83 |
| Recall (Survived) | 0.73–0.78 |
| F1-score (Survived) | 0.78 |

> Feature engineering (family size, age groups, and title extraction) significantly improved model performance.

---

## 📈 Feature Importance
![Feature Importance](feature_importance.png)

> Gender and passenger class are the most important features for predicting survival.

---

## ⚡ How to Run
```bash
# Clone the repo
git clone https://github.com/YourUsername/Titanic-ML.git

# Install dependencies
pip install -r requirements.txt

# Run the notebook
jupyter notebook Titanic_Project.ipynb
