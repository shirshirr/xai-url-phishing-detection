# Explainable AI-Based URL Phishing Detection

An intelligent phishing URL detection system combining handcrafted URL features, TF-IDF-based textual representations, ensemble machine learning, and Explainable Artificial Intelligence (XAI) to improve detection transparency and interpretability.

## Overview

Phishing attacks use deceptive URLs to trick users into visiting malicious websites and exposing sensitive information.

Traditional machine learning models can identify suspicious URLs, but their predictions are often difficult to interpret.

This project explores an explainable machine learning framework for URL phishing detection, combining feature engineering, machine learning classification, and explainability techniques to understand why a URL is classified as legitimate or phishing.

## Project Objectives

- Develop machine learning models for phishing URL detection.
- Extract meaningful handcrafted URL features.
- Incorporate TF-IDF to capture URL-based textual patterns.
- Compare handcrafted-only and hybrid feature representations.
- Apply Explainable AI techniques to interpret model predictions.
- Investigate the faithfulness and reliability of generated explanations.

## Project Implementations

The repository contains three Jupyter notebooks:

| Notebook | Description |
|---|---|
| `handcrafted_features.ipynb` | Phishing detection using manually engineered URL features. |
| `handcrafted_tfidf.ipynb` | Hybrid phishing detection using handcrafted features and TF-IDF representations. |
| `faithfulness_analysis.ipynb` | Analysis of explanation faithfulness and reliability. |

## Methodology

### 1. Dataset Preparation

The project explores phishing and legitimate URL data collected from multiple sources, including:

- Kaggle
- PhishTank
- Alexa

Dataset preprocessing and preparation are performed before feature extraction and model training.

### 2. Feature Engineering

**A. Handcrafted URL Features**

Manually extracted URL characteristics include:

- URL length
- Number of dots
- Number of digits
- Presence of `@` symbol
- Other URL structural characteristics

**B. TF-IDF Features**

TF-IDF (Term Frequency–Inverse Document Frequency) is used to represent URL textual patterns numerically.

It helps capture distinguishing patterns in URL components that may indicate phishing activity.

**C. Hybrid Feature Representation**

The hybrid approach combines handcrafted URL features with TF-IDF representations to capture both structural and textual characteristics.

### 3. Machine Learning Models

The project explores ensemble-based classification using:

- Random Forest
- Multi-Layer Perceptron (MLP)
- XGBoost

A Voting Classifier is used to combine model predictions in the ensemble-based approach.

### 4. Explainable Artificial Intelligence

The project investigates multiple explainability techniques:

| Technique | Purpose |
|---|---|
| SHAP | Explains feature contributions to model predictions. |
| LIME | Provides local explanations for individual predictions. |
| Permutation Importance | Evaluates global feature importance by measuring performance changes after feature permutation. |
| DiCE | Generates counterfactual examples to investigate changes that could alter predictions. |

### 5. Faithfulness Analysis

An important aspect of explainable AI is determining whether explanations accurately represent the behaviour of the underlying model.

The faithfulness analysis notebook investigates the reliability of generated explanations and their relationship with model predictions.

## Technology Stack

- **Programming Language:** Python
- **Environment:** Jupyter Notebook
- **Machine Learning:** Scikit-learn, XGBoost
- **Data Processing:** Pandas, NumPy
- **Feature Extraction:** TF-IDF
- **Explainable AI:** SHAP, LIME, Permutation Importance, DiCE
- **Visualization:** Matplotlib, Seaborn

## Repository Structure

```text
xai-url-phishing-detection/
│
├── handcrafted_features.ipynb
├── handcrafted_tfidf.ipynb
├── faithfulness_analysis.ipynb
│
└── README.md
```

## Getting Started

### 1. Clone the Repository

```bash
git clone https://github.com/shirshir/xai-url-phishing-detection.git
cd xai-url-phishing-detection
```

### 2. Install Dependencies

```bash
pip install numpy pandas scikit-learn xgboost
pip install matplotlib seaborn shap lime dice-ml
```

### 3. Run the Notebooks

Launch Jupyter Notebook:

```bash
jupyter notebook
```

Open the required notebook and execute the cells sequentially.

**Note:** Dataset files are not currently included in this repository. You may need to configure the dataset paths according to your local environment.

## Research Focus

This project focuses on exploring the intersection of cybersecurity and Explainable Artificial Intelligence, particularly how interpretable machine learning techniques can improve the transparency and analysis of phishing detection systems.

## Future Scope

- Improve detection performance through advanced feature engineering.
- Investigate explanation stability and consistency.
- Develop consensus-based explanations using multiple XAI techniques.
- Integrate cybersecurity domain knowledge into explanation generation.
- Explore LLM-assisted generation of analyst-friendly explanations.

## Author

**Shishir**

AI/ML Research | Explainable AI | Cybersecurity | Phishing Detection

---

If you find this project interesting, feel free to explore the notebooks and follow the repository for future developments.
