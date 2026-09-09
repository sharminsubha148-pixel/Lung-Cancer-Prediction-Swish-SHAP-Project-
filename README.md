# An Interpretable Deep Learning Framework for Lung Cancer Prediction using Swish-optimized Neural Networks and SHAP Explanations

This repository contains the official implementation and source code for the research paper accepted and published in **IEEE**. The project proposes a robust, clinically interpretable deep learning framework designed for accurate lung cancer prediction, addressing class imbalance using SMOTE and utilizing **SHAP (SHapley Additive exPlanations)** to ensure model transparency and clinical interpretability.

---

## 📌 Table of Contents
- [Abstract](#-abstract)
- [Dataset Details](#-dataset-details)
- [Key Features & Methodology](#-key-features--methodology)
- [Project Structure](#-project-structure)
- [Installation & Setup](#-installation--setup)
- [Running the Code](#-running-the-code)
- [Model Evaluation & Results](#-model-evaluation--results)
- [Explainable AI (SHAP) Analysis](#-explainable-ai-shap-analysis)
- [Citation](#-citation)

---

## 📖 Abstract
Early detection of lung cancer significantly improves patient survival rates. However, traditional "black-box" deep learning models lack the transparency required in clinical decision-making. This study introduces an optimized deep learning framework integrated with Swish activation functions for enhanced pattern recognition in medical survey data. To mitigate the class imbalance inherent in medical datasets, SMOTE (Synthetic Minority Over-sampling Technique) was applied. Furthermore, SHAP analysis was incorporated to provide patient-specific and global feature interpretability, bridging the gap between high predictive accuracy and clinical trust.

---

## 📊 Dataset Details
* **Source:** UCI Machine Learning Repository / Standard Lung Cancer Survey Dataset.
* **Features:** Includes demographic details (Age, Gender) and clinical/lifestyle symptoms (Smoking, Yellow Fingers, Anxiety, Peer Pressure, Chronic Disease, Fatigue, Allergy, Wheezing, Alcohol Consumption, Coughing, Shortness of Breath, Swallowing Difficulty, Chest Pain).
* **Target Variable:** `LUNG_CANCER` (YES / NO).

---

## ⚙️ Key Features & Methodology
1. **Data Preprocessing:** Cleaning, duplicate removal, handling missing values, and label encoding for categorical attributes.
2. **Class Imbalance Handling:** Implementation of **SMOTE** to balance the target classes and prevent model bias.
3. **Deep Neural Network (DNN):** Built using **TensorFlow/Keras** featuring Dense layers, Dropout for regularization, Batch Normalization, and callbacks (`EarlyStopping`, `ReduceLROnPlateau`).
4. **Clinical Interpretability:** Integration of **SHAP** to compute Shapley values and explain individual predictions as well as overall feature importance.

---

## 📂 Project Structure
```text
├── dataset/
│   └── survey lung cancer.csv   # Dataset file
├── notebooks/                   # Jupyter Notebooks / VS Code script files
├── models/                      # Saved trained models (optional)
├── outputs/                     # Generated evaluation plots & SHAP summaries
├── requirements.txt             # Required Python packages
└── README.md                    # Project Documentation
🛠️ Installation & Setup
Clone the Repository:

Bash
git clone [https://github.com/your-username/your-repo-name.git](https://github.com/your-username/your-repo-name.git)
cd your-repo-name
Create a Virtual Environment (Recommended):

Bash
python -m venv venv
source venv/bin/activate   # On Windows use: venv\Scripts\activate
Install Dependencies:

Bash
pip install -r requirements.txt
🚀 Running the Code
You can run this project in VS Code or Jupyter Notebook:

Open the project folder in VS Code.

Make sure you have the Jupyter extension installed in VS Code.

Update the dataset file path in the code to match your local directory:

Python
df = pd.read_csv("path/to/your/survey lung cancer.csv")
Run the cells sequentially to execute data preprocessing, SMOTE balancing, deep learning model training, and SHAP interpretability analysis.

📈 Model Evaluation & Results
Performance Metrics: Evaluated using Accuracy, Precision, Recall, F1-Score, and ROC-AUC Curve.

Handling Imbalance: Visualized class distribution before and after applying SMOTE to ensure unbiased data distribution.

🔍 Explainable AI (SHAP) Analysis
To satisfy medical standards, the model uses SHAP values to uncover:

Which clinical symptoms have the highest impact on lung cancer risk prediction.

Directional impact of features (e.g., how specific symptom combinations escalate risk scores for individual patients).
