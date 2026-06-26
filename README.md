# Employee Attrition Prediction using Machine Learning

> **Machine Learning Internship – Week 2 Project**

Predicting employee attrition using machine learning and translating analytical findings into actionable Human Resources (HR) recommendations.

---

# 📖 Project Overview

Employee attrition is one of the biggest challenges faced by organizations across industries. Losing experienced employees results in increased recruitment costs, onboarding expenses, knowledge loss, reduced productivity, and disruption of ongoing projects.

The objective of this project is to analyze historical employee information to identify patterns associated with employee turnover and develop a predictive machine learning model capable of identifying employees who are more likely to leave the organization.

Beyond prediction, this project emphasizes translating analytical findings into practical business recommendations that HR teams can use to improve employee retention.

---

# 🎯 Problem Statement

Every organization experiences employee turnover, but unexpected attrition can significantly affect business operations.

The objective of this project is to answer questions such as:

* Which employees are more likely to leave?
* Which departments experience the highest turnover?
* Does salary alone explain employee attrition?
* What workplace factors contribute most to employee resignation?
* How can HR proactively improve employee retention?

---

# 📂 Dataset Information

**Dataset Name**

IBM HR Analytics Employee Attrition & Performance

**Source**

https://www.kaggle.com/datasets/pavansubhasht/ibm-hr-analytics-attrition-dataset

### Dataset Statistics

| Property               |                     Value |
| ---------------------- | ------------------------: |
| Total Employees        |                      1470 |
| Features               | 35 (before preprocessing) |
| Target Variable        |                 Attrition |
| Employees Stayed       |                      1233 |
| Employees Left         |                       237 |
| Overall Attrition Rate |                    ~16.1% |

Target Variable:

* **Yes** → Employee left the organization
* **No** → Employee stayed with the organization

---

# 🛠 Technologies Used

| Tool         | Purpose                              |
| ------------ | ------------------------------------ |
| Python       | Programming Language                 |
| Google Colab | Development Environment              |
| Pandas       | Data Loading & Manipulation          |
| NumPy        | Numerical Operations                 |
| Matplotlib   | Data Visualization                   |
| Seaborn      | Statistical Visualization            |
| Scikit-learn | Machine Learning Models & Evaluation |

---

# 📌 Project Workflow

The project follows a complete machine learning pipeline.

## 1. Data Loading

* Imported the HR dataset
* Examined dataset dimensions
* Identified feature types
* Calculated overall attrition rate

---

## 2. Data Cleaning

The dataset was prepared for machine learning by:

* Checking missing values
* Removing duplicate records
* Removing irrelevant columns

  * EmployeeNumber
  * EmployeeCount
  * Over18
  * StandardHours
* Encoding the target variable
* Applying One-Hot Encoding to categorical variables
* Standardizing numerical features using StandardScaler

---

## 3. Exploratory Data Analysis (EDA)

Several business-focused analyses were performed to understand employee turnover patterns.

The following questions were investigated:

* Which department experiences the highest attrition?
* Which job roles are most affected?
* Does salary influence employee attrition?
* How does work-life balance relate to employee turnover?
* During which stage of employment do employees usually resign?

The notebook includes visualizations such as:

* Department-wise Attrition Rate
* Job Role-wise Attrition Rate
* Monthly Income vs Attrition
* Work-Life Balance vs Attrition
* Years at Company vs Attrition

---

## 4. Machine Learning Models

Three classification models were trained and compared.

| Model                        |
| ---------------------------- |
| Logistic Regression          |
| Random Forest Classifier     |
| Gradient Boosting Classifier |

The dataset was divided into:

* **Training Set:** 80%
* **Testing Set:** 20%

To reduce the impact of class imbalance, `class_weight='balanced'` was used wherever supported.

---

## 5. Model Evaluation

Models were evaluated using multiple performance metrics:

* Precision
* Recall
* F1-Score
* ROC-AUC Score
* Confusion Matrix

A comparison table was created to determine the best-performing model.

---

## 6. Feature Importance Analysis

After selecting the best-performing model, feature importance analysis was conducted to determine which employee characteristics most strongly influenced attrition predictions.

The ten most influential features were visualized using a horizontal bar chart.

---

# 📊 Key Findings

The exploratory analysis produced several important business insights.

### Department Analysis

* Sales recorded the highest attrition rate (~20.6%).
* Research & Development showed the lowest attrition.

### Job Role Analysis

* Sales Representatives exhibited the highest attrition (~39.8%).
* Laboratory Technicians also experienced relatively high turnover.
* Managers and Research Directors showed the lowest attrition.

### Salary Analysis

Employees who left generally earned lower salaries.

However, salary alone was insufficient to explain employee turnover, indicating that workplace conditions and job characteristics also influence attrition.

### Work-Life Balance

Employees reporting poor work-life balance experienced substantially higher attrition than employees reporting better work-life balance.

### Employee Tenure

Most resignations occurred during the early years of employment, suggesting that onboarding and early-career engagement are critical.

---

# 💼 Business Recommendations

Based on the analysis, the following recommendations are proposed:

* Prioritize retention initiatives within the Sales department.
* Conduct regular retention discussions with Sales Representatives and Laboratory Technicians.
* Improve work-life balance through flexible work arrangements and workload management.
* Strengthen onboarding, mentoring, and career development programs during employees' first few years.
* Monitor employees working frequent overtime or traveling regularly for business.

---

# 📈 Project Outputs

The project includes:

* Complete exploratory data analysis
* Machine learning model comparison
* Confusion Matrix
* ROC Curve
* Top 10 Important Features
* HR-focused business recommendations
* Executive Summary for non-technical stakeholders

---

# 📁 Repository Structure

```text
EmployeeAttrition_Indrayani/
│
├── analysis.ipynb
├── HR_Attrition.csv
├── README.md
├── summary.pdf
└── charts/
    ├── AttritionRateByDept.png
    ├── AttritionRateByJobRole.png
    ├── MonthlyIncomeByAttrition.png
    ├── AttritionRateByWorkLife.png
    ├── AttritionVSYearsAtCompany.png
    ├── ConfusionMatrixLR.png
    ├── Top10ImpFeatures.png
    └── ROC_Curve.png
```

---

# ▶️ Running the Project

1. Open `analysis.ipynb` in Google Colab.
2. Execute all cells from top to bottom.
3. The dataset is automatically downloaded using **gdown**, so no manual upload is required.
4. The notebook generates all charts, model evaluation metrics, and business recommendations.

---

# ⚠️ Project Limitation

The prediction model is built using historical employee information available in the dataset. Factors such as personal circumstances, organizational restructuring, economic conditions, employee relationships, or future policy changes are not included. Therefore, the model should be used as a decision-support tool alongside HR expertise rather than as the sole basis for employee-related decisions.

---

# 👩‍💻 Author

**Indrayani Mude**

Machine Learning Internship – Week 2

Employee Attrition Prediction using Machine Learning
