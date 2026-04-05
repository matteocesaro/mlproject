## End to End Machine Learning Projects

An end-to-end Machine Learning project that predicts students' math scores based on demographic and academic features. The project covers the full ML pipeline from data ingestion to production deployment on AWS.

## 🚀 Live Demo
Deployed on AWS Elastic Beanstalk with CI/CD pipeline via AWS CodePipeline.

## 📌 Project Overview
The application takes as input student information such as gender, ethnicity, parental education, lunch type, test preparation course, reading and writing scores, and predicts the expected math score.

## 🛠️ Tech Stack
- **Language**: Python
- **ML Libraries**: Scikit-learn, NumPy, Pandas
- **Web Framework**: Flask
- **Cloud**: AWS Elastic Beanstalk, AWS CodePipeline
- **Version Control**: GitHub

## 📂 Project Structure
```
├── artifacts/              # Saved model and preprocessor
├── notebook/               # EDA and model experimentation
├── src/
│   ├── components/         # Data ingestion, transformation, model trainer
│   ├── pipeline/           # Predict pipeline
│   ├── exception.py
│   ├── logger.py
│   └── utils.py
├── templates/              # Flask HTML templates
├── .ebextensions/          # AWS Elastic Beanstalk configuration
├── application.py          # Flask app entry point
├── requirements.txt
└── README.md
```

## ⚙️ ML Pipeline
1. **Data Ingestion** — loads raw data and splits into train/test sets
2. **Data Transformation** — handles missing values, encodes categorical features, scales numerical features
3. **Model Training** — trains and evaluates 9 algorithms, automatically selects the best one:
   - Linear Regression ✅ (best model)
   - Lasso, Ridge
   - K-Neighbors Regressor
   - Decision Tree
   - Random Forest
   - XGBoost, CatBoost
   - AdaBoost
4. **Prediction Pipeline** — loads saved model and preprocessor to serve predictions via Flask

## 🔄 CI/CD
Automated deployment pipeline:
- Push to GitHub triggers AWS CodePipeline
- Automatically deploys to AWS Elastic Beanstalk

## 📦 Installation (local)
```bash
git clone https://github.com/matteocesaro/mlproject
cd your-repo-name
pip install -r requirements.txt
python application.py
```

## 📊 Result
The best performing model was **Linear Regression** selected automatically among 9 algorithms.
