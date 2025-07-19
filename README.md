# 🧠 Support Vector Regression (SVR) on Tips Dataset

This project demonstrates how to use **Support Vector Regression (SVR)** to predict restaurant **total bills** using the well-known **Tips dataset**. It includes preprocessing (label + one-hot encoding), model training, evaluation, and hyperparameter tuning using GridSearchCV.

---

## 📚 Dataset Overview

The Tips dataset from Seaborn includes information about meals in a restaurant and the corresponding tips. It contains both numerical and categorical variables.

**Features:**

- `total_bill`: Total cost of the meal (target)
- `tip`: Tip amount
- `sex`: Gender of the customer (`Male`/`Female`)
- `smoker`: Whether the customer smokes (`Yes`/`No`)
- `day`: Day of the week
- `time`: Time of day (`Lunch`/`Dinner`)
- `size`: Number of people in the party

---
## 🧪 Libraries Used
- pandas
- numpy
- seaborn
- scikit-learn (SVR, GridSearchCV, LabelEncoder, OneHotEncoder, ColumnTransformer)
- matplotlib or seaborn (for optional visualizations)

## 🧼 Data Preprocessing

### 🔄 Feature Encoding

- **Label Encoding**: Applied to binary categorical features (`sex`, `smoker`, `time`)
- **One-Hot Encoding**: Applied to `day` using `ColumnTransformer` with `drop='first'` to avoid multicollinearity

### 📊 Feature and Target Separation

- `X = ['tip', 'sex', 'smoker', 'day', 'time', 'size']`
- `y = total_bill`

### ✂️ Train-Test Split

- Performed **before** encoding to avoid data leakage
- `test_size=0.2`, `random_state=42`

---

## 🤖 Model: Support Vector Regression (SVR)

### ✅ Training

- Model: `SVR()`
- Fitted on encoded training data
- Evaluated on test set

### 📈 Metrics

Initial SVR Results:
- **R-squared Score:** `0.5502`
- **Mean Absolute Error (MAE):** `4.41`

---

## 🔍 Hyperparameter Tuning

Using **GridSearchCV**


## ✅ Conclusion
This project showcases the application of SVR on real-world-like data, along with:
- Proper feature engineering (label + one-hot encoding)
- Avoiding data leakage
- Hyperparameter tuning for optimization
While performance could still be improved with more complex models or feature engineering, this provides a strong foundation for regression modeling with scikit-learn.

## 📎 Author
Mai3Prabhu
