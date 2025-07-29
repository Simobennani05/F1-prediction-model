
# 🏎️ Formula 1 Race Prediction  
Predicting Formula 1 race results using machine learning  

## 📌 Project Overview  
This project focuses on predicting Formula 1 race standings by leveraging:  
- **Qualifying Performance**  
- **Historical Race Data**  
- **Starting Grid Position**  

These inputs are used to estimate total race time for the **2025 Australian Grand Prix**. The model is built using **Python**, the **FastF1 API**, and **Scikit-Learn**, with an emphasis on predicting lap times.

---

## 📊 Data Collection (FastF1 API)  
Historical data from the **2024 season** was collected using the **FastF1 API**, including:  
- **Lap times** from the 2024 Australian Grand Prix  
- **Grid positions** from the same race  
- **Simulated qualifying times** for the 2025 race to test the model  

---

## 🧠 Feature Engineering  
To predict lap times for 2025, the following features were used:  
- **2024 Lap Times** – Baseline performance for each driver  
- **2025 Qualifying Times** – Proxy for current form  
- **Starting Grid Position** – Impacts overtaking difficulty and race dynamics  

Variables like **fuel loads**, **pit stops**, and **weather conditions** were **excluded in this version**, but are strong candidates for future iterations.

---

## ⚙️ Model Selection  
The model chosen was **Gradient Boosting Regressor** from Scikit-Learn due to its:  
- Suitability for **tabular, non-linear data**  
- Ability to model **complex relationships**  
- Robustness with **limited datasets** (critical in F1 context)  

---

## 📈 Model Evaluation  
Performance was assessed using **Mean Absolute Error (MAE)**:  
- **MAE:** *3.47 seconds per lap*  
While reasonable for a first version, improving lap-level accuracy is essential given F1's high precision demands.

---

## 🚧 Challenges & Limitations  
- **New Driver Data Gaps** – No lap history for drivers debuting in 2025  
- **Prediction Error (3.47s)** – Acceptable for proof of concept but needs refinement  
- **Missing Race-Day Variables** – Tire wear, weather, pit strategy, etc., were not included  


