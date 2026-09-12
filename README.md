# 🌊 Uncertainty Analysis of Flood Susceptibility Mapping of the West Coast of India

## 📌 Project Overview

This project develops a **Flood Susceptibility Mapping (FSM)** system for the West Coast of India using **geospatial analysis, Google Earth Engine, and machine learning**.

The system integrates multiple geospatial conditioning factors to identify areas with different levels of flood susceptibility. A **Random Forest (RF)** machine learning model is used to generate flood susceptibility predictions.

In addition to susceptibility mapping, the project incorporates **uncertainty and calibration analysis** to understand the reliability of model predictions. The model performance is evaluated using **ROC-AUC**, while the final results are presented through interactive geospatial visualizations.

The project is implemented using **Python, Google Earth Engine, Geemap, and Google Colab**.

---

## 🎯 Objectives

* Identify areas with different levels of flood susceptibility.
* Integrate multiple geospatial conditioning factors for flood analysis.
* Apply a Random Forest machine learning model for flood susceptibility prediction.
* Analyze the contribution of individual geospatial variables.
* Quantify prediction uncertainty.
* Perform conformal calibration to assess prediction reliability.
* Evaluate model performance using ROC curves and AUC.
* Generate interactive flood susceptibility maps.
* Provide a geospatial framework for understanding flood-prone regions.

---

## 🗺️ Study Area

The study focuses on the **West Coast region of India**, covering selected coastal areas and districts.

The study region is analyzed using Google Earth Engine to process and combine multiple spatial datasets.

The workflow can be applied at the **district level**, allowing flood susceptibility to be analyzed for individual districts within the study region.

---

## 🛠️ Technologies & Tools

### Programming

* Python
* NumPy
* Pandas
* Matplotlib

### Geospatial Technologies

* Google Earth Engine
* Geemap
* Remote Sensing
* GIS
* Google Colab

### Machine Learning

* Random Forest

### Model Evaluation

* ROC Curve
* ROC-AUC
* Variable Importance

### Uncertainty Analysis

* Bernoulli Variance
* Margin Confidence
* Bootstrap Random Forest Variance
* Conformal Prediction / Calibration

---

## 🌍 Geospatial Conditioning Factors

The model uses **17 geospatial conditioning variables** to analyze flood susceptibility.

These variables represent different environmental and terrain characteristics that can influence flood occurrence and susceptibility.

The input variables are processed and combined within the Google Earth Engine workflow before being used for machine learning.

---

## 🔬 Methodology

The overall methodology consists of the following stages:

```text
Study Area Selection
        ↓
Geospatial Data Collection
        ↓
Preprocessing & Data Preparation
        ↓
Selection of 17 Conditioning Factors
        ↓
Flood Inventory / Training Data
        ↓
Random Forest Model
        ↓
Flood Susceptibility Prediction
        ↓
Variable Importance Analysis
        ↓
Uncertainty Analysis
        ↓
Conformal Calibration
        ↓
ROC-AUC Evaluation
        ↓
Interactive Flood Susceptibility Map
```

---

## 📊 Project Workflow

### 1. Define Study Area

The required coastal study region is defined using geographic boundaries and district-level regions.

### 2. Collect Geospatial Data

Multiple geospatial datasets are accessed and processed using **Google Earth Engine**.

### 3. Data Preprocessing

The input datasets are prepared, aligned, and combined into a common analysis framework.

### 4. Conditioning Factor Preparation

A total of **17 geospatial conditioning factors** are prepared as model inputs.

### 5. Random Forest Classification

A **Random Forest classifier** is trained using the prepared training data.

The trained model is then used to predict flood susceptibility for the selected study region.

### 6. Flood Susceptibility Mapping

The Random Forest predictions are converted into different susceptibility levels:

* 🟢 **Low Susceptibility**
* 🟡 **Medium Susceptibility**
* 🔴 **High Susceptibility**

### 7. Variable Importance Analysis

Random Forest variable importance is analyzed to identify which conditioning factors contribute more strongly to the model predictions.

### 8. Uncertainty Analysis

Uncertainty analysis is performed to understand the confidence and reliability of flood susceptibility predictions.

The project considers:

* Bernoulli variance
* Margin-based confidence
* Bootstrap Random Forest variance
* Conformal prediction/calibration

### 9. Model Evaluation

The model is evaluated using the **Receiver Operating Characteristic (ROC) curve** and **Area Under the Curve (AUC)**.

### 10. Interactive Visualization

The final flood susceptibility results are visualized using **Geemap** and Google Earth Engine interactive maps.

---

## 🧠 Random Forest Model

Random Forest is used as the primary machine learning algorithm for flood susceptibility prediction.

The model combines the information from the 17 conditioning factors and learns patterns from the available flood-related training data.

The Random Forest approach also provides **variable importance information**, which helps identify the relative contribution of the input factors.

---

## 🔎 Uncertainty Analysis

A major component of this project is the analysis of uncertainty associated with flood susceptibility predictions.

### Bernoulli Variance

Bernoulli variance is used to represent uncertainty associated with probabilistic classification outcomes.

### Margin Confidence

The difference between the predicted class probabilities is used to estimate the confidence of a prediction.

A larger margin indicates greater separation between competing classes, while a smaller margin indicates greater uncertainty.

### Bootstrap Random Forest Variance

Multiple bootstrap samples are used to train Random Forest models and examine the variation between predictions.

This helps estimate the stability of the model predictions.

### Conformal Prediction

Conformal methods are used to calibrate prediction confidence and provide a reliability-oriented interpretation of the model outputs.

---

## 📈 Model Evaluation

### ROC Curve & AUC

The **ROC curve** is used to evaluate the ability of the Random Forest model to distinguish between flood-related classes.

The **Area Under the Curve (AUC)** provides a summary measure of model discrimination performance.

A higher AUC generally indicates better separation between the evaluated classes.

---

## 📊 Project Results

### 1. Study Area & Input Variables

Shows the selected study region and the geospatial variables used in the analysis.

![Study Area & Input Variables](01-study-area.png)

---

### 2. Random Forest Variable Importance

Shows the relative importance of the conditioning factors used by the Random Forest model.

![Random Forest Variable Importance](02-rf-variable-importance.png)

---

### 3. Flood Susceptibility Area Distribution

Shows the distribution of the study area across the different flood susceptibility classes.

![Flood Susceptibility Area Distribution](03-fsm-area-distribution.png)

---

### 4. Conformal Calibration Analysis

Shows the conformal calibration results used to analyze the reliability of the model predictions.

![Conformal Calibration](04-conformal-calibration.png)

---

### 5. ROC-AUC Model Evaluation

Shows the ROC curve and AUC obtained during model evaluation.

![ROC Curve](05-roc-curve.png)

---

### 6. Interactive Flood Susceptibility Map

The final susceptibility results are visualized through an interactive Geemap map.

![Interactive Geemap](06-interactive-geemap.png)

---

## 🗺️ Flood Susceptibility Classes

The generated susceptibility map represents three major classes:

| Class     | Description                                          |
| --------- | ---------------------------------------------------- |
| 🟢 Low    | Areas with comparatively lower flood susceptibility  |
| 🟡 Medium | Areas with moderate flood susceptibility             |
| 🔴 High   | Areas with comparatively higher flood susceptibility |

---

## ✨ Key Features

* 🌊 Flood susceptibility mapping for the West Coast of India
* 🛰️ Google Earth Engine-based geospatial processing
* 🌍 District-level analysis
* 📊 17 geospatial conditioning factors
* 🌲 Random Forest-based prediction
* 🔎 Random Forest variable importance analysis
* 📉 ROC curve and AUC evaluation
* 📐 Prediction uncertainty analysis
* 🔄 Bootstrap-based Random Forest uncertainty
* 🎯 Conformal calibration
* 🗺️ Interactive Geemap visualization
* 📍 Low, Medium, and High susceptibility classification

---

## 📁 Project Structure

```text
FloodSight-UQ/
│
├── SAMUDRA_UQ.ipynb
│
├── 01-study-area.png
├── 02-rf-variable-importance.png
├── 03-fsm-area-distribution.png
├── 04-conformal-calibration.png
├── 05-roc-curve.png
├── 06-interactive-geemap.png
│
└── README.md
```

---

## 🚀 Getting Started

### Prerequisites

The project requires:

* Python 3.x
* Google Colab
* Google Earth Engine account
* Google Drive account

### Required Python Libraries

```bash
pip install earthengine-api geemap numpy pandas matplotlib scikit-learn
```

### Google Earth Engine

The project requires authentication with Google Earth Engine before executing the geospatial analysis.

The notebook can be executed through **Google Colab** after connecting and authenticating the Earth Engine environment.

---

## ▶️ How to Run

1. Open `SAMUDRA_UQ.ipynb` in Google Colab.
2. Authenticate your Google Earth Engine account.
3. Define or select the required study district.
4. Load and process the geospatial datasets.
5. Prepare the 17 conditioning factors.
6. Run the Random Forest analysis.
7. Generate the flood susceptibility map.
8. Perform uncertainty and conformal calibration analysis.
9. Generate the ROC curve and calculate AUC.
10. View the final interactive Geemap visualization.

---

## 📌 Expected Outputs

The system produces:

* Flood susceptibility classification maps
* Low, Medium, and High susceptibility regions
* Random Forest variable importance
* Uncertainty estimates
* Conformal calibration results
* ROC curve
* AUC value
* Interactive geospatial visualization
* District-level flood susceptibility analysis

---

## 🎓 Project Type

**Major Project**

### Domain

**Machine Learning | GIS | Remote Sensing | Geospatial Analysis | Uncertainty Quantification**

---

## 📍 Project Status

**Currently Implementing**

The current implementation focuses on integrating Random Forest flood susceptibility mapping with uncertainty analysis, conformal calibration, ROC-AUC evaluation, and interactive geospatial visualization.

---

## 🔮 Future Scope

* Extend the analysis to additional coastal regions.
* Improve the spatial resolution and quality of input datasets.
* Incorporate additional flood-related observations.
* Improve uncertainty quantification techniques.
* Develop a web-based interface for exploring susceptibility maps.
* Provide automated district-wise reporting.
* Support more advanced visualization and decision-support features.

---

## 👩‍💻 Author

**SUPRITHA**

Computer Science Student

---

## ⭐ Acknowledgement

This project makes use of **Google Earth Engine** and open geospatial datasets for processing and analyzing environmental information for flood susceptibility mapping.
