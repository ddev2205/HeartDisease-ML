# Software Requirements Specification (SRS)
## Heart Disease Prediction Machine Learning Model

**Document Version:** 1.0  
**Date:** August 30, 2025  
**Prepared by:** Divyanshu Dev, Krish Tyagi, Kashish  
**Project:** Heart Disease Prediction ML Model - Educational Tool  

---

## Table of Contents

1. [Introduction](#1-introduction)  
   - 1.1 [Purpose](#11-purpose)  
   - 1.2 [Document Scope](#12-document-scope)  
   - 1.3 [Target Users](#13-target-users)  
   - 1.4 [Definitions and Terms](#14-definitions-and-terms)  
   - 1.5 [References](#15-references)  

2. [Overall Description](#2-overall-description)  
   - 2.1 [Product Overview](#21-product-overview)  
   - 2.2 [Main Functions](#22-main-functions)  
   - 2.3 [User Types](#23-user-types)  
   - 2.4 [System Environment](#24-system-environment)  
   - 2.5 [Assumptions](#25-assumptions)  

3. [System Requirements](#3-system-requirements)  
   - 3.1 [User Interface](#31-user-interface)  
   - 3.2 [Software Requirements](#32-software-requirements)  
   - 3.3 [Hardware Requirements](#33-hardware-requirements)  

4. [System Features](#4-system-features)  
   - 4.1 [Data Loading](#41-data-loading)  
   - 4.2 [Data Analysis](#42-data-analysis)  
   - 4.3 [Data Preparation](#43-data-preparation)  
   - 4.4 [Model Training](#44-model-training)  
   - 4.5 [Model Testing](#45-model-testing)  
   - 4.6 [Results Display](#46-results-display)  

5. [Performance Requirements](#5-performance-requirements)  

6. [Other Requirements](#6-other-requirements)  

---

## 1. Introduction

### 1.1 Purpose

This document describes a simple machine learning project to predict heart disease using patient data. The system is built for learning purposes and helps students understand how to use basic ML algorithms for classification problems.

The project uses the UCI Heart Disease dataset and implements three simple algorithms: Logistic Regression, Decision Tree, and Random Forest.

### 1.2 Document Scope

This project covers:  
- Loading heart disease data from UCI dataset  
- Basic data analysis and visualization  
- Training three different ML models  
- Testing model performance  
- Comparing results between models  

**Not Included:**  
- Real medical diagnosis  
- Advanced ML techniques  
- Clinical use or deployment  
- Complex data processing  

### 1.3 Target Users

**Students:** Learning machine learning basics  
- Need: Simple examples and clear explanations  
- Skills: Basic Python knowledge  

**Teachers:** Using for ML education  
- Need: Easy to understand and modify  
- Skills: Good programming knowledge  

### 1.4 Definitions and Terms

| Term               | Meaning                                           |
|--------------------|--------------------------------------------------|
| **ML**             | Machine Learning                                  |
| **Classification** | Predicting categories (yes/no for heart disease) |
| **Training Data**  | Data used to teach the model                       |
| **Test Data**      | Data used to check how well the model works       |
| **Accuracy**       | How often the model makes correct predictions     |
| **Precision**      | How many positive predictions are actually correct|
| **Recall**         | How many actual positives the model finds         |
| **F1-Score**       | Combines precision and recall into one number     |
| **Confusion Matrix**| Table showing correct and wrong predictions       |

### 1.5 References

1. **UCI Heart Disease Dataset**  
   Heart Disease Data Set. UCI Machine Learning Repository.

2. **Python Libraries**  
   - Pandas for data handling  
   - NumPy for calculations  
   - Matplotlib for charts  
   - Scikit-learn for ML algorithms  

---

## 2. Overall Description

### 2.1 Product Overview

This is a simple educational tool built as a Jupyter notebook. It teaches students how to:  
- Work with real medical data  
- Apply basic ML algorithms  
- Compare different models  
- Understand classification results  

The system is standalone and doesn't connect to other medical systems. It's only for learning, not for actual medical use.

### 2.2 Main Functions

The system does these main tasks:

**Data Handling**  
- Loads heart disease dataset (303 patients, 13 features)  
- Cleans missing data  
- Prepares data for ML models  

**Model Building**  
- Trains Logistic Regression model  
- Trains Decision Tree model  
- Trains Random Forest model  

**Results Analysis**  
- Tests each model on new data  
- Calculates accuracy scores  
- Creates comparison charts  
- Shows confusion matrices  

### 2.3 User Types

**Primary Users - Students**  
- Learning ML for the first time  
- Want to see how algorithms work  
- Need step-by-step explanations  

**Secondary Users - Instructors**  
- Teaching ML concepts  
- Need working examples for classes  
- May modify code for assignments  

### 2.4 System Environment

**Software Needed:**  
- Python 3.7 or newer  
- Jupyter Notebook  
- Required packages: pandas, numpy, scikit-learn, matplotlib, seaborn  

**Hardware Needed:**  
- Any regular computer with 2GB RAM  
- 500MB free disk space  
- Internet connection (only for first-time setup)  

**Operating Systems:**  
- Windows 10+  
- Mac OS 10.14+  
- Linux (Ubuntu 18.04+)  

### 2.5 Assumptions

**What We Assume:**  
- Users know basic Python programming  
- Users can install Python packages  
- Dataset remains available online  
- Learning is more important than perfect accuracy  
- Simple approach is better than complex methods  

---

## 3. System Requirements

### 3.1 User Interface

**Jupyter Notebook Interface:**  
- Standard notebook with code and text cells  
- Users click "Run" to execute each step  
- Results appear below each code section  
- All charts and tables display in the notebook  

### 3.2 Software Requirements

**Required Python Packages:**  
- pandas >= 1.2.0 (for data handling)  
- numpy >= 1.19.0 (for calculations)  
- scikit-learn >= 0.24.0 (for ML models)  
- matplotlib >= 3.3.0 (for basic charts)  
- seaborn >= 0.11.0 (for better visualizations)  

### 3.3 Hardware Requirements

**Minimum Specs:**  
- 2GB RAM  
- 500MB free disk space  
- Standard processor (Intel/AMD)  
- No special graphics card needed  

---

## 4. System Features

### 4.1 Data Loading

**What it does:** Gets the heart disease data and loads it into the system

**Requirements:**  
- Load UCI heart disease dataset (303 patients)  
- Show basic info about the data (rows, columns)  
- Display first few rows to user  
- Handle download errors gracefully  

### 4.2 Data Analysis  

**What it does:** Explores the data to understand patterns

**Requirements:**  
- Show statistics for all features (mean, median, etc.)  
- Create charts showing data distribution  
- Display correlation between different features  
- Show how many patients have/don't have heart disease  

### 4.3 Data Preparation

**What it does:** Cleans and prepares data for ML models

**Requirements:**  
- Fill in any missing values  
- Convert text categories to numbers  
- Split data into training set (80%) and test set (20%)  
- Make sure both sets have similar proportions of heart disease cases  

### 4.4 Model Training

**What it does:** Teaches three different algorithms using the training data

**Requirements:**  
- Train Logistic Regression with default settings  
- Train Decision Tree with default settings  
- Train Random Forest with default settings  
- Complete all training within 2 minutes  

### 4.5 Model Testing

**What it does:** Tests how well each model works on new data

**Requirements:**  
- Test all models on the same test data  
- Calculate accuracy, precision, recall, and F1-score  
- Create confusion matrix for each model  
- All models should achieve at least 65% accuracy  

### 4.6 Results Display

**What it does:** Shows results in easy-to-understand format

**Requirements:**  
- Display performance table comparing all models  
- Show confusion matrix charts  
- Create bar charts comparing model performance  
- Provide simple explanation of which model works best  

---

## 5. Performance Requirements

**Speed Requirements:**  
- Complete notebook execution in under 5 minutes  
- Data loading within 1 minute  
- All model training within 2 minutes  
- Charts and results within 1 minute  

**Accuracy Requirements:**  
- All models must achieve minimum 65% accuracy  
- Results must be reproducible (same results each time)  
- Memory usage should not exceed 1GB  

---

## 6. Other Requirements

**Educational Requirements:**  
- Include clear explanations between code sections  
- Use simple language in all documentation  
- Provide interpretation of all results  
- Include warnings that this is for learning only, not medical use  

**Legal Requirements:**  
- State clearly this is not for medical diagnosis  
- Give credit to UCI for the dataset  
- Follow all open-source software licenses  
- Include disclaimer about educational use only  

**Data Requirements:**  
- Use only the provided UCI dataset  
- No personal or private medical information  
- All data processing happens locally on user's computer  
- No data is sent anywhere else  

---

## Success Criteria

The project is successful if:  
- All models achieve over 65% accuracy  
- Notebook runs completely without errors  
- Results are clear and easy to understand  
- Students can learn basic ML concepts from it  
- Code is well-documented and explained  
