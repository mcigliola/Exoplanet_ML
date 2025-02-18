# **Exoplanet Classification with Machine Learning**

## **Overview**
This project explores the use of machine learning techniques to classify distant stars as either harboring exoplanets or not, using stellar flux time-series data. The dataset is "Exoplanet Hunting in Deep Space" available through Kaggle (https://www.kaggle.com/datasets/keplersmachines/kepler-labelled-time-series-data), which compiles data from the NASA Kepler Space Telescope. The goal is to train models that can detect exoplanets based on variations in brightness.

This project was completed as a learning exercise in data preprocessing, model training, and hyperparameter tuning. It explores different architectures to handle imbalanced classification problems in real-world datasets.

## **Dataset**
- The dataset consists of stellar light curves, which are time-series data representing the brightness of stars over time.
- Labels:
  - **1** - Star has no detected exoplanets.
  - **2** - Star has at least one exoplanet.
- The dataset is highly imbalanced, with very few examples of confirmed exoplanets compared to non-exoplanet stars.

## **Approach**
The project explores two types of neural network machine learning models:
- **1D Convolutional Neural Network (CNN)** to detect spatial patterns in light curves.
- **Long Short-Term Memory (LSTM) Network** to capture temporal dependencies in the data.

## **Techniques Used**
### **Data Preprocessing**
- Feature scaling with StandardScaler.
- Handling class imbalance using SMOTE.
- Exploratory Data Analysis (EDA) of light curves.

### **Model Training & Tuning**
- **Regularization techniques**: Dropout and batch normalization.
- **Hyperparameter tuning** using early stopping, learning rate adjustments, and weighted loss functions.
- **Model comparison** between CNN and LSTM architectures.

## **Results & Challenges**
- The models successfully identified patterns in the data but struggled with class imbalance, especially in detecting stars with exoplanets.
- The **CNN models** performed well in identifying non-exoplanet stars but had difficulty generalizing to exoplanet candidates.
- The **LSTM models** improved recall for exoplanets but at the cost of overall accuracy.
- Additional feature extraction techniques (e.g., periodicity analysis) may improve performance but were beyond the scope of this project.

## **Next Steps**
- **Feature Engineering**: Extracting astrophysical features beyond raw light curves.
- **Alternative Architectures**: Trying hybrid CNN-LSTM models for better pattern recognition.
- **More Data**: Combining multiple Kepler datasets to improve class balance.
