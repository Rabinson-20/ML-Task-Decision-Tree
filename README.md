# 🔍 Phishing URL Detection Using Decision Tree Classifier

## 📌 Project Overview

Phishing is a cyberattack in which attackers create fake websites or URLs to trick users into revealing sensitive information, such as passwords, banking details, and personal data.

This project uses Machine Learning and a **Decision Tree Classifier** to classify URLs based on features from the PhiUSIIL Phishing URL Dataset.

The project is implemented using Python and Jupyter Notebook. It includes data preprocessing, model training, decision tree visualization, and performance evaluation.

## 🎯 Objectives

- To analyze the phishing URL dataset.
- To preprocess and clean the dataset.
- To identify useful numerical features for classification.
- To train a Decision Tree Classifier.
- To visualize the trained decision tree.
- To evaluate the model using different performance metrics.

## 🛠️ Technologies Used

- Python
- Jupyter Notebook
- Pandas
- NumPy
- Matplotlib
- Scikit-learn
- Machine Learning

## 📂 Project Structure

```text
Phishing-URL-Detection/
│
├── README.md
├── decisiontree.ipynb
└── PhiUSIIL_Phishing_URL_Dataset.csv
```

## 📊 Dataset Description

This project uses the **PhiUSIIL Phishing URL Dataset**, which contains URL-related features for phishing classification.

The dataset is loaded using Pandas:

```python
df = pd.read_csv("PhiUSIIL_Phishing_URL_Dataset.csv")
```

The dataset is inspected to understand its structure, columns, missing values, and label distribution.

**Note:** Extract the dataset ZIP file before running the notebook. Keep the CSV file in the same directory as the notebook.

## ⚙️ Project Workflow

### 1. Data Loading

The dataset is loaded into a Pandas DataFrame for analysis.

### 2. Data Exploration

The notebook examines:
- Dataset dimensions
- First five records
- Column names
- Missing values
- Target label distribution

### 3. Data Preprocessing

The following preprocessing steps are performed:

- Remove records with missing target labels.
- Select numerical columns as input features.
- Exclude the target column from the input features.
- Replace infinite values with missing values.
- Fill missing feature values using the median.

### 4. Train-Test Split

The dataset is divided into training and testing sets.

- Training data: 80%
- Testing data: 20%
- Random state: 42
- Stratified splitting to preserve class proportions.

### 5. Model Training

A Decision Tree Classifier is trained using Scikit-learn.

```python
model = DecisionTreeClassifier(
    max_depth=5,
    class_weight="balanced",
    random_state=42
)
```

The model learns decision rules from the training dataset and uses them to classify unseen records.

### 6. Decision Tree Visualization

The trained decision tree is visualized using Matplotlib and Scikit-learn. This helps illustrate the features and decision rules used by the model.

### 7. Prediction

The trained model predicts the target classes for the test dataset.

The actual and predicted values are compared to understand the model's performance.

### 8. Model Evaluation

The model is evaluated using a confusion matrix and classification metrics.

## 📈 Evaluation Metrics

| Metric | Description |
|---|---|
| Accuracy | Measures the proportion of correct predictions. |
| Precision | Measures how many predicted positive cases are actually positive. |
| Recall | Measures how many actual positive cases are correctly identified. |
| F1-Score | Combines precision and recall into a single metric. |
| Specificity | Measures how many actual negative cases are correctly identified. |
| Confusion Matrix | Shows correct and incorrect predictions for each class. |

The actual metric values are generated when the notebook is executed.

**Important:** Verify the dataset's original label definitions before interpreting the results. The notebook maps original label `0` to class `1`, so the meaning of the positive class depends on the dataset's label definitions.

## 💻 Installation and Requirements

Install Python and Jupyter Notebook before running the project.

Install the required libraries using:

```bash
pip install pandas numpy matplotlib scikit-learn jupyter
```

## ▶️ How to Run the Project

1. Clone or download this repository.
2. Extract the dataset ZIP file.
3. Place the extracted CSV file in the project directory.
4. Open a terminal in the project directory.
5. Start Jupyter Notebook:

```bash
jupyter notebook
```

6. Open `decisiontree.ipynb`.
7. Run all notebook cells from top to bottom.
8. Review the model predictions, decision tree visualization, and evaluation metrics.

## 🌟 Key Features

- Machine-learning-based URL classification.
- Data cleaning and preprocessing.
- Numerical feature selection.
- Decision Tree model training.
- Decision tree visualization.
- Confusion matrix generation.
- Classification performance evaluation.

## 🚀 Future Enhancements

- Compare Decision Tree with Random Forest and other machine learning algorithms.
- Perform hyperparameter tuning.
- Add cross-validation.
- Analyze feature importance.
- Test the model on additional datasets.
- Develop a web interface for URL classification.
- Improve model evaluation and real-world testing.

## ⚠️ Limitations

- The model may incorrectly classify phishing or legitimate URLs.
- Performance depends on dataset quality and feature selection.
- Dataset labels must be verified before interpreting results.
- This project is an educational demonstration and is not a complete phishing protection system.

## 👨‍💻 Author

**Samrabinson P**
