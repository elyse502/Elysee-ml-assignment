# Titanic Survival Prediction - ML Assignment 🤖🧠

This project implements a complete data science pipeline using the Titanic dataset. It includes data cleaning, exploratory data analysis (EDA), machine learning model training, and an interactive UI using Gradio.

## 📁 Project Structure

```json
├── cleaned_data.csv         # Cleaned dataset
├── notebook.ipynb           # Full pipeline in Jupyter Notebook
├── titanic_model.joblib     # Trained RandomForestClassifier model
├── requirements.txt         # Python dependencies
├── README.md                # Project documentation
```

<br /><hr /><br />

## 📊 Features

### 🧹 Task 1: Data Cleaning
- Loaded the Titanic dataset from:
  `https://raw.githubusercontent.com/datasciencedojo/datasets/master/titanic.csv`
- Handled missing values:
  - `Age`: filled with median
  - `Embarked`: filled with mode
- Dropped the following columns:
  - `Cabin`: ~77% missing data
  - `Ticket`: inconsistent, high-cardinality
  - `Name`: raw text, no immediate value unless parsed (e.g. title extraction)
  - `PassengerId`: unique row ID, not useful for prediction
- Encoded categorical columns:
  - `Sex`: male → 0, female → 1
  - `Embarked`: S → 0, C → 1, Q → 2
- Removed exact duplicate rows based on all columns
- Saved final cleaned dataset as `cleaned_data.csv`

<br />

### 📈 Task 2: Exploratory Data Analysis (EDA)
- Generated summary statistics using `df.describe()`
- Created 3 visualizations:
  1. **Survival Distribution** using a countplot
  2. **Age Distribution** using histogram with KDE
  3. **Correlation Heatmap** for numeric relationships

<br />

### 🤖 Task 3: Machine Learning Model
- Split data into train/test using `train_test_split`
- Trained a `RandomForestClassifier`
- Evaluated using:
  - `accuracy_score`
  - `classification_report`
- Saved the trained model as `titanic_model.joblib`

<br />

### 🌐 Task 4: UI with Gradio
- Implemented interactive Gradio app for prediction
- Inputs:
  - Passenger class, sex, age, sibsp, parch, fare, embarked
- Outputs:
  - Survival prediction (`Survived` or `Did Not Survive`)

<br /><hr /><br />

## 🚀 How to Run the Project

### 1. Clone the repository
```console
git clone https://github.com/elyse502/Elysee_NIYIBIZI-ml-assignment.git
cd Elysee_NIYIBIZI-ml-assignment
```

### 2. Create a virtual environment (Prevents System Pollution)
```console
python -m venv ml-env
source ml-env/bin/activate  # or venv\Scripts\activate on Windows
```

### 3. Install dependencies
```console
pip install -r requirements.txt
```

### 4. Launch the notebook
```console
jupyter notebook notebook.ipynb
```

### 5. Run the Gradio UI
Once the model is trained and saved, run the last cell in the notebook or:
```console
python gradio_ui.py  # If extracted to a script
```

<br /><hr /><br />

## ✅ Requirements
- Python 3.7+
- Jupyter Notebook
- Pandas, Seaborn, Matplotlib
- Scikit-learn, Joblib
- Gradio

<br /><hr /><br />

## 🙌 Author

- [**NIYIBIZI Elysée**](https://linktr.ee/niyibizi_elysee)👨🏿‍💻 | [Github](https://github.com/elyse502) | [Linkedin](https://www.linkedin.com/in/niyibizi-elys%C3%A9e/) | [Twitter](https://twitter.com/Niyibizi_Elyse).
- **Email**: <elyseniyibizi502@gmail.com>

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/niyibizi-elys%C3%A9e/) [![@phenrysay](https://img.shields.io/badge/Twitter-1DA1F2?style=for-the-badge&logo=twitter&logoColor=white)](https://twitter.com/Niyibizi_Elyse) [![pH-7](https://img.shields.io/badge/GitHub-100000?style=for-the-badge&logo=github&logoColor=white)](https://github.com/elyse502)

---

<br />

<div align="center">
  
This project is part of the AI/ML & Big Data assignment at the [University of Kigali](https://uok.ac.rw/) 👨‍🎓📚🏫.

<br />
Made with ❤️ by <b>Elysée NIYIBIZI</b>
</div>





