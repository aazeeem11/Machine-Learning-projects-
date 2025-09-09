# Air Quality Index (AQI) Prediction

## Overview
This project involves building a machine learning model to predict and classify Air Quality Index (AQI) levels based on real-world datasets. The model categorizes air quality as **Good**, **Moderate**, or **Bad**. It includes data collection, cleaning, preprocessing, feature engineering, exploratory data analysis (EDA), visualization, handling class imbalance, and training a Support Vector Classifier (SVC) for accurate predictions.

The goal is to provide insights into air quality trends and enable better decision-making for environmental monitoring.

## Tech Stack
- **Programming Language**: Python
- **Libraries**:
  - Scikit-learn (for machine learning models and evaluation)
  - NumPy (for numerical computations)
  - Pandas (for data manipulation and analysis)
  - Matplotlib (for data visualization)
  - Seaborn (for enhanced data visualization)

## Features
- **Data Preprocessing**: Cleaning datasets, feature engineering, exploratory data analysis (EDA), and label encoding.
- **Visualization**: Plots and charts to identify patterns and insights in air quality data.
- **Class Imbalance Handling**: Using SMOTE (Synthetic Minority Over-sampling Technique) to balance classes for improved model performance.
- **Model Training**: Support Vector Classifier (SVC) trained and evaluated for classification accuracy.
- **Prediction**: Classifies AQI into Good, Moderate, or Bad categories.

## Installation
1. Clone the repository:
   ```
   git clone https://github.com/aazeeem11/aqi-prediction.git
   ```
   (Replace with the actual repo URL if different.)

2. Navigate to the project directory:
   ```
   cd aqi-prediction
   ```

3. Install the required dependencies manually:
   ```
   pip install numpy pandas scikit-learn matplotlib seaborn
   ```

## Usage
1. **Prepare Data**: Place your AQI dataset (e.g., CSV file) in the `data/` directory. Ensure it includes relevant features like pollutant levels, weather data, etc.

2. **Run the Notebook/Script**:
   - Open the Jupyter Notebook: `aqi_prediction.ipynb` (or main script: `main.py`).
   - Execute cells/step-by-step for data loading, preprocessing, EDA, model training, and evaluation.

3. **Example Command** (if using a script):
   ```
   python main.py --dataset path/to/your_dataset.csv
   ```

4. **Output**:
   - Visualizations saved in `plots/` directory.
   - Model performance metrics (accuracy, precision, recall, F1-score) printed in the console.
   - Trained model saved as `svc_model.pkl` for future predictions.

## Dataset
- This project uses real-world AQI datasets (e.g., from sources like Kaggle or environmental APIs).
- Example features: PM2.5, PM10, NO2, SO2, CO, O3, temperature, humidity, etc.
- Target: AQI category (Good: 0-50, Moderate: 51-100, Bad: 101+ – adjust based on standards).

Note: Dataset not included in repo due to size/licensing. Download from [Kaggle AQI Datasets](https://www.kaggle.com/search?q=air+quality+index) or similar.

## Exploratory Data Analysis (EDA) Visualizations
During the EDA phase, several visualizations were generated to understand the data distribution, correlations, trends over time, and key feature statistics. Below are the key plots with explanations. (Assume these images are saved in the `plots/` directory of the repository for embedding.)

### 1. AQI Category Distribution
<img width="589" height="455" alt="image" src="https://github.com/user-attachments/assets/55680edb-9d72-4fa6-b369-ea9b5ed38ec4" />


This bar chart shows the distribution of AQI categories in the dataset. The "Bad" category has the highest count (around 17,000 instances), followed by "Moderate" (around 10,000), and "Good" (around 2,000). This highlights a class imbalance, which was addressed using SMOTE to prevent model bias toward the majority class.

### 2. Correlation Heatmap
<img width="942" height="682" alt="image" src="https://github.com/user-attachments/assets/af1e0781-bb10-4e6b-a86a-5b479efba829" />


This heatmap illustrates the Pearson correlations between key pollutants (e.g., PM2.5, PM10, NO, NO2, NOx, NH3, CO, SO2, O3, Benzene, Toluene) and AQI. Strong positive correlations are visible, such as between PM2.5 and PM10 (0.52), NO2 and NOx (0.58), and AQI with pollutants like PM2.5 (0.60) and PM10 (0.42). Negative correlations are minimal, indicating that higher pollutant levels generally contribute to worse AQI. This guided feature selection for the model.

### 3. AQI Over Time
<img width="1169" height="509" alt="image" src="https://github.com/user-attachments/assets/caef9cb5-c310-4f16-af5f-4d22ccf8c5f5" />


This line plot tracks AQI values from 2015 to 2020. AQI fluctuates significantly, with notable spikes in 2017-2019 reaching up to 2,000, possibly due to seasonal or event-based pollution increases. Overall, there's a slight upward trend in variability post-2017, providing temporal insights into air quality deterioration.

### 4. Boxplots of Key Air Quality Features
<img width="1490" height="1025" alt="image" src="https://github.com/user-attachments/assets/a1e59683-1386-4662-b76f-df21d47d0b41" />


These boxplots summarize the distribution of selected features: PM2.5 (median ~50, outliers up to 800+), PM10 (median ~100, outliers to 1,000), NO2 (median ~20, outliers to 350), CO (median ~1, outliers to 175), SO2 (median ~10, outliers to 200), O3 (median ~30, outliers to 250), and AQI (median ~100, outliers to 2,000). They reveal skewness and outliers in pollutant levels, which informed data cleaning and normalization steps.

## Model Evaluation
- **Metrics**: Accuracy, Precision, Recall, F1-Score, Confusion Matrix.
- **Handling Imbalance**: SMOTE applied to oversample minority classes.
- **Cross-Validation**: Used to ensure model generalizes well.

### Confusion Matrix (After SMOTE)
```
[[2929  213  288]
 [  27 3325   71]
 [ 202  219 3057]]
```

### Classification Report
```
              precision    recall  f1-score   support

         Bad       0.93      0.85      0.89      3430
        Good       0.89      0.97      0.93      3423
    Moderate       0.89      0.88      0.89      3478

    accuracy                           0.90     10331
   macro avg       0.90      0.90      0.90     10331
weighted avg       0.90      0.90      0.90     10331
```

## About the Developer
- **Name**: Abdul Azeem
- **LinkedIn**: [www.linkedin.com/in/aazeeem11](https://www.linkedin.com/in/aazeeem11)
- **GitHub**: [github.com/aazeeem11](https://github.com/aazeeem11)
- **Email**: [abdulaaazeem@gmail.com](mailto:abdulaaazeem@gmail.com)
- **Mobile**: +91-6397927883


## License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

Project completed in November 2024.
```


