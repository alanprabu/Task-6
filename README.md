# Phishing URL Detection Using Decision Tree Classifier

## 📌 Project Overview

This project focuses on detecting phishing URLs using Machine Learning. A Decision Tree Classifier is trained to classify URLs as **Phishing** or **Legitimate** based on URL characteristics and website-related features.

The project uses the **PhiUSIIL Phishing URL Dataset** and evaluates the model using Accuracy, Precision, Recall, F1-score, and Specificity.

## 🎯 Objectives

- Detect phishing URLs using Machine Learning.
- Analyze URL and website features to identify suspicious websites.
- Train a Decision Tree Classification model.
- Evaluate model performance using classification metrics.
- Visualize the decision tree and confusion matrix.

## 📂 Dataset Information

**Dataset:** PhiUSIIL Phishing URL Dataset

- Total Records: 78,962
- Total Columns: 56
- Numerical Features Selected: 50
- Target Column: `label`
- Missing Values: 45

The dataset contains URL information, domain characteristics, security indicators, and website content features.

### Target Labels

**Original Labels:**
- `0` — Phishing
- `1` — Legitimate

**Labels After Preprocessing:**
- `0` — Legitimate
- `1` — Phishing

## 🛠️ Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Scikit-learn
- Google Colab / Jupyter Notebook

## ⚙️ Project Workflow

### 1. Data Loading

Load the dataset using Pandas and examine its structure, first five rows, column names, missing values, and target distribution.

### 2. Data Preprocessing

- Remove rows with missing target labels.
- Convert target labels into the required binary format.
- Select numerical features for model training.
- Replace infinite values with missing values.
- Fill missing feature values using column medians.

### 3. Train-Test Split

Split the dataset into training and testing sets.

- Training Data: 80%
- Testing Data: 20%
- Random State: 42
- Stratified Sampling: Used to maintain the target class distribution.

### 4. Model Training

Train a Decision Tree Classifier using the following parameters:

- `max_depth=5`
- `class_weight="balanced"`
- `random_state=42`

The trained model learns patterns in URL and website features to classify phishing and legitimate websites.

### 5. Model Prediction

Use the trained model to predict labels for the test dataset and compare the predicted labels with the actual labels.

### 6. Model Evaluation

Evaluate the model using the following metrics:

- Accuracy
- Precision
- Recall
- F1-score
- Specificity

### 7. Data Visualization

Generate the following visualizations:

- Decision Tree Plot
- Confusion Matrix

These visualizations help explain the model's decision-making process and classification results.

## 📊 Model Evaluation Results

The initial evaluation produced the following results:

| Metric | Score |
|---|---:|
| Accuracy | 1.0000 (100%) |
| Precision | 1.0000 (100%) |
| Recall | 1.0000 (100%) |
| F1-score | 1.0000 (100%) |
| Specificity | 1.0000 (100%) |

### Confusion Matrix

| Actual Class | Predicted Legitimate | Predicted Phishing |
|---|---:|---:|
| Legitimate | 9,184 | 0 |
| Phishing | 0 | 6,609 |

**Note:** These are the results produced by the current experiment. Perfect scores are unusual for real-world phishing detection. Further validation is required to rule out data leakage, duplicate records, or other dataset-related issues before claiming 100% generalization accuracy.

## 📈 Key Findings

- The Decision Tree Classifier was successfully trained using the selected numerical features.
- The model classified all test records correctly in the initial evaluation.
- The confusion matrix showed zero false positives and zero false negatives.
- Additional validation is necessary to confirm performance on previously unseen URLs.

## 🚀 How to Run the Project

1. Download or clone the project repository.
2. Open the notebook in Google Colab or Jupyter Notebook.
3. Upload the PhiUSIIL Phishing URL Dataset CSV file.
4. Update the dataset file path if necessary.
5. Run all notebook cells in sequence.
6. Review the model evaluation metrics and visualizations.

### Required Libraries

Install the required libraries using the following command:

```bash
pip install pandas numpy matplotlib scikit-learn
```

## 🔮 Future Enhancements

- Evaluate the model using cross-validation.
- Check for duplicate URLs and possible data leakage.
- Test the model on an independent dataset.
- Compare Decision Tree performance with Random Forest and other classifiers.
- Develop a simple web application for URL classification.
- Improve model reliability on previously unseen phishing URLs.

## 🏁 Conclusion

This project demonstrates how Machine Learning can be used to classify phishing and legitimate URLs using website and URL characteristics. The Decision Tree Classifier provides an interpretable approach to phishing detection, while evaluation metrics and visualizations help assess its performance.

Further independent testing is essential before using the model in a real-world security application.
