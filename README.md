#  Earthquake Damage Prediction (PRCP-1015)

*A 5-Day Machine Learning Project using the DrivenData PRCP-1015 Dataset*  

---

#  **Team Members**
- **Nandhakumar (Team Lead)**
- **Suvaathii**
- **Swetha**
- **Rehana**
---

#  **Project Objective**
This project predicts the **damage grade of buildings** affected by the  
**2015 Gorkha Earthquake (Nepal)** using machine learning.

The target variable:

| Damage Grade | Meaning |
|--------------|----------|
| **1** | Low damage |
| **2** | Medium damage |
| **3** | Heavy/Complete destruction |

Dataset Link (official):  
https://d3ilbtxij3aepc.cloudfront.net/projects/CDS-Capstone-Projects/PRCP-1015-EquakeDamagePred.zip

---

#  **5-Day Project Timeline**

## **Day 1 – Dataset Setup + EDA (Part 1)**
- Load & merge data  
- Summary statistics  
- Target distribution  
- Numeric and categorical feature exploration  
- Geo-level insights  

## **Day 2 – Deep EDA (Part 2) + Feature Engineering**
- Outlier detection & IQR capping  
- One-hot encoding  
- Frequency encoding (geo-levels)  
- Binary flag conversion  
- New features added:
  - floors_to_height_ratio  
  - area_to_height_ratio  
  - total_superstructures  
  - secondary_use_count  
  - age_buckets  

## **Day 3 – Machine Learning Models**
We trained **6 models**:

| Model | Status |
|-------|--------|
| Logistic Regression | ✔ Baseline |
| Decision Tree | ✔ |
| Random Forest | ✔ |
| XGBoost | ✔ |
| LightGBM | ✔ |
| **CatBoost** |  **Best model** |

Evaluation Metrics:
- Accuracy  
- Macro F1 Score (important due to class imbalance)

## **Day 4 – Reports**
- Full EDA Report  
- Predictive Model Report  
- Model Comparison Table  
- Seismologist Recommendations  
- Challenges and solutions  

## **Day 5 – Finalization**
- Notebook cleanup  
- README creation  
- Submission packaging  

---

#  **1. Exploratory Data Analysis (EDA)**

## **Dataset Insights**
- 260,601 buildings  
- 39 features + 1 target  
- Structural + material + geographic information  

## **Key EDA Findings**
- **Material types heavily influence damage**
  - Mud, Adobe, Stone → high damage  
  - Reinforced Concrete (Engineered) → low damage  
- **Old and tall buildings show severe destruction**
- **Damage patterns differ by geographic cluster**
- **Secondary-use buildings (schools, rentals, industry) require priority reinforcement**

---

#  **2. Data Preprocessing**

### ✔ Outlier handling (IQR method)  
### ✔ One-hot encoding for low-cardinality features  
### ✔ Frequency encoding for geo-levels (high-cardinality)  
### ✔ Binary conversion for yes/no flags  
### ✔ Feature engineering to improve model performance  
### ✔ Standard scaling for numeric features  

---

#  **3. Machine Learning Models**

## **Models Used**
- Logistic Regression  
- Decision Tree Classifier  
- Random Forest  
- XGBoost  
- LightGBM  
- **CatBoost (Best Performer)**  

## **Best Model: CatBoost**
- Handles categorical data well  
- Robust to class imbalance  
- Best Accuracy & Macro F1 Score  

---

#  **4. Recommendations for Seismologists**

### **Improve Building Materials**
- Avoid mud/adobe/stone  
- Promote engineered RC structures  
- Use proper curing & load distribution  

### **Improve Building Stability**
- Lower height-to-area ratios  
- Avoid extremely tall narrow structures  

### **Region-Based Mitigation**
- Strengthen codes in high-damage geo clusters  
- Target retrofitting for old buildings  

### **Prioritize Secondary Use Buildings**
- Schools  
- Hospitals  
- Rental & commercial spaces  
- Industrial units  

---

#  **5. Challenges & Solutions**

| Challenge | Solution |
|----------|----------|
| Outliers in age & height | IQR capping |
| High-cardinality geo features | Frequency encoding |
| Class imbalance | Stratified train-test split + Macro F1 |
| Multicollinearity | Tree-based models |
| Very large dataset | Efficient encoding + optimized models |

---

# **Conclusion**
This project delivers:
- A full EDA report  
- Complete preprocessing pipeline  
- Multiple ML models  
- Comparison table  
- Seismologist recommendations  
- Challenges & solutions  

The final model (**CatBoost**) performs best in predicting ordinal earthquake damage (1, 2, 3).

---

