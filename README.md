# Gamma-Hadron Signal classification

### **Project Overview**
Space telescopes pick up a lot of "noise" from the sky. This project uses Machine Learning to help a telescope tell the difference between real **Gamma particles** (the signal we want) and **Hadronic showers** (the background noise).

---

### **Core Objectives**
* **Find the Signal:** Build and experiment with different classification Machine Learning models to automatically spot Gamma particles in a massive dataset.
* **Evaluate Models:** Test and compare various algorithms to identify the models with the highest **F1-score** and **Accuracy** for the most reliable results.

---

### **Technical Stack & Methodology**
* **Tools:** Python: Pandas, Scikit-learn, Google Colab.
* **The Process:**
    1. **Data Prep:** Cleaned up a famous scientific dataset (MAGIC Gamma Telescope).
    2. **Exploratory Data Analysis (EDA):** * Built **Histograms** and **Box Plots** for every feature to visualize how they relate to the target (Gamma vs. Hadron).
        * Identified "key features" (like `fLength` and `fSize`) that showed the strongest correlation with the target particles.
        * **Multicollinearity Check:** Created a **Correlation Heatmap** to spot highly correlated variables. 
    3. **Data Engineering:** 
    * **Encoding:** Converted text labels into numbers for the models to process.
    * **Scaling:** Normalized the data so that large numbers didn't overwhelm the smaller ones.
    * **Fixing Imbalance:** Used **Random Over-Sampling** to balance the dataset, ensuring the models learned from both Gamma and Hadron particles equally.
    3. **Modeling:** Built and compared multiple models, including **KNN, Naive Bayes, Logistic Regression, and SVM**, to find the best signal-to-noise filter.
    4. **Checking Results:** Used a "Classification Report" to see exactly how many times the model was right or wrong.
    5. **Evaluation:** Selected the top-performing models by comparing **Accuracy** and **F1-Score** to ensure scientific reliability.

---

### **Key Insights**
**Winning Model:** The SVM classifier achieved an **86% accuracy** rate, proving to be a strong tool for this type of data.
* **High Reliability:** By focusing on the **F1-score** (highest for SVM: 0.85), I ensured the model was balanced and didn't just guess, making it more dependable for scientists.
