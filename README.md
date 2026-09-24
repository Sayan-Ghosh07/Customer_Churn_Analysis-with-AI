# 📊 Customer Churn Analysis with AI

An end-to-end Data Analytics and Artificial Intelligence project for analyzing telecom customer behavior, predicting customer churn, identifying high-risk customers, and explaining machine learning predictions using Explainable AI techniques.

---

## 📌 Project Overview

Customer churn is an important business problem for telecom companies because retaining existing customers can be more efficient than acquiring new ones.

This project analyzes customer data to understand the factors and behavioral patterns associated with churn. A machine learning model is used to generate churn probabilities, evaluate customer risk, and identify customers who may require retention attention.

The project also uses SHAP (SHapley Additive exPlanations) to make machine learning predictions more interpretable and understand which features contribute to individual predictions.

The analysis combines:

- Data Analytics
- Exploratory Data Analysis
- Machine Learning
- Customer Risk Analysis
- Profit-Based Threshold Optimization
- Explainable AI
- SHAP Analysis
- Lift and Gains Analysis
- Customer Behavior Analysis

---

## 🎯 Objectives

The main objectives of this project are:

- Analyze telecom customer behavior and churn patterns.
- Explore the relationship between customer characteristics and churn.
- Perform exploratory data analysis and visualization.
- Evaluate a machine learning model for customer churn prediction.
- Measure model performance using ROC-AUC and PR-AUC.
- Generate churn probabilities for customers.
- Identify high-risk customers.
- Determine a business-oriented probability threshold using profit analysis.
- Explain model predictions using SHAP.
- Analyze customer risk using deciles, cumulative gains, and lift.
- Study the relationship between customer tenure and contract type.
- Analyze the effect of additional services on customer churn.
- Examine the relationship between important numerical features and predicted churn probability.

---

## 📂 Dataset

### IBM Telco Customer Churn Dataset

This project uses the Telco Customer Churn dataset containing information about telecom customers and their services.

The dataset includes information related to:

- Customer demographics
- Customer tenure
- Phone services
- Internet services
- Online security
- Online backup
- Device protection
- Technical support
- Streaming services
- Contract type
- Payment method
- Monthly charges
- Total charges
- Churn status

### Dataset Source

Kaggle:

https://www.kaggle.com/datasets/blastchar/telco-customer-churn

The dataset is commonly used for customer churn analysis and machine learning research and contains 7,043 customer records and 21 columns.

---

## 🛠️ Technologies Used

### Programming Language

- Python

### Data Analysis

- Pandas
- NumPy

### Data Visualization

- Matplotlib
- Seaborn

### Machine Learning

- Scikit-learn
- Joblib

### Explainable AI

- SHAP

### Development Tools

- Jupyter Notebook
- Git
- GitHub

---

## 🔄 Project Workflow

```text
Dataset
   ↓
Data Loading
   ↓
Data Cleaning
   ↓
Feature Engineering
   ↓
Exploratory Data Analysis
   ↓
Customer Behavior Analysis
   ↓
Machine Learning Model
   ↓
Model Evaluation
   ↓
Churn Probability Prediction
   ↓
Profit-Based Threshold Optimization
   ↓
SHAP Explainability
   ↓
Risk Decile Analysis
   ↓
Lift & Cumulative Gains Analysis
   ↓
Business Insights
```

---

## 📊 Exploratory Data Analysis

The project performs exploratory analysis to understand customer behavior and identify patterns related to churn.

### Categorical Features

The analysis includes churn behavior across:

- Contract type
- Internet service
- Payment method
- Technical support
- Online security
- Paperless billing
- Multiple lines
- Additional customer services

### Numerical Features

The project analyzes:

- Tenure
- Monthly charges
- Total charges
- Customer charges relative to tenure

### Visualizations

The notebook includes multiple visualizations such as:

- Churn distribution
- Churn rate comparisons
- Feature distributions
- Boxplots
- Correlation analysis
- Heatmaps
- Customer risk analysis
- Gains and lift charts
- SHAP visualizations

---

## 🤖 Machine Learning

A trained machine learning pipeline is used to generate customer churn probabilities.

Instead of using only a binary prediction, the model produces a probability representing the estimated likelihood that a customer will churn.

These probabilities are then used for:

- Customer risk ranking
- ROC analysis
- Precision-Recall analysis
- Threshold optimization
- Customer segmentation by risk
- Retention analysis
- Explainable AI

---

## 📈 Model Evaluation

The model is evaluated using several metrics.

### ROC-AUC

ROC-AUC measures the ability of the model to distinguish between customers who churn and customers who do not churn across different classification thresholds.

### PR-AUC

Precision-Recall AUC evaluates the relationship between precision and recall and provides useful information when identifying the positive class is important.

The project also performs probability-based customer ranking and risk analysis.

---

## 💰 Profit-Based Threshold Optimization

A classification threshold of 0.5 is not always the most appropriate threshold for a business application.

Therefore, this project evaluates different probability thresholds using a simplified business profit model.

The analysis considers factors such as:

- Potential customer value or margin
- Retention incentive cost
- Customer outreach cost
- Estimated benefit of successfully retaining a customer

The threshold producing the highest estimated profit is identified from the available assumptions.

> **Note:** The financial values used for threshold optimization are illustrative assumptions for analytical purposes. They should be replaced with real business costs and customer-value estimates before being used in a production environment.

---

## 🔍 Explainable AI with SHAP

SHAP (SHapley Additive exPlanations) is used to understand how individual features influence machine learning predictions.

### Global Feature Importance

SHAP analysis is used to identify features that have a strong influence on the model's predictions across the customer population.

### Local Customer Explanation

SHAP explanations are also generated for selected customers.

This helps answer questions such as:

- Why was this customer assigned a high churn probability?
- Which features contributed to the prediction?
- Which features pushed the prediction toward lower churn risk?

This makes the machine learning model easier to interpret.

---

## 🎯 Customer Risk Analysis

Customers are ranked according to their predicted churn probability.

The customers are then divided into risk groups/deciles.

The analysis calculates:

- Number of customers
- Number of actual churners
- Average predicted churn probability
- Cumulative churners captured
- Cumulative customer population
- Lift

This allows high-risk customer groups to be analyzed separately from lower-risk groups.

---

## 📈 Cumulative Gains and Lift Analysis

### Cumulative Gains

The cumulative gains analysis examines how many actual churners can be identified by targeting customers in descending order of predicted churn probability.

This helps evaluate how effectively the model can prioritize customers for potential retention campaigns.

### Lift Analysis

Lift measures the concentration of churners within different customer risk groups compared with the overall churn rate.

Higher lift indicates that a particular risk group contains a greater concentration of churners relative to the overall customer population.

---

## 📊 Tenure and Contract Analysis

Customer tenure and contract type are analyzed together to understand differences in churn behavior.

Tenure is divided into groups and compared across different contract categories.

A heatmap is used to visualize churn rates across the combinations of:

- Customer tenure
- Contract type

This provides a more detailed view of customer behavior than analyzing either feature separately.

---

## 🔧 Add-on Services Analysis

The project analyzes the relationship between additional services and customer churn.

The services considered include:

- Online Security
- Online Backup
- Device Protection
- Technical Support
- Streaming TV
- Streaming Movies

The analysis examines churn behavior based on the number of additional services used by customers.

---

## 📉 Partial Dependence Analysis

Partial dependence analysis is used to examine how selected numerical features relate to the model's predicted churn behavior.

The project analyzes features such as:

- Tenure
- Monthly Charges

Partial dependence plots provide an overall view of how changes in these features are associated with model predictions while averaging over other features.

---

## 🔬 SHAP Dependence Analysis

The project identifies influential features using mean absolute SHAP values.

SHAP dependence plots are then used to investigate how individual important features affect model predictions.

This provides additional insight into the relationship between customer characteristics and predicted churn risk.

---

## 💡 Key Insights

The analysis investigates several important customer churn patterns, including:

- Contract type is associated with differences in observed churn behavior.
- Customer tenure provides useful information when analyzing churn risk.
- Monthly charges are an important numerical feature for customer analysis.
- Payment method shows differences in observed churn rates.
- Additional services can be examined as indicators of customer behavior.
- Customer risk deciles can help prioritize customers based on predicted churn probability.
- SHAP provides explanations for both overall model behavior and individual customer predictions.
- Lift and cumulative gains analysis can help evaluate how effectively the model prioritizes potential churners.

These findings describe patterns observed in the dataset and model. They should not be interpreted as proof that a particular feature directly causes customer churn.

---

## 📁 Project Structure

```text
Customer_Churn_Analysis-with-AI/
│
├── data/
│   └── raw/
│       └── Telco-Customer-Churn.csv
│
├── models/
│   └── model.pkl
│
├── notebooks/
│   └── Sayan_Ghosh_Customer_Churn_Analysis.ipynb
│
├── src/
│   ├── features/
│   │   └── build_features.py
│   │
│   ├── models/
│   │   ├── predict.py
│   │   └── metrics.py
│   │
│   └── ...
│
├── requirements.txt
│
└── README.md
```

> Make sure the folder and file names above match the actual structure of your GitHub repository.

---

## 🚀 How to Run the Project

### 1. Clone the Repository

```bash
git clone https://github.com/Sayan-Ghosh07/Customer_Churn_Analysis-with-AI.git
```

### 2. Navigate to the Project Directory

```bash
cd Customer_Churn_Analysis-with-AI
```

### 3. Create a Virtual Environment

For Windows:

```bash
python -m venv venv
```

Activate the environment:

```bash
venv\Scriptsctivate
```

For Git Bash:

```bash
source venv/Scripts/activate
```

### 4. Install Dependencies

```bash
pip install -r requirements.txt
```

### 5. Download the Dataset

Download the Telco Customer Churn dataset from:

https://www.kaggle.com/datasets/blastchar/telco-customer-churn

Place the dataset inside:

```text
data/raw/
```

The expected dataset file is:

```text
data/raw/Telco-Customer-Churn.csv
```

### 6. Launch Jupyter Notebook

```bash
jupyter notebook
```

Open:

```text
notebooks/Sayan_Ghosh_Customer_Churn_Analysis.ipynb
```

Run the notebook cells sequentially.

---

## 📦 Requirements

The project uses the following Python libraries:

```text
numpy
pandas
matplotlib
seaborn
scikit-learn
joblib
shap
jupyter
openpyxl
```

A complete dependency list is available in:

```text
requirements.txt
```

---

## ⚠️ Limitations

- The dataset represents a historical/sample telecom customer population.
- The dataset may not represent every telecom market or customer population.
- Model performance depends on the dataset and preprocessing pipeline.
- Feature importance does not necessarily imply causation.
- Profit calculations use illustrative assumptions.
- Predictions should be validated using current business data before being used for real-world customer retention decisions.
- Model performance and data distribution should be monitored if the model is deployed in production.

---

## 🔮 Future Scope

The project can be further improved by:

- Developing an interactive Streamlit dashboard.
- Deploying the churn prediction model as a web application.
- Adding real-time customer churn scoring.
- Performing model calibration.
- Monitoring model and data drift.
- Adding customer segmentation using clustering.
- Testing different customer retention strategies.
- Integrating the model with CRM systems.
- Performing A/B testing of retention campaigns.
- Using real business retention costs and customer lifetime value for improved threshold optimization.

---

## 👨‍💻 Author

**Sayan Ghosh**

GitHub:  
https://github.com/Sayan-Ghosh07

Project:  
**Customer Churn Analysis with AI**

---

## 📚 Dataset Reference

IBM Telco Customer Churn dataset distributed through Kaggle:

https://www.kaggle.com/datasets/blastchar/telco-customer-churn

---

## ⭐ Project Highlights

- 📊 Exploratory Data Analysis
- 🤖 Machine Learning
- 🎯 Customer Churn Prediction
- 📈 ROC-AUC and PR-AUC Evaluation
- 💰 Profit-Based Threshold Optimization
- 🔍 SHAP Explainable AI
- 📊 Risk Decile Analysis
- 📈 Cumulative Gains and Lift Analysis
- 👥 Customer Behavior Analysis
- 📉 Partial Dependence Analysis
- 🔬 SHAP Dependence Analysis

---

**Built using Python, Data Analytics, Machine Learning, and Explainable AI.**
