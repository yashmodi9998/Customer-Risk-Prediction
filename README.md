# Customer Risk Prediction

## Overview

This project aims to predict the risk of default payment for online purchase orders using a dataset containing 30,000 orders with 44 attributes. The objective is to classify orders into two categories: high risk (`yes`) and low risk (`no`).

## Table of Contents

- [Dataset Description](#dataset-description)
- [Data Preprocessing](#data-preprocessing)
- [Classification Method](#classification-method)
- [Solutions and Findings](#solutions-and-findings)
- [Usage](#usage)

## Dataset Description

The dataset utilized in this project is a tab-separated file (`risk-train.txt`) with 30,000 online purchase orders. The key target attribute is `CLASS`, which indicates the risk level of an order. The dataset includes various attributes related to customer information, order details, and historical payment behavior.

### Key Attributes

- `ORDER_ID`: Unique identifier for each order.
- `B_BIRTHDATE`: Customer's birth date.
- `DATE_LORDER`: Date of the last order.
- `CLASS`: Target variable indicating risk (high/low).

## Data Preprocessing

Data preprocessing steps include:

1. Replacing missing values represented by '?' with NaN.
2. Dropping rows with missing critical fields (`ORDER_ID`, `CLASS`).
3. Converting date fields to appropriate datetime formats.
4. Feature engineering to derive age and days since the last order.
5. Filling missing numerical and categorical values with appropriate defaults.
6. One-hot encoding of categorical variables.

## Classification Method

A **Cost-Sensitive Decision Tree Classifier** is implemented to address class imbalance in the dataset. The classifier is optimized for minimizing false negatives (FN) to ensure high recall, which is crucial for accurately identifying high-risk orders.

## Solutions and Findings

Significant recall scores were achieved after training the model, indicating effectiveness in identifying high-risk orders. Confusion matrices and various evaluation metrics were used to analyze model performance.

### Performance Metrics

- **Recall**: Measures the ability of the model to identify positive instances (high-risk orders).
- **Cost**: Measures the Cost of the model.

## Usage

To run this project, ensure the following dependencies are installed:

- Python 3.x
- pandas
- numpy
- scikit-learn

Clone the repository and run the main script to preprocess the data, train the model, and evaluate its performance.

```bash
git clone <https://github.com/yashmodi9998/Customer-Risk-Prediction>
cd <Customer-Risk-Prediction>
python main.py
```
