# Global Superstore Prediction Tools
## LnT Camp 2026: Bridging the Gap: Empowering Future Talent through Machine Learning for Industry Innovation

### About the Project
After 10 meeting of learning about **Machine Learning** by online zoom. This 3 weeks project become the final project of the series of ***LnT Camp 2026: Bridging the Gap: Empowering Future Talent through Machine Learning for Industry Innovation*** learning how the flow of building a machine learning that taught by *Yahya Putra Pradana*.

### Modelling Tasks
#### A. Regression
Predict a sales of an order items by using Linear Regression
#### B. Classification
Predict whether an order items is profitable or not profitable

### Dataset
Download the database from: https://drive.google.com/file/d/1M2sonY7serOCzWYDCKEdxZ5fJ7quOoKd/view?usp=sharing
Place it in the notebook folder as database.sqlite before running the notebook.

### Folder Structure
```lnt-camp-2026-final-project/
├── backend/
│   ├── main.py
│   └── requirements.txt
├── frontend/
│   ├── app.py
│   ├── requirements.txt
│   ├── templates/
│   │   └── index.html
│   └── static/
│       ├── styles.css
│       └── js/
│           └── script.js
├── model/
│   ├── classification_model.pkl
│   ├── regression_model.pkl
│   ├── scaler.pkl
│   └── feature_columns.json
├── notebook/
│   ├── pipeline.ipynb
│   └── database.sqlite       (gitignored, not pushed — see download instructions below)
├── .gitignore
└── README.md 
```

### How to Setup and Run
#### 1. Backend (FastAPI)
```bash
cd backend
python -m venv venv
venv\Scripts\Activate.ps1        # Windows
# source venv/bin/activate       # Mac/Linux
pip install -r requirements.txt
uvicorn main:app
```
Runs at `http://127.0.0.1:8000`. Confirm it's running by visiting `/health`.

#### 2. Frontend (Flask)
Requires the backend to be running first (see above).
```bash
cd frontend
python -m venv venv
venv\Scripts\Activate.ps1        # Windows
# source venv/bin/activate       # Mac/Linux
pip install -r requirements.txt
python app.py
```
Open `http://127.0.0.1:5000` in your browser.


### Key Findings

- Sales and profit are both right-skewed, driven by a small number of large orders.
- **Tables** is the only product sub-category with negative total profit.
- Discounts above ~40% are strongly associated with unprofitable orders.

Full analysis and interpretation available in `notebook/pipeline.ipynb`.

### Tech Stack
Frontend: Flask, HTML, CSS, Javascript
Backend: joblib, pandas, FastAPI, pydantic
Modelling: joblib, sqlite3, numpy, pandas, seaborn, matplotlib, scikit-learn

### Links
Deploy Frontend:
LinkedIn post: 

### Social
Github      : https://github.com/patrickseroh
LinkedIn    : https://www.linkedin.com/in/patrickseroh/
Instagram   : https://www.instagram.com/patrickseroh/