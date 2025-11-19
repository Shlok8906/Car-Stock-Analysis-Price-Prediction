# 🚗 Used Car Price Prediction — Machine Learning Project

This project performs **data cleaning**, **exploratory data analysis (EDA)**, **feature engineering**, and **machine learning model development** to build a highly accurate used car price prediction system.  
It includes a fully cleaned dataset, visualizations, prediction pipeline, and reports (text + graphs).

---

# 📌 Project Overview

The used car market is highly dynamic, with prices influenced by numerous variables including engine capacity, power, mileage, age, fuel type, transmission, and overall vehicle specifications.  
This project helps:

- Identify **which features impact car prices the most**
- Perform deep **EDA** with graphs and insights
- Build a **Random Forest model** for accurate predictions
- Understand the pricing behavior of different makes/models
- Create a **user input prediction system**
- Provide a complete end-to-end ML pipeline

---

# 📁 Dataset Description

This project uses a dataset containing structural, mechanical, and usage-related attributes of used cars.

### **Columns Included**

### **Feature Types**
- **Numerical Features:**  
  Price, Year, Kilometer, Engine, Max Power, Max Torque, Length, Width, Height, Seating Capacity, Fuel Tank Capacity  
- **Categorical Features:**  
  Make, Model, Fuel Type, Transmission, Location, Owner, Seller Type, Color, Drivetrain  

---

# 🧼 Data Cleaning & Preprocessing

The following steps were applied to clean the dataset:

### ✔ Missing Value Handling
- Rows with missing **Price** were removed.
- Missing values in Fuel Type, Transmission, Owner, and Color were filled with `"Unknown"`.

### ✔ Standardizing Numerical Columns
- Cleaned Engine, Max Power, Max Torque (converted to numeric values).
- Standardized unit formats (mm, cc, bhp).
- Converted Mileage, Dimensions, Seating Capacity to proper numeric formats.

### ✔ Categorical Cleaning
- Unified inconsistent category labels (e.g., `"manual"` → `"Manual"`).
- Normalized Make/Model names for consistency.

### ✔ Outlier Removal
- Removed unrealistic prices (< ₹50,000 or > ₹40,00,000).
- Removed unusable entries with missing or corrupted mechanical specifications.

### ✔ Encoding
- Applied **One-Hot Encoding** to categorical features.
- Ensured consistent feature alignment during prediction.

---

# 📊 Exploratory Data Analysis (EDA)

Key insights discovered during EDA:

---

## 🔹 **1. Price Distribution**
- Price is **heavily right-skewed**.
- Log transformation normalizes price and improves prediction accuracy.

## 🔹 **2. Correlation Insights**
Strong positive correlations with Price:
- Engine
- Max Power
- Fuel Tank Capacity
- Width, Length, Height

Negative correlations with Price:
- Kilometer Driven  
- Transmission (encoded)

Multicollinearity identified:
- Engine ↔ Max Power  
- Length ↔ Width ↔ Fuel Tank Capacity  

## 🔹 **3. Scatter Plot Findings**
- Price increases significantly with **Max Power**.
- Larger **Engine CC** cars are consistently more expensive.
- Cars with larger **Fuel Tank Capacity** tend to be SUVs/high-end vehicles.

## 🔹 **4. Categorical Insights**
- **Automatic > Manual** in pricing.
- **Diesel > Petrol** median price.
- **First-owner vehicles** command significantly higher prices.
- Luxury brands cluster at the high-price end.

## 🔹 **5. Make & Model Trends**
- Maruti Suzuki and Hyundai dominate in volume.
- Mercedes, BMW, Audi form the luxury clusters.
- Make alone is not a strong predictor — mechanical features matter more.

---

