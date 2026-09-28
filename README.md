


# Customer Churn Prediction Using Neural Network

## 📌 Project Overview

This project predicts whether a bank customer is likely to leave the bank using Machine Learning and a Neural Network.

The project uses customer demographic and banking-related information to perform binary classification, where:

* `0` = Customer did not exit
* `1` = Customer exited

## 🎯 Objective

The main objective of this project is to build a Neural Network model that can predict customer churn based on available customer attributes.

## 📂 Dataset

The project uses the `Churn_modelling.csv` dataset.

The dataset contains customer-related information such as:

* Credit Score
* Geography
* Gender
* Age
* Tenure
* Balance
* Number of Products
* Has Credit Card
* Is Active Member
* Estimated Salary

The target variable is:

* `Exited`

## 🛠️ Technologies Used

* Python
* Pandas
* NumPy
* Scikit-learn
* TensorFlow
* Keras
* Jupyter Notebook

## 🔄 Project Workflow

### 1. Data Loading

The dataset is loaded using Pandas.

```python
df = pd.read_csv("Churn_modelling.csv")
```

### 2. Data Preprocessing

Unnecessary columns such as:

* RowNumber
* CustomerId
* Surname

are removed.

Categorical columns such as `Geography` and `Gender` are converted into numerical values using one-hot encoding.

### 3. Feature and Target Separation

The input features are separated from the target variable:

```python
X = df.drop(columns=["Exited"])
y = df["Exited"]
```

### 4. Train-Test Split

The dataset is divided into training and testing sets using `train_test_split`.

### 5. Feature Scaling

`StandardScaler` is used to scale the numerical input features.

### 6. Neural Network

A Neural Network is developed using TensorFlow/Keras.

The model contains:

* Input layer
* Hidden layers
* Output layer

The output layer uses the sigmoid activation function because this is a binary classification problem.

### 7. Model Compilation

The model uses:

* Optimizer: Adam
* Loss Function: Binary Crossentropy
* Evaluation Metric: Accuracy

### 8. Model Training

The model is trained using the training dataset for multiple epochs.

### 9. Prediction

The trained model predicts whether a customer is likely to exit.

### 10. Evaluation

The model performance is evaluated using accuracy.

## 📊 Model Architecture

The Neural Network consists of:

* Input layer with 11 features
* Hidden layer with 11 neurons
* Hidden layer with 11 neurons
* Output layer with 1 neuron
* Sigmoid activation for binary classification

## 📁 Project Structure

```text
Customer-Churn-Prediction-Neural-Network/
│
├── NN.ipynb
├── Churn_modelling.csv
├── README.md
├── requirements.txt
└── .gitignore
```

## 🚀 How to Run the Project

### 1. Clone the repository

```bash
git clone YOUR_GITHUB_REPOSITORY_LINK
```

### 2. Install the required libraries

```bash
pip install -r requirements.txt
```

### 3. Open the notebook

```bash
jupyter notebook NN.ipynb
```

### 4. Run all cells

Run the notebook cells from top to bottom to train the Neural Network and evaluate the model.

## 📌 Key Learning Outcomes

Through this project, I practiced:

* Data preprocessing
* Exploratory data inspection
* Categorical encoding
* Train-test splitting
* Feature scaling
* Neural Networks
* Binary classification
* TensorFlow/Keras
* Model evaluation

## 🔮 Future Improvements

Possible improvements include:

* Hyperparameter tuning
* Confusion matrix
* Precision, recall and F1-score
* ROC-AUC evaluation
* Training/validation accuracy visualization
* Training/validation loss visualization
* Streamlit deployment

## 👨‍💻 Author

**Ayan Ahmad**

GitHub: https://github.com/mohdayan7178-stack

LinkedIn: https://linkedin.com/in/mohd-ayan-027ba1386
