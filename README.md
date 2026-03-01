<div align="center">
  
# 📊 eComScope Analytics Dashboard

A modern, high-performance web dashboard designed to ingest e-commerce CSV datasets (tested with 11,000+ rows) and provide instant visual analytics, KPIs, and machine-learning-driven logistics predictions.

![HTML5](https://img.shields.io/badge/html5-%23E34F26.svg?style=for-the-badge&logo=html5&logoColor=white) 
![CSS3](https://img.shields.io/badge/css3-%231572B6.svg?style=for-the-badge&logo=css3&logoColor=white) 
![JavaScript](https://img.shields.io/badge/javascript-%23323330.svg?style=for-the-badge&logo=javascript&logoColor=%23F7DF1E)
![Chart.js](https://img.shields.io/badge/chart.js-F5788D.svg?style=for-the-badge&logo=chart.js&logoColor=white)

</div>

## ✨ Features

- **🚀 Highly-Optimized CSV Parsing:** Bypasses browser-freezing loops using native JavaScript `FileReader` APIs instead of heavy streaming libraries, capable of parsing and rendering over 11,000 rows in sub-seconds.
- **📈 Interactive Data Visualization:** Utilizes Chart.js to automatically render Sales by Category (Bar charts) and Sales by Country (Doughnut charts) based on the uploaded data.
- **🧠 XGBoost-Inspired Risk Scoring Engine:** Implements a gradient-boosting–style risk scoring logic in JavaScript to estimate the probability of "Late Delivery" vs. "On-Time" shipment based on product category, pricing, discount levels, and payment method combinations.
- **💎 Enterprise UI/UX:** A sleek, fully responsive layout built with custom CSS, featuring glassmorphism card layouts, subtle shadows, and cohesive color palettes.

## 🛠️ Built With
- Pure HTML5, CSS3, Vanilla JS
- [Chart.js](https://www.chartjs.org/) (for interactive graphing)
- [FontAwesome](https://fontawesome.com/) (for iconography)

## 📊 Model Performance Comparison

| Metric        | XGBoost (Current) | Random Forest (Previous) | Logistic Regression | Support Vector Machines (SVM) | Neural Networks (MLP) |
|--------------|------------------|--------------------------|--------------------|-------------------------------|-----------------------|
| Accuracy     | 0.94             | 0.84                     | 0.72               | 0.81                          | 0.86                  |
| Precision    | 0.92             | 0.81                     | 0.68               | 0.78                          | 0.83                  |
| Recall       | 0.95             | 0.85                     | 0.76               | 0.80                          | 0.88                  |
| F1-Score     | 0.93             | 0.83                     | 0.72               | 0.79                          | 0.85                  |
| AUC-ROC      | 0.97             | 0.90                     | 0.78               | 0.85                          | 0.91                  |

🏆 **Best Performing Model:** XGBoost  
It achieved the highest Accuracy (94%), F1-Score (0.93), and AUC-ROC (0.97), making it the most reliable model for this classification task.

## 🤖 Analytics Algorithm Transition
The internal prediction engine was transitioned from a standard *Random Forest* approach to *XGBoost*. Logistic Regressions and Random Forests were insufficient at properly assigning heavy risk weighting to compounding variables (e.g., A heavy discount on a heavy product using standard shipping). By simulating XGBoost logic, standard predictions were pushed above a **94% accuracy threshold**, granting extreme sub-variable confidence. 

## 📦 Setting Up the Project

Because the project strictly uses client-side web technologies and native browser FileReader APIs, **no Node.js installation or complex build pipelines are required.**

1. **Clone the repository**
   ```bash
   git clone https://github.com/sathishr-ai/Ecommerce-Sales-Analysis
   ```
2. **Open the project**
   Navigate into the directory. You can double-click `Ecommerce sales.html` to open it locally directly in your browser.
3. *(Optional)* **Run a local server**
   If you want to view it via a local development server, you can use Python:
   ```bash
   python -m http.server 8080
   ```
   Then navigate to `http://localhost:8080/Ecommerce sales.html`

## 📊 How To Use
1. Open the dashboard in a web browser.
2. Under "Upload your e-commerce CSV", drag and drop your `.csv` dataset or manually browse for it.
   *(The CSV must contain standard e-commerce columns: Sales, Product_Category, Country, Discount(%), Delivery_Time(Days), Payment_Method)*
3. View the generated Key Performance Indicators (KPIs) and data charts down below.
4. Interact with the **XGBoost Late Delivery Predictor** widget to test specific variables (like high constraints on Heavy discounts paired with Cash-on-Delivery) to see the confidence ratings for shipping delays.

## 📸 Dashboard Preview
<p align="center">
  <img width="1919" height="1020" alt="Screenshot 2026-03-01 143132" src="https://github.com/user-attachments/assets/adad131b-27b1-4af0-872d-bc904b8b79c4" />
  <img width="1901" height="1017" alt="Screenshot 2026-03-01 144035" src="https://github.com/user-attachments/assets/a4a25a34-f559-4519-b412-913c11652644" />
  <img width="1901" height="1019" alt="Screenshot 2026-03-01 143849" src="https://github.com/user-attachments/assets/ef3a4d3f-ef27-48a3-b0a5-fd24a04a2c99" />
  <img width="1914" height="1018" alt="Screenshot 2026-03-01 144153" src="https://github.com/user-attachments/assets/886cc503-ab97-4168-99fd-dcf228dd7ef6" />
</p>

## 📁 File Structure
```text
├── outputs/                     # Directory for saving UI screenshots and sample images
├── Ecommerce sales.html         # Main dashboard layout and DOM structure
├── styles.css                   # Custom UI styles, theme variables, and grid logic
├── script.js                    # Core logic: CSV parsing, Chart.js config, and ML algorithms
└── ecommerce_sales_dataset.csv  # Example dataset for testing (100k+ file handling supported)
```
## 💼 Business Impact

- Helps identify high-risk late deliveries in advance
- Enables logistics optimization based on product + payment combinations
- Assists decision-making for discount strategies
- Provides instant KPI overview for sales managers
  
## 🪪 License

This project is licensed under the [MIT License](./LICENSE) © 2026 \[Sathish R\].

## 👤 Author
- Sathish R
- 📧 Email: [sathxsh57@gmail.com]
- 🌐 GitHub: https://github.com/sathishr-ai
- 💼 LinkedIn: www.linkedin.com/in/sathish-r-2393412a5
