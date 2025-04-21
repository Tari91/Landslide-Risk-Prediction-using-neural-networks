🧠 Landslide Risk Prediction using Neural Networks
This project demonstrates how to build and train a neural network for predicting landslide risk using a synthetic dataset generated to simulate real-world geospatial and environmental data.

📁 File Overview
landslide_prediction.py – Main Python script containing:

Synthetic data generation

Neural network model definition and training

Risk prediction and evaluation

Data export to Excel

synthetic_landslide_data_with_predictions.xlsx – Output Excel file with synthetic data and model predictions

🔧 Technologies Used
Python 3.x

TensorFlow / Keras

scikit-learn

pandas

matplotlib

🧪 Features in Dataset

Feature	Description
elevation	Elevation in meters (0–3000 m)
slope	Slope in degrees (0–90°)
rainfall	Rainfall in mm (0–500 mm)
soil_type	Categorical feature (integer: 0–4)
vegetation_index	NDVI-like vegetation index (0 to 1)
risk	True risk label (1 = high risk, 0 = low risk)
predicted_risk	Predicted label from neural network (1 = high risk, 0 = low risk)
risk_probability	Probability output from the neural network (0–1)
📊 Risk Label Logic (Synthetic)
The label risk is set to 1 (high risk) if at least two of the following conditions are true:

Slope > 30°

Rainfall > 300 mm

Vegetation index < 0.3
Otherwise, it is 0 (low risk).

🧠 Model Architecture
A simple feedforward neural network:

Input Layer (based on number of features)

Dense Layer (16 units, ReLU)

Dense Layer (8 units, ReLU)

Output Layer (1 unit, Sigmoid)

📈 Output
Prints training and validation accuracy

Shows plot of training history

Saves Excel file with predictions:

Copy
Edit
synthetic_landslide_data_with_predictions.xlsx
▶️ How to Run
1. Install Dependencies
bash
Copy
Edit
pip install numpy pandas matplotlib scikit-learn tensorflow openpyxl
2. Run the Script
bash
Copy
Edit
python landslide_prediction.py
3. Output Files
Check the generated Excel file in the project directory.

🚀 Future Work
Replace synthetic data with real-world DEM, rainfall, and NDVI data

Use geospatial libraries like rasterio or geopandas

Deploy as a web app for interactive risk mapping

👨‍💻 Author
Tarinabo  geosoftconsultingltd@gmail.com 
