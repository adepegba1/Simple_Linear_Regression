# 📘 Student Exam Score Prediction using Linear Regression

## 1. 🎯 Introduction

This project, **"Student Linear Regression Model,"** marks the beginning of my journey into **Machine Learning**.
The goal of this project is to **predict students’ exam scores based on their study hours**, and to explore whether other factors, such as **attendance rate**, have any significant impact on performance.

This exercise builds foundational skills in:

* Data exploration and visualization,
* Correlation analysis,
* Building and evaluating regression models using **Scikit-learn**, and
* Interpreting model metrics and residuals.

---

## 2. 🧠 Methodology

### 🗂️ Dataset

The dataset used, `student_exam_scores_large.csv`, contains information about students, including:

* **Hours_Studied**
* **Attendance_Rate**
* **Exam_Score**

### 🧹 Data Preprocessing

* Checked for **duplicates** and **missing values** using `df.duplicated()` and `df.isnull()`.
* Verified dataset shape and column information using `df.info()` and `df.describe()`.

### 📊 Exploratory Data Analysis (EDA)

1. **Scatter plots** were created to visualize the relationship between:

   * Hours_Studied vs Exam_Score
   * Attendance_Rate vs Exam_Score
2. **Correlation analysis** was performed using `df.corr()` to confirm linear relationships.

### 📈 Model Building

* A **Linear Regression** model from `sklearn.linear_model` was used.
* Independent variable: `Hours_Studied`
* Dependent variable: `Exam_Score`

The model follows the simple regression equation:
[
y = mx + b
]
Where:

* *y* = predicted exam score
* *x* = hours studied
* *m* = slope (rate of change)
* *b* = intercept (exam score when hours studied = 0)

### ⚙️ Model Evaluation

* The model’s performance was measured using:

  * **R² (Coefficient of Determination)**
  * **MAE (Mean Absolute Error)**
  * **MSE (Mean Squared Error)**
  * **RMSE (Root Mean Squared Error)**

### 🧬 Model Validation

* The dataset was split using **train_test_split** (80% training, 20% testing).
* Residuals were analyzed visually using a **histogram** and **scatter plot** to check model bias and variance.

---

## 3. 🔍 Findings and Results

### 💡 Key Insights

| Relationship                  | Correlation                | Insight                                                    |
| ----------------------------- | -------------------------- | ---------------------------------------------------------- |
| Hours Studied vs Exam Score   | **0.81 (Strong Positive)** | As hours studied increase, exam scores rise predictably.   |
| Attendance Rate vs Exam Score | **0.22 (Weak Positive)**   | Attendance alone does not strongly determine exam success. |

### 📊 Model Performance (Full Data)

| Metric | Value  | Interpretation                           |
| ------ | ------ | ---------------------------------------- |
| R²     | 0.6636 | Model explains 66.36% of score variation |
| MAE    | 4.65   | Average prediction error: ±4.65 points   |
| RMSE   | 5.86   | Typical error in prediction ≈ 6 points   |

### 📈 Model Performance (Train/Test Split)

| Metric | Value |
| ------ | ----- |
| R²     | ~0.66 |
| MAE    | ~4.65 |
| RMSE   | ~5.90 |

The residuals had:

* **Mean ≈ 0.22** → Indicates an unbiased model.
* **Std ≈ 5.9** → Shows moderate prediction variance.

### 🖼️ Visualizations

1. **Scatter Plot:**
   Shows a clear linear upward trend between study hours and scores.
2. **Residual Histogram:**
   Residuals are roughly normally distributed around zero — a good sign.
3. **Residual vs Prediction Plot:**
   Most residuals cluster near the zero line → consistent prediction spread.

---

## 4. 🦯 Recommendations

1. **For Students:**
   Increasing study time significantly improves exam scores, but attendance alone doesn’t guarantee better results.

2. **For Educators:**
   Encourage **consistent study habits** and focus on **engagement strategies** that reinforce learning beyond attendance.

---

## 5. 🧼 Conclusion

This project demonstrates the foundational process of building a **predictive model using Linear Regression**:

* A clear linear relationship exists between **hours studied** and **exam performance**.
* The model can predict exam scores with moderate accuracy (R² ≈ 0.66).
* It highlights the importance of consistent studying as a key driver of academic success.

---

## 💎 Example Output

**Prediction Example:**

> A student who studies **10 hours** is expected to score **~74 marks**.

---

## 🧪 Tech Stack

* **Language:** Python
* **Libraries:** Pandas, NumPy, Matplotlib, Seaborn, Scikit-learn
* **IDE:** Jupyter Notebook
* **Algorithm:** Simple Linear Regression

---
