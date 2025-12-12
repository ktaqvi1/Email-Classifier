# 📧 Email Spam Classification

A Machine Learning project that classifies emails as **Spam (1)** or **Not Spam (0)** using multiple algorithms including **Naive Bayes**, **Support Vector Machine (SVM)**, and **Random Forest Classifier**. The dataset contains **5172 emails** represented by **word-frequency features** (3000+ columns).

---

## 📂 Project Structure

```
├── emails.csv
├── email_spam_classification.py
└── README.md
```

---

## 📌 Objective

To build and compare machine learning models that classify emails as spam or ham using numerical word-frequency features.

---

## 🧵 Dataset Description

* **5172 rows**
* **3002 columns**

  * 3000 columns: Word frequency counts
  * `Email No.`: Identifier
  * `Prediction`: Target variable (0 = Not Spam, 1 = Spam)

No missing values are present in the dataset.

---

## 🔧 Technologies Used

* Python
* NumPy
* Pandas
* Scikit-learn

---

## 🧠 Machine Learning Models Used

1. **Multinomial Naive Bayes**
2. **Support Vector Machine (SVC - RBF Kernel)**
3. **Random Forest Classifier (with GridSearchCV)**

---

## 🧪 Model Performance

### **1️⃣ Naive Bayes (MultinomialNB)**

```
Accuracy: 93.81%

Precision (Ham): 0.98
Recall (Ham): 0.93

Precision (Spam): 0.85
Recall (Spam): 0.95
```

---

### **2️⃣ Support Vector Classifier (RBF Kernel)**

```
Accuracy: 89.94%

Precision (Ham): 0.90
Recall (Ham): 0.96

Precision (Spam): 0.90
Recall (Spam): 0.74
```

---

### **3️⃣ Random Forest Classifier (Best Model)**

```
Accuracy: 97.52%

Precision (Ham): 0.99
Recall (Ham): 0.98

Precision (Spam): 0.95
Recall (Spam): 0.97
```

✔ **Random Forest performs the best** due to its ensemble nature—combining many decision trees results in higher stability and robustness.

---

## 📈 Why Random Forest Performed Best?

* Handles high-dimensional data well (3000+ features)
* Resistant to overfitting due to bagging
* Captures complex nonlinear relationships
* GridSearchCV optimizes hyperparameters for peak performance

---

## ▶️ How to Run

1. Install required libraries:

```bash
pip install numpy pandas scikit-learn
```

2. Run the script:

```bash
python email_spam_classification.py
```

3. Output will display accuracy and classification reports for all three models.

---

## 📚 Conclusion

This project compares three popular classifiers on a high-dimensional email dataset. The Random Forest model achieved the **highest accuracy (97.5%)**, making it the best choice for this classification task.
