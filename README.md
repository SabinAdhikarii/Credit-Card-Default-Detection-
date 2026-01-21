# 💳 Credit Card Default Detection System

[![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)](https://www.python.org/downloads/)
[![Machine Learning](https://img.shields.io/badge/ML-Scikit--Learn-orange.svg)](https://scikit-learn.org/)
[![License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)
[![Status](https://img.shields.io/badge/Status-Complete-success.svg)]()

> An AI-powered machine learning system that predicts credit card default risk using supervised learning algorithms.

**Student:** Sabin Adhikari (23048604)  
**Module:** CU6051NI Artificial Intelligence  
**Institution:** London Metropolitan University  
**Semester:** Autumn 2025

---

## 🎯 Overview

Credit card default prediction is a critical challenge in the financial sector. This project implements a **supervised machine learning solution** to predict whether a credit card customer will default on their payment in the following month.

### Why This Matters?

- 💰 **Financial Impact:** Banks lose billions annually due to credit card defaults
- 🔍 **Early Detection:** Identify high-risk customers before defaults occur
- 📊 **Data-Driven Decisions:** Replace traditional credit scoring with AI-powered predictions
- 🇳🇵 **Nepal Context:** With 318,428+ credit cards in circulation, proactive risk management is essential

### Key Objectives

✅ Develop accurate ML models for default prediction  
✅ Compare multiple classification algorithms  
✅ Achieve >80% prediction accuracy  
✅ Provide actionable insights for financial institutions  
✅ Enable proactive risk mitigation strategies

---

## ❗ Problem Statement

**Challenge:** Traditional credit scoring systems fail to capture complex behavioral and financial patterns that influence default risk.

**Issues:**
- Limited demographic and historical data
- Imbalanced datasets (77% non-default vs 23% default)
- Delayed detection leading to financial losses
- Manual assessment prone to errors

**Solution:** Implement machine learning algorithms that analyze 23+ features including payment history, billing amounts, demographics, and credit utilization to predict default probability with high accuracy.

---

## 📊 Dataset

**Source:** [UCI Machine Learning Repository](https://archive.ics.uci.edu/ml/datasets/default+of+credit+card+clients)

**Dataset Name:** Default of Credit Card Clients (Taiwan)

### Dataset Characteristics

| Attribute | Details |
|-----------|---------|
| **Instances** | 30,000 credit card clients |
| **Features** | 23 input variables + 1 target variable |
| **Target** | default.payment.next.month (binary: 0 = No Default, 1 = Default) |
| **Class Distribution** | ~22% Default, ~78% Non-default (Imbalanced) |
| **Time Period** | 2005-2006 (Taiwan) |
| **Feature Types** | Mixed (Categorical + Numerical) |

### Key Features

- **Demographics:** Age, Gender, Education, Marriage Status
- **Credit Information:** Credit Limit
- **Payment History:** PAY_0 to PAY_6 (6 months repayment status)
- **Bill Amounts:** BILL_AMT1 to BILL_AMT6
- **Payment Amounts:** PAY_AMT1 to PAY_AMT6

---

## ✨ Features

### Core Functionality

- 📥 **Data Loading & Preprocessing**
  - Automatic dataset loading from UCI Repository
  - Missing value handling
  - Feature scaling using StandardScaler
  - Train-test split (80:20 ratio)

- 🤖 **Machine Learning Models**
  - Logistic Regression (Baseline)
  - Random Forest Classifier
  - Gradient Boosting Classifier

- 📈 **Model Evaluation**
  - Accuracy, Precision, Recall, F1-Score
  - ROC-AUC Score
  - Confusion Matrix
  - ROC Curves

- 🎨 **Visualizations**
  - Class distribution plots
  - Model performance comparison charts
  - Confusion matrices heatmaps
  - ROC curve analysis
  - Feature importance analysis (Top 15 features)

- 💾 **Results Export**
  - Model comparison CSV
  - Feature importance CSV
  - Trained model serialization

---

## 🛠️ Technologies Used

### Programming Language
- **Python 3.8+**

### Core Libraries

| Library | Purpose |
|---------|---------|
| **Pandas** | Data manipulation and analysis |
| **NumPy** | Numerical computations |
| **Scikit-learn** | Machine learning algorithms and metrics |
| **Matplotlib** | Data visualization |
| **Seaborn** | Statistical data visualization |
| **Google Colab** | Development environment |

### Machine Learning Algorithms

1. **Logistic Regression**
   - Binary classification baseline
   - Sigmoid function for probability estimation
   - Interpretable coefficients

2. **Random Forest**
   - Ensemble of 100 decision trees
   - Handles non-linear relationships
   - Robust to overfitting

3. **Gradient Boosting**
   - Sequential ensemble learning
   - Minimizes loss function iteratively
   - Industry-standard for financial predictions

---

## 🚀 Installation

### Prerequisites

- Python 3.8 or higher
- pip (Python package installer)
- Google Colab account (recommended) or Jupyter Notebook

### Option 1: Google Colab (Recommended)

1. Open [Google Colab](https://colab.research.google.com/)
2. Upload the `Credit_Card_Default_Detection.ipynb` notebook
3. Run all cells - libraries are pre-installed!

### Option 2: Local Installation

```bash
# Clone the repository
git clone https://github.com/SabinAdhikarii/Credit-Card-Default-Detection.git
cd Credit-Card-Default-Detection

# Create virtual environment (optional but recommended)
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate

# Install required packages
pip install -r requirements.txt
```

### `requirements.txt`

```txt
numpy>=1.21.0
pandas>=1.3.0
scikit-learn>=1.0.0
matplotlib>=3.4.0
seaborn>=0.11.0
openpyxl>=3.0.0
```

---

## 💻 Usage

### Quick Start

1. **Open the Notebook**
   ```bash
   jupyter notebook Credit_Card_Default_Detection.ipynb
   ```
   Or upload to Google Colab

2. **Run All Cells**
   - Dataset loads automatically from UCI Repository
   - Models train and evaluate sequentially
   - Results display with visualizations

3. **View Results**
   - Model comparison table
   - Performance metrics
   - Confusion matrices
   - ROC curves
   - Feature importance
   - 
## 📊 Model Performance

### Results Summary

| Model | Accuracy | Precision | Recall | F1-Score | ROC-AUC |
|-------|----------|-----------|--------|----------|---------|
| **Logistic Regression** | 80.87% | 65.23% | 42.15% | 51.22% | 77.45% |
| **Random Forest** | 81.73% | 67.84% | 43.78% | 53.17% | 77.89% |
| **🏆 Gradient Boosting** | **81.93%** | **68.70%** | **44.96%** | **54.36%** | **78.23%** |

### Best Model: Gradient Boosting ✨

**Accuracy:** 81.93%

**Why Gradient Boosting?**
- ✅ Highest accuracy among all models
- ✅ Best balance of precision and recall
- ✅ Sequential learning corrects previous errors
- ✅ Captures complex non-linear patterns
- ✅ Industry-standard for financial risk modeling

### Key Findings

1. **Top 5 Most Important Features:**
   - PAY_0 (Repayment status - most recent month)
   - PAY_2 (Repayment status - 2 months ago)
   - PAY_3 (Repayment status - 3 months ago)
   - LIMIT_BAL (Credit limit)
   - PAY_AMT1 (Payment amount - most recent)

2. **Model Insights:**
   - Payment history is the strongest predictor
   - Recent behavior matters more than older history
   - Credit limit utilization impacts default risk
   - Demographic features have moderate influence

---

| Metric | Count | Percentage |
|--------|-------|------------|
| **True Negatives (TN)** | 4,585 | 76.42% |
| **False Positives (FP)** | 580 | 9.67% |
| **False Negatives (FN)** | 502 | 8.37% |
| **True Positives (TP)** | 333 | 5.55% |

**Interpretation:**
- High TN: Successfully identifies non-defaulters
- Low TP: Room for improvement in catching actual defaulters
- Trade-off between false alarms and missed defaults

---
```

## 🤝 Contributing

Contributions are welcome! Here's how you can help:

### How to Contribute

1. **Fork the repository**
   ```bash
   git fork https://github.com/SabinAdhikarii/Credit-Card-Default-Detection.git
   ```

2. **Create a feature branch**
   ```bash
   git checkout -b feature/AmazingFeature
   ```

3. **Commit your changes**
   ```bash
   git commit -m 'Add some AmazingFeature'
   ```

4. **Push to the branch**
   ```bash
   git push origin feature/AmazingFeature
   ```

5. **Open a Pull Request**

### Contribution Guidelines

- Follow PEP 8 coding standards
- Add comments and docstrings
- Update documentation
- Write unit tests for new features
- Ensure all tests pass before submitting

### Areas for Contribution

- 🐛 Bug fixes
- ✨ New features
- 📝 Documentation improvements
- 🎨 UI/UX enhancements
- 🧪 Test coverage
- 🌐 Translations

---

## 📜 License

This project is licensed under the **MIT License** - see the [LICENSE](LICENSE) file for details.

```
---

## ⭐ Star This Repository!

If you find this project useful, please give it a ⭐ on GitHub!

```
Made with ❤️ by Sabin Adhikari | © 2025
```

---

### 📈 Project Status

![Status](https://img.shields.io/badge/Status-Complete-brightgreen)
![Maintenance](https://img.shields.io/badge/Maintained-Yes-green)
![Last Updated](https://img.shields.io/badge/Last%20Updated-January%202025-blue)

**Version:** 1.0.0  
**Last Updated:** January 21, 2025  
**Status:** ✅ Completed & Deployed





## 🤝 Contributing

Contributions are welcome! Please feel free to submit issues or pull requests to improve the project.

---


## 👤 Author

**SabinAdhikari**  
GitHub: [SabinAdhikarii](https://github.com/SabinAdhikarii)

---

## 📞 Support

For questions or issues, please contact me at sabinofficial99@gmail.com).

---

**Version:** 1.0.0  
**Last Updated:** January 21, 2025  
**Status:** ✅ Completed & Deployed
