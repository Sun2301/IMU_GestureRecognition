# IMU Gesture Recognition - EEIA 2025

## Overview
This project implements gesture recognition using IMU (Inertial Measurement Unit) sensor data in industrial environments. The goal is to enable hands-free interface interaction through reliable gesture detection using wrist-worn IMU sensors.

## Problem Statement
In industrial settings, workers often need to interact with interfaces without using their hands due to:
- Hygiene requirements
- Protective equipment (gloves)
- Electrical safety concerns

## Solution
A machine learning model that:
- Recognizes predefined gestures from IMU sensor readings
- Processes instantaneous measurements from 6-axis sensors
- Provides robust performance in noisy conditions
- Is suitable for embedded deployment

## Dataset
The training dataset consists of 3,500 individual observations collected using a 6-axis IMU sensor:

### Features
| Sensor Reading | Description | Unit |
|----------------|-------------|------|
| Ax | X-axis acceleration | m/s² |
| Ay | Y-axis acceleration | m/s² |
| Az | Z-axis acceleration | m/s² |
| Gx | X-axis angular velocity | rad/s |
| Gy | Y-axis angular velocity | rad/s |
| Gz | Z-axis angular velocity | rad/s |

### Data Files
- `data/X_train.csv`: Training features
- `data/y_train.csv`: Training labels
- `data/X_test.csv`: Test features

## Implementation
The project includes:
1. **Data Analysis**
   - Feature distribution analysis
   - Class balance checking
   - Correlation analysis
   
2. **Model Development**
   - Multiple classifier comparison:
     - Logistic Regression
     - K-Nearest Neighbors
     - Random Forest
   - Hyperparameter optimization
   - Performance evaluation

## Performance Metric
The model is evaluated using accuracy:
```
Accuracy = (Number of correct predictions) / (Total number of predictions)
```

## Project Structure
```
IMU_Gesture_Recognition/
├── data/               # Dataset files
├── notebooks/         # Jupyter notebooks
│   └── notebook_starter.ipynb
└── README.md
```

## Requirements
- Python 3.x
- pandas
- numpy
- matplotlib
- seaborn
- scikit-learn

## Setup and Usage
1. Clone the repository
2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
3. Open and run `notebooks/notebook_starter.ipynb`

## Future Improvements
- Feature engineering for better gesture recognition
- Model optimization for embedded deployment
- Real-time prediction implementation
- Cross-validation for robust performance estimation
- Hyperparameter tuning
- Model serialization and deployment script