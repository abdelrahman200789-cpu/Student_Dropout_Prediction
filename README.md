# Student Dropout Prediction Project 🎓

An End-to-End Machine Learning project built with **Python** and **Scikit-Learn** to analyze academic & socioeconomic student data and predict student dropout risk to support early academic intervention.

---

## 📊 About the Dataset & Features
The dataset contains student academic performance, financial background, and personal indicators:

### Categorical & Binary Features
* **Gender:** Student gender (`Male` / `Female`).
* **Department:** Academic department (e.g., `CS`, `Engineering`, `Business`).
* **Semester:** Current academic level (`Year 1`, `Year 2`, etc.).
* **Parental_Education:** Education level of parents (`High School`, `Bachelor`, `Master`, `PhD`).
* **Binary Flags:** `Internet_Access`, `Part_Time_Job`, and `Scholarship` (`Yes` / `No`).

### Numerical Features
* **CGPA & Semester_GPA:** Cumulative and current semester academic performance (0.0 – 4.0 scale).
* **Attendance_Rate:** Percentage of overall class attendance (0% – 100%).
* **Stress_Index:** Self-reported stress level scale (1 – 10).
* **Demographics & Logistics:** `Age`, `Family_Income`, `Study_Hours_per_Day`, `Assignment_Delay_Days`, and `Travel_Time_Minutes`.

---

## 🛠️ Project Workflow
1. **Data Cleaning & Handling Missing Values:** Managed missing numerical and categorical records using median and mode imputation.
2. **Feature Engineering:** Created **`GPA_Change`** (`Semester_GPA` - `GPA`) to capture real-time academic trends and performance drop-offs.
3. **Data Preprocessing & Encoding Pipeline:**
   * Encoded binary features using **`OrdinalEncoder`**.
   * Encoded categorical features (`Department`, `Semester`, `Parental_Education`) using **`OneHotEncoder`**.
   * Scaled bounded numeric features using **`MinMaxScaler`** and continuous variance features using **`StandardScaler`**.
4. **Handling Class Imbalance:** Applied `class_weight='balanced'` to effectively handle class distribution (23.5% minority dropout class).
5. **Model Building & Evaluation:** Trained **Random Forest** and **KNN** classifiers, evaluating models using **Accuracy**, **Precision**, **Recall**, **F1-Score**, and **ROC-AUC Score**.

---

## 💻 Tech Stack & Tools
* **Language:** Python
* **Libraries:** Pandas, NumPy, Scikit-Learn, Matplotlib
* **Environment:** Jupyter Notebook / Visual Studio Code