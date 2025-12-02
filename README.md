 # **Wine Quality Predictor – Product Overview**
*Predicting the quality of Portuguese "Vinho Verde" red wine using machine learning.*

---

## **📌 Product Summary**
This product leverages **machine learning** to predict the **quality of red wine** based on physicochemical properties (e.g., acidity, alcohol content, sulphates). It helps **wineries, sommeliers, and wine enthusiasts** assess wine quality **without expensive lab testing**, enabling data-driven decisions in production, purchasing, or tasting.

### **🔍 Key Features**
✅ **Predicts wine quality** (Low, Medium, High) with **81% accuracy**
✅ **Uses 8 key wine attributes** (e.g., alcohol, sulphates, density)
✅ **Trained on 1,599 real red wine samples** from Portugal
✅ **Optimized with Random Forest** (best-performing model)
✅ **Easy-to-interpret results** for non-technical users

---

## **📊 How It Works**
### **1. Input Data (Wine Characteristics)**
The model analyzes **8 key features** of red wine:

| Feature               | Description                          | Example Range       |
|-----------------------|--------------------------------------|---------------------|
| **Volatile Acidity**  | Vinegar-like taste (lower = better)  | 0.12 – 1.58         |
| **Citric Acid**       | Adds freshness (higher = better)     | 0.0 – 1.0           |
| **Residual Sugar**    | Sweetness level                      | 0.9 – 15.5 g/dm³    |
| **Chlorides**         | Saltiness                            | 0.01 – 0.61 g/dm³   |
| **Total Sulfur Dioxide** | Preservative (lower = better)      | 6 – 289 mg/dm³      |
| **Density**           | Alcohol & sugar content indicator   | 0.99 – 1.00 g/cm³   |
| **pH**                | Acidity level (3-4 is typical)       | 2.74 – 4.01         |
| **Sulphates**         | Preservative (higher = better)       | 0.33 – 2.0 g/dm³    |
| **Alcohol**           | Alcohol percentage                   | 8.4% – 14.9%        |

### **2. Quality Prediction**
The model classifies wine into **3 quality categories**:
- **🟢 High Quality (7-10)** – Premium wines
- **🟡 Medium Quality (5-6)** – Standard wines
- **🔴 Low Quality (3-4)** – Below-average wines

### **3. Model Performance**
| Model               | Accuracy | Best For                     |
|---------------------|----------|------------------------------|
| **Random Forest**   | **83%**  | Highest accuracy             |
| **Logistic Regression** | 73%   | Simple, interpretable        |
| **Decision Tree**   | 68%      | Quick decisions             |

**Confusion Matrix (Random Forest):**
| Actual \ Predicted | Low | Medium | High |
|--------------------|-----|--------|------|
| **Low**            | 184 | 50     | 0    |
| **Medium**         | 45  | 244    | 0    |
| **High**           | 1   | 4      | 0    |

*(Note: High-quality wines are rare in the dataset, affecting predictions.)*

---

## **📈 Key Insights from Data**
### **What Affects Wine Quality?**
✔ **Alcohol (10.4% avg)** – **Strongest positive impact** (higher alcohol = better quality)
✔ **Sulphates (0.66 g/dm³ avg)** – Helps preservation & taste
✔ **Volatile Acidity (0.53 avg)** – Too high = sour/vinegar taste (bad)
❌ **pH (3.31 avg)** – Less impact than expected (correlates with acidity)
❌ **Residual Sugar** – Minimal effect on quality

### **Data Distribution**
- **Most wines are medium quality (6/10 avg)**
- **High-quality wines are rare (only 1.1%)**
- **No missing data** – Clean and ready for predictions

---

## **🚀 Use Cases**
### **For Wineries & Producers**
✅ **Optimize production** – Adjust acidity, alcohol, or sulphates for better quality
✅ **Cost reduction** – Avoid expensive lab tests by predicting quality early
✅ **Batch consistency** – Ensure uniform quality across productions

### **For Sommeliers & Retailers**
✅ **Wine selection** – Quickly assess quality before purchasing
✅ **Customer recommendations** – Suggest higher-quality wines based on data
✅ **Pricing strategy** – Justify premium pricing for high-quality wines

### **For Wine Enthusiasts**
✅ **Smart purchases** – Check expected quality before buying
✅ **Home winemaking** – Improve DIY wine quality with data insights

---

## **🛠️ Technical Details (For Developers)**
### **Dataset**
- **Source:** [Kaggle – Red Wine Quality (Cortez et al., 2009)](https://www.kaggle.com/datasets/uciml/red-wine-quality-cortez-et-al-2009)
- **Samples:** 1,599 red wines (Portuguese "Vinho Verde")
- **Features:** 11 physicochemical properties + quality score (3-8)

### **Preprocessing**
✔ **Feature selection** – Removed redundant features (e.g., `fixed acidity`, `pH`)
✔ **Normalization** – Scaled data for better model performance
✔ **Quality categorization** – Grouped into **Low/Medium/High**

### **Best Model: Random Forest**
- **Accuracy:** 83% (10-fold cross-validation)
- **Why?** Handles non-linear relationships well
- **Alternative:** Logistic Regression (73%) for simplicity

### **Limitations**
⚠ **Class imbalance** – Few high-quality wines (affects predictions)
⚠ **Subjective quality scores** – Based on human tastings (not lab-measured)
⚠ **Only red wine** – White wine requires a separate model, the data is available in the kaggle to do so as well. 
The point of this exercise is the fact that this demonstrate there's a chance to have this type of forecasting even for subjective attributes.

---

## **🔮 Future Improvements**
🔹 **More data** – Include white wines & other regions
🔹 **Hyperparameter tuning** – Boost accuracy further
🔹 **Real-time API** – Deploy as a web/mobile app
🔹 **Explainable AI** – Show why a wine is predicted as high/low quality

---
**🍷 Cheers to data-driven wine tasting!** 🍷
