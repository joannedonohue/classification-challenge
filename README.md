# 📧 Spam Detector Project

## 📌 Overview
This project focuses on developing a spam email detection system for an Internet Service Provider (ISP). The objective is to build and evaluate machine learning models to classify emails as either spam or not spam. By implementing both **Logistic Regression** and **Random Forest Classifier** models, we aim to improve the ISP's filtering system to protect customers from unwanted emails.

## 🗃️ Dataset
The dataset used in this project is sourced from the [UCI Machine Learning Library](https://archive.ics.uci.edu/dataset/94/spambase), and can be accessed at:
[Spam Data CSV](https://static.bc-edx.com/ai/ail-v-1-0/m13/challenge/spam-data.csv).

### Dataset Features
The dataset includes various features extracted from emails, such as word frequencies and specific character counts. It has been labeled with:
- **0** for non-spam emails
- **1** for spam emails

### Dataset Statistics
- Approximately **61%** of the emails are labeled as non-spam.
- The remaining **39%** are labeled as spam.

## 🛠️ Project Workflow
### 1. **Data Preprocessing**
- Loaded the dataset into a Pandas DataFrame and explored its structure.
- Split the data into features (`X`) and target labels (`y`).
- Scaled the feature data using `StandardScaler` to ensure all features are on the same scale.

### 2. **Model Development**
Two classification models were built and evaluated:
- **Logistic Regression**
- **Random Forest Classifier**

### 3. **Model Evaluation Metrics**
The models were evaluated using the following metrics:
- **Accuracy**
- **Precision**
- **Recall**
- **F1-Score**
- **Confusion Matrix**

## 🧪 Results & Findings
### **Logistic Regression Model**
- **Accuracy**: 93%
- **Precision**:
  - Not Spam (0): 92%
  - Spam (1): 94%
- **Recall**:
  - Not Spam (0): 96%
  - Spam (1): 87%
- **F1-Score**:
  - Not Spam (0): 94%
  - Spam (1): 90%

**Confusion Matrix**:

| 676  |  25  |
|------|------|
|  58  |  392 |


### **Random Forest Classifier**
- **Accuracy**: 97%
- **Precision**:
  - Not Spam (0): 96%
  - Spam (1): 97%
- **Recall**:
  - Not Spam (0): 98%
  - Spam (1): 94%
- **F1-Score**:
  - Not Spam (0): 97%
  - Spam (1): 95%

**Confusion Matrix**:

| 687  |  14  |
|------|------|
|  26  |  424 |


### 📝 Analysis
The **Random Forest Classifier** outperformed the Logistic Regression model in all key metrics:
- Higher accuracy (97% vs. 93%)
- Better precision and recall, especially for identifying spam emails.
- Lower false positives and false negatives, indicating more robust predictions.

## 🚀 Conclusion
- The Random Forest model's ability to handle non-linear relationships and capture complex patterns led to its superior performance over Logistic Regression.
- These results align with our initial prediction that the Random Forest model would be better suited for detecting spam due to its flexibility and robustness.

## ⚙️ Installation & Usage
### Prerequisites
Make sure you have the following Python packages installed:
```bash
pip install pandas scikit-learn
```

## Running the Project
1. Clone this repository:
```bash
   git clone https://github.com/joannedonohue/classification-challenge
```

2. Navigate to the project directory:
```bash
  cd spam_detector_Final
```

3. Run the Jupyter Notebook:
```bash
  jupyter notebook spam_detector_Final.ipynb
```

## Usage
The code reads the spam dataset, preprocesses it, and trains two classification models.
You can view the confusion matrices and classification reports to assess model performance.

🔍 Future Enhancements

Hyperparameter Tuning: Further fine-tuning of the Random Forest model using techniques like GridSearchCV.

Additional Models: Testing other algorithms such as Gradient Boosting, SVM, or Deep Learning models for potentially higher accuracy.

Feature Engineering: Extracting additional features such as email metadata (sender, subject line, etc.) could improve model performance.

Model Interpretability: Use tools like SHAP or LIME to interpret the predictions and understand which features contribute most to the classification.

🤝 Contributing
If you’d like to contribute to this project, please open an issue or submit a pull request.


👤 Author

Joanne Donohue

https://github.com/joannedonohue
