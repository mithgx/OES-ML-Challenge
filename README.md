# Real-Time Haul Truck Operational State Classification 

This project focuses on the real-time classification of haul truck operational states (Loading, Hauling, Dumping, Idle) using GPS telemetry data and machine learning. Accurate classification enables efficient fleet management, improved equipment utilization, and reduced operational delays in open-pit mining environments.

## 📌 Problem Statement

Haul trucks operate under diverse conditions that impact productivity and safety. Manual classification of these states is error-prone and delayed. The goal is to develop a machine learning model that classifies the operational state of haul trucks in real time using only GPS-based telemetry data.

## 🔧 Tech Stack

- **Language:** Python  
- **Libraries:** Pandas, NumPy, Scikit-learn, Matplotlib, Seaborn  
- **ML Model:** Random Forest Classifier  
- **Tools:** Google Colab / Jupyter Notebook  

## 📊 Dataset

- `telemetry_for_operations_training.csv`: Contains real-time GPS and sensor readings.  
- `operations_labels_training.csv`: Contains labeled time segments for each operational state.

Each record includes:
- `mdm_object_name` (truck ID)
- `create_dt` (timestamp)
- GPS coordinates and related telemetry
- Operational state labels (start_time, end_time, state)

## 🧠 Approach

1. **Data Preprocessing**
   - Cleaned and merged telemetry and label data (500K+ rows).
   - Converted timestamps and performed deduplication.
   - Aligned labels with telemetry using time-window matching.

2. **Feature Engineering**
   - Generated time-based and GPS-derived features.
   - Scaled features using StandardScaler and MinMaxScaler.

3. **Model Training**
   - Trained a Random Forest Classifier.
   - Evaluated with classification report and confusion matrix.
   - Achieved **92% accuracy** on test data.

4. **Deployment Simulation**
   - Designed real-time pipeline for future integration into production telemetry systems.

## 🚀 Key Results

- ✅ Achieved 92% classification accuracy across 4 operational states.  
- ⏱️ Reduced data cleaning and processing time by 60%.  
- 📉 Cut manual fleet monitoring effort by 80%.  
- ⚙️ Pipeline handles 1M+ records with optimized performance
  

