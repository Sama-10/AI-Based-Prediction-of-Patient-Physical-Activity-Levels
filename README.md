
# AI-Based Prediction of Patient Physical Activity Levels

An Artificial Intelligence and Machine Learning group project developed at **Sri Lanka Institute of Information Technology (SLIIT)** for the **IT2011 – Artificial Intelligence and Machine Learning** module.

## 📌 Project Overview

This project focuses on developing an AI/ML-based predictive system to classify an individual's physical activity level into three categories:

- **Low**
- **Moderate**
- **High**

The system uses routine health indicators and lifestyle information to identify patterns and relationships between physiological factors and physical activity levels.

The objective is to support preventive healthcare by providing insights into physical activity patterns and promoting healthier lifestyles.

## 🎯 Project Objectives

- Develop machine learning models to predict patient physical activity levels.
- Analyze relationships between health indicators and physical activity.
- Perform data preprocessing, cleaning, and exploratory data analysis (EDA).
- Address class imbalance to improve classification performance.
- Compare multiple machine learning algorithms.
- Identify the best-performing model using classification evaluation metrics.

## 📂 Dataset Overview

The project uses a health-related dataset containing physiological and lifestyle attributes.

**Original Dataset:**
- Records: 25,000
- Features: 11
- Missing values: None identified in the initial dataset analysis.

**Main Features:**

| Feature | Description |
|---|---|
| Age | Patient age |
| BMI | Body Mass Index |
| Systolic_BP | Systolic blood pressure |
| Diastolic_BP | Diastolic blood pressure |
| Total_Cholesterol | Total cholesterol level |
| HDL_Cholesterol | HDL cholesterol level |
| LDL_Cholesterol | LDL cholesterol level |
| Triglycerides | Triglyceride level |
| Smoking_Status | Smoking status |
| Physical_Activity_Level | Target variable |

**Target Classes:** Low, Moderate, and High.

## ⚙️ Machine Learning Workflow

The project follows a structured machine learning pipeline.

### 1. Data Preprocessing

- Missing value analysis and handling.
- Duplicate record identification.
- Categorical variable encoding.
- Outlier detection and treatment using the IQR method.
- Feature engineering.
- Feature selection using Variance Threshold.
- Numerical feature normalization using Min-Max Scaling.

### 2. Exploratory Data Analysis (EDA)

- Analyzed distributions of health indicators.
- Examined physical activity class distributions.
- Visualized correlations between selected features.
- Investigated patterns in patient health attributes.

### 3. Outlier Treatment

The Interquartile Range (IQR) method was applied to identify extreme values in numerical health features.

A conservative 1.5 × IQR capping technique was used to reduce the influence of extreme observations while preserving valuable data.

### 4. Feature Engineering

Two additional categorical features were developed:

- **BMI Category:** Underweight, Normal, Overweight, and Obese.
- **BP Category:** Low BP, Normal BP, and Hypertension.

### 5. Class Imbalance Handling

SMOTE (Synthetic Minority Over-sampling Technique) was applied to the training dataset to improve the representation of minority classes.

### 6. Model Training and Evaluation

- Training and testing split: 70% / 30%.
- Stratified sampling to maintain class distribution.
- Random state: 42.
- Hyperparameter optimization and model evaluation.

## 🤖 Machine Learning Algorithms

Six machine learning algorithms were evaluated:

1. Random Forest
2. XGBoost
3. Decision Tree
4. Support Vector Machine (SVM)
5. K-Nearest Neighbors (KNN)
6. Logistic Regression

## 📊 Model Performance

The tuned Random Forest model achieved the strongest overall performance among the evaluated models.

| Evaluation Metric | Random Forest |
|---|---:|
| Accuracy | 66.7% |
| Precision | 0.83 |
| Recall | 0.67 |
| F1-Score | 0.663 |

**Best Performing Model:** Random Forest Classifier

The results demonstrate the effectiveness of ensemble-based learning techniques in identifying patterns within the health dataset.

## 👨‍💻 My Contributions

As a member of this six-person group project, my main responsibilities included:

### 🧹 Data Preprocessing & Outlier Treatment

- Conducted comprehensive outlier analysis across numerical health features using the Interquartile Range (IQR) method.
- Identified outliers in Systolic BP, Diastolic BP, LDL Cholesterol, Triglycerides, BMI, and Age.
- Implemented a conservative 1.5 × IQR capping technique to minimize information loss while reducing the influence of extreme values.

### 🌲 Random Forest Model Development

- Developed and trained a Random Forest classification model.
- Contributed to the model training and evaluation pipeline.
- Predicted patient physical activity levels across Low, Moderate, and High categories.
- Evaluated model performance using Accuracy, Precision, Recall, and F1-Score.

## 📁 Repository Structure

```text
AI-Based-Prediction-of-Patient-Physical-Activity-Levels/
│
├── Data/
│   └── Health.csv
│
├── notebooks/
│   ├── Encoding_Categorical_Variables.ipynb
│   ├── Feature_Selection.ipynb
│   ├── Handling_Claas_Imbalance.ipynb
│   ├── Handling_Missing_Data.ipynb
│   ├── Outlier_Removal.ipynb
│   └── Scaling.ipynb
│
├── Results/
│   ├── eda_visualization/
│   └── outputs/
│
├── docs/
│   └── Final_Report.pdf
│
├── requirements.txt
└── README.md
```

## 🛠️ Technologies & Tools

- **Programming Language:** Python
- **Data Manipulation:** Pandas, NumPy
- **Machine Learning:** Scikit-learn, Imbalanced-learn, XGBoost
- **Data Visualization:** Matplotlib, Seaborn
- **Development Environment:** Jupyter Notebook

## 🚀 Getting Started

### Prerequisites

Make sure Python 3.8 or later and Jupyter Notebook are installed.

### 1. Clone the Repository

```bash
git clone https://github.com/YOUR-USERNAME/YOUR-REPOSITORY-NAME.git
```

### 2. Navigate to the Project Directory

```bash
cd YOUR-REPOSITORY-NAME
```

### 3. Install Dependencies

```bash
pip install pandas numpy scikit-learn imbalanced-learn matplotlib seaborn xgboost jupyter
```

### 4. Launch Jupyter Notebook

```bash
jupyter notebook
```

Open the notebooks directory and execute the notebooks to explore the preprocessing and analysis workflow.

## 👥 Project Team

This was a collaborative project completed by a six-member team.

1. Henarangoda M.P.
2. Gunasena P.G.P.
3. Hansaja H.A.
4. Lakshan M.S.
5. Jayasena W.M.S.A.
6. Wickramarachchi W.A.D.M.

**Institution:** Sri Lanka Institute of Information Technology (SLIIT)  
**Degree Programme:** B.Sc. (Hons) in Information Technology  
**Academic Year:** Year 2 – Semester 1  
**Module:** IT2011 – Artificial Intelligence and Machine Learning

## 🔮 Future Improvements

- Improve classification accuracy through advanced ensemble techniques.
- Explore explainable AI (XAI) for model interpretability.
- Improve prediction confidence and reliability.
- Integrate additional health and lifestyle features.
- Develop a user-friendly application for real-world use.

## ⚠️ Disclaimer

This project was developed for academic and educational purposes. Its predictions are not intended to replace professional medical advice, diagnosis, or treatment.

---

⭐ If you find this project interesting, feel free to explore the notebooks and machine learning workflow.

**Developed as a six-member academic group project at SLIIT.**
