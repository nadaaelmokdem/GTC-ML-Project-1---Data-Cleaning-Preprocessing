# 🏨 GTC ML Project 1 – Data Cleaning & Preprocessing

## 📌 Project Overview

This project is part of the **GTC Machine Learning Internship 2025**.

The main objective is to **clean and preprocess the raw hotel bookings dataset** so it is ready for building a machine learning model that predicts booking cancellations.

We are **not training a model here** — the focus is on preparing **high-quality input data**.

---

## 🎯 Business Problem

Last-minute booking cancellations significantly reduce hotel profitability.

By preparing a robust dataset, we enable predictive models to anticipate cancellations and help the hotel improve revenue management.

---

## 🛠️ Steps Completed

The project was divided into three main phases:

### **Phase 1: Exploratory Data Analysis (EDA)**

- Loaded and inspected the dataset (shape, info, summary statistics).
- Identified missing values and visualized them with heatmaps.
- Detected outliers in key numerical features (`adr`, `lead_time`).
- Documented main data quality issues.

### **Phase 2: Data Cleaning**

- Handled missing values with appropriate strategies:
    - `company`, `agent` → replaced with `"None"` or `0`
    - `country` → imputed with mode (most frequent)
    - `children` → imputed with median
- Removed duplicate rows.
- Capped extreme values in `adr` (>1000).
- Fixed data types (converted `reservation_status_date` to datetime).

### **Phase 3: Feature Engineering & Preprocessing**

- Created new features:
    - `total_guests` = adults + children + babies
    - `total_nights` = stays_in_weekend_nights + stays_in_week_nights
    - `is_family` = binary flag (1 if children or babies > 0)
- Encoded categorical variables:
    - One-Hot Encoding for `meal` and `market_segment`
    - Grouped rare `country` values into `"Other"`
- Removed data leakage columns (`reservation_status`, `reservation_status_date`).
- Split dataset into training (80%) and testing (20%).

---

## 📂 Project Structure

```
GTC-ML-Project-1/
│
├── hotel_bookings.csv              # Raw dataset
├── cleaned_hotel_bookings.csv      # Final cleaned dataset
├── project_notebook.ipynb          # Jupyter/Colab notebook with all steps
├── README.md                       # Project documentation

```

---

## 🚀 How to Run

1. Open the notebook (`project_notebook.ipynb`) in **Google Colab** or Jupyter.
2. Upload the dataset (`hotel_bookings.csv`).
3. Run all cells step by step (Steps 1 → 13).
4. The final cleaned dataset will be ready for modeling.

---

## ✅ Final Outcome

- A **machine-learning-ready dataset** that can be directly used for cancellation prediction models.
- Clean, consistent, and enriched data after handling missing values, duplicates, outliers, and categorical encodings.
- Dataset split into **train/test sets** to ensure reproducibility.

---

✨ **Prepared as part of the GTC ML Internship 2025 By Nada Elmokdem**