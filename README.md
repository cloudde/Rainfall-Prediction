🌧️ Rainfall Prediction using ML Classifiers
This project implements a machine learning pipeline to predict rainfall occurrence (yes or no) based on meteorological data. The workflow includes data preprocessing, feature selection, class imbalance handling, model training, evaluation, and visualization.

📁 Project Overview
Goal: Predict whether it will rain based on weather features.

Models Used: Logistic Regression, XGBoost, and SVM (RBF kernel)

Techniques: Data cleaning, visualization, feature engineering, oversampling (SMOTE/ROS), normalization

Evaluation Metrics: AUC-ROC, classification report, confusion matrix

🧾 Dataset
The dataset Rainfall.csv contains daily weather observations with the target column rainfall labeled as yes or no.

Key Features:
Temperature (max/min)

Humidity

Pressure

Wind speed

Day

Rainfall (yes/no - Target)

Preprocessing steps:
Handled missing values using column-wise mean

Renamed/cleaned column names

Encoded target variable (yes = 1, no = 0)

Removed highly correlated features (maxtemp, mintemp)

Balanced the dataset using RandomOverSampler

Normalized features using StandardScaler

🧰 Tech Stack
Python (NumPy, Pandas, Matplotlib, Seaborn)

scikit-learn (SVC, Logistic Regression, model selection & evaluation)

XGBoost

imblearn (RandomOverSampler)

Matplotlib/Seaborn (for visualizations)

🧪 Model Training and Evaluation
Models trained:

LogisticRegression()

XGBClassifier()

SVC(kernel='rbf', probability=True)

Training/Validation AUC Scores:
Model	Training AUC	Validation AUC
Logistic Regression	0.889	0.897
XGBoost	1.000	0.839
SVM (RBF Kernel)	0.903	0.886

Evaluated using AUC-ROC

Printed classification reports and plotted confusion matrices

📊 Visualizations
Pie chart of rainfall class distribution

Distribution and boxplots of all numerical features

Heatmap to identify high correlations

Confusion matrix for model predictions

📂 Project Structure
Copy
Edit
rainfall-prediction/


├── Rainfall.csv

├── rainfall_prediction.py

├── README.md

▶️ How to Run

Clone the repo:


git clone https://github.com/cloudde/Rainfall-Prediction.git

cd rainfall-prediction

Install dependencies:

pip install -r requirements.txt

Run the script:



python rainfall_prediction.py

🔬 Sample Output
yaml


LogisticRegression() :

Training Accuracy :  0.889

Validation Accuracy :  0.897


XGBClassifier() :

Training Accuracy :  1.000

Validation Accuracy :  0.839


SVC() :

Training Accuracy :  0.903

Validation Accuracy :  0.886

🤝 Contributions

Feel free to fork this repo and submit a pull request with improvements.


📄 License

This project is licensed under the MIT License.
