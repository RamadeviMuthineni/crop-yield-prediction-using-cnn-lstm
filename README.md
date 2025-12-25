 🌾 Crop Yield Prediction using CNN–LSTM

Project Overview

This project predicts crop yield by combining spatial features extracted using a convolutional Neural Network (CNN) and temporal features captured using a Long Short-Term Memory (LSTM) network.
The hybrid CNN–LSTM model improves prediction accuracy by learning both image-based patterns and time-series agricultural data.

 Problem Statement

Accurate crop yield prediction is crucial for:

* Agricultural planning
* Resource optimization
* Reducing economic losses

Traditional statistical models fail to capture complex spatial and temporal relationships.
This project addresses that limitation using **deep learning**.


 Solution Approach

A **hybrid deep learning architecture** is used:

* **CNN** → Extracts spatial features
* **LSTM** → Learns temporal dependencies
* **Fully Connected Layer** → Predicts crop yield

---

 Project Structure

```
crop-yield-prediction-using-cnn-lstm/
│
├── Preprocessing.ipynb        # Data cleaning, encoding, scaling
├── Untitled.ipynb             # Model training & evaluation
├── final_crop.csv             # Processed dataset
│
├── cnn_model.pth              # Trained CNN model
├── cnn_model_weights.pth      # CNN weights
├── hybrid_model.pth           # CNN–LSTM hybrid model
├── hybrid_model_weights.pth   # Hybrid model weights
│
├── scaler.pkl                 # Feature scaler
├── scaler_target.pkl          # Target variable scaler
├── label_encoders.pkl         # Encoded categorical features
│
├── templates/                 # UI templates (if applicable)
└── README.md                  # Project documentation
```

---

 Working Process

### 1️⃣ Data Collection

The dataset (`final_crop.csv`) contains:

* Crop type
* Weather parameters (rainfall, temperature, etc.)
* Soil and region details
* Historical yield values

---

### 2️⃣ Data Preprocessing

Performed in **Preprocessing.ipynb**:

* Removed missing and inconsistent values
* Encoded categorical variables using **Label Encoding**
* Normalized numerical features using **StandardScaler**
* Scaled target variable for better model convergence

Saved preprocessing objects:

* `label_encoders.pkl`
* `scaler.pkl`
* `scaler_target.pkl`

---

### 3️⃣ CNN Model (Spatial Feature Extraction)

* CNN processes feature matrices to extract **spatial patterns**
* Learns relationships between crop, soil, and environmental attributes
* Trained CNN model stored as:

  * `cnn_model.pth`
  * `cnn_model_weights.pth`

---

### 4️⃣ LSTM Model (Temporal Learning)

* LSTM captures **time-dependent patterns** in agricultural data
* Learns seasonal and climatic trends affecting yield
* Handles long-term dependencies efficiently

---

### 5️⃣ Hybrid CNN–LSTM Model

* CNN output is passed as input to LSTM
* Combined model learns **both spatial and temporal features**
* Final prediction generated through dense layers

Saved model:

* `hybrid_model.pth`
* `hybrid_model_weights.pth`

---

### 6️⃣ Model Training & Evaluation

* Loss function: Mean Squared Error (MSE)
* Optimizer: Adam
* Evaluation metrics:

  * RMSE
  * MAE
* Hybrid model outperformed individual CNN model

---

### 7️⃣ Prediction

* New input data is:

  * Encoded using saved label encoders
  * Scaled using saved scalers
* Hybrid model predicts crop yield
* Output is inverse-transformed to original scale

---

## 🧪 Technologies Used

* **Python**
* **PyTorch**
* **NumPy, Pandas**
* **Scikit-learn**
* **Matplotlib**
* **Jupyter Notebook**

---

## 📊 Key Highlights

* Hybrid CNN–LSTM architecture
* Handles complex agricultural data
* Improved prediction accuracy over traditional models
* Scalable for different crops and regions
## 📬 Contact

For any queries or collaboration:

- Name: Rama Devi Muthineni
- Phone no: 8019116518 
- Email: ramadevimuthineni76@gmail.com
