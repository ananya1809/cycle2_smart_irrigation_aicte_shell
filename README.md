# cycle2_smart_irrigation_aicte_shell
# 🌾 Smart Irrigation System - Multi-Label Classification Model

This project implements a **machine learning-based Smart Irrigation System** that predicts irrigation requirements for multiple agricultural parcels using sensor data. The model supports **multi-label classification** where irrigation decisions are made simultaneously for several zones (e.g., Parcel 0, Parcel 1, Parcel 2).

---

## 📦 Dataset
- Input features include sensor data such as:
  - `sensor_0` to `sensor_19` (environmental readings)
- Output labels:
  - `parcel_0`, `parcel_1`, `parcel_2` (whether to irrigate each parcel)

Ensure your dataset is in CSV format named `irrigation_machine.csv` and includes both features and target labels.

---

## 🔧 Technologies Used
- **Python 3.13.5**
- pandas, matplotlib, seaborn
- scikit-learn (RandomForestClassifier, MultiOutputClassifier)
- joblib (for model saving)

---

## 🧠 Model Overview

The project uses a **Random Forest classifier** wrapped in `MultiOutputClassifier` to simultaneously predict irrigation needs for multiple parcels.

### Steps:
1. Load and preprocess data
2. Normalize using `MinMaxScaler`
3. Train/test split (80/20)
4. Train `RandomForestClassifier` using custom hyperparameters
5. Evaluate performance using `classification_report`
6. Visualize parcel activation and pump status
7. Save trained model with `joblib`

---

## 🗂️ Project Structure

├── irrigation_machine.csv # Dataset file
├── Farm_Irrigation_System.pkl # Trained model (output)
├── week2_smart_irrigation_aicte_shell.ipynb # Source code 
├── README.md # Project documentation
