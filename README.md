
# Phishing Email Detection System

A machine learning-based web application that detects phishing emails and distinguishes them from legitimate emails using email content analysis and classification models.

## About the Project

Phishing emails are commonly used to trick users into sharing sensitive information such as passwords, banking details, and personal data.

This project aims to identify potentially malicious emails by analyzing their textual content, extracting relevant features, and applying machine learning algorithms to classify them.

The application provides an easy-to-use interface where users can submit email content and view the prediction along with suspicious indicators.

## Features

- Email classification as Phishing or Legitimate.
- Machine learning-based prediction using Random Forest and Support Vector Machine (SVM).
- TF-IDF-based text feature extraction.
- Detection of suspicious keywords and URLs.
- Email statistics and risk score analysis.
- Individual model predictions and combined prediction.
- Email file upload and analysis.
- Analytics dashboard for viewing prediction statistics.
- MySQL database integration for storing email and prediction records.

## Technologies Used

**Programming Language**
- Python

**Backend**
- Flask

**Frontend**
- HTML
- CSS
- JavaScript
- Bootstrap

**Machine Learning**
- Scikit-learn
- Pandas
- NumPy
- TF-IDF Vectorizer
- Random Forest
- Support Vector Machine (SVM)

**Database**
- MySQL

## Project Structure

```text
phishing-email-detection/
│
├── app.py
├── config.py
├── train_model.py
├── requirements.txt
│
├── database/
│   └── create_tables.sql
│
├── data/
│   └── models/
│
├── src/
│   ├── prediction.py
│   └── database.py
│
├── static/
│   ├── css/
│   └── js/
│
├── templates/
│   ├── index.html
│   ├── dashboard.html
│   ├── upload.html
│   └── result.html
│
├── uploads/
│
└── README.md
```

## Installation and Setup

### 1. Clone the Repository

```bash
git clone <repository-url>
cd phishing-email-detection
```

### 2. Create a Virtual Environment

```bash
python -m venv .venv
```

Activate it on Windows:

```bash
.venv\Scripts\activate
```

### 3. Install Dependencies

```bash
pip install -r requirements.txt
```

### 4. Configure Environment Variables

Create a `.env` file in the project root directory.

Add your MySQL database configuration:

```env
DB_HOST=localhost
DB_USER=root
DB_PASSWORD=your_mysql_password
DB_NAME=phishing_detection
```

### 5. Setup the Database

Create the database and tables using the SQL script:

```sql
CREATE DATABASE phishing_detection;
```

Execute the SQL commands in:

```text
database/create_tables.sql
```

### 6. Run the Application

```bash
python app.py
```

Open your browser and visit:

```text
http://127.0.0.1:5000
```

## How It Works

1. The user enters email content or uploads an email file.
2. The application preprocesses the email text.
3. TF-IDF vectorization converts text into numerical features.
4. Machine learning models analyze the extracted features.
5. The system generates phishing or legitimate predictions.
6. Suspicious indicators and email statistics are displayed.
7. Email and prediction records are stored in the MySQL database.

## Machine Learning Models

| Model | Purpose |
|---|---|
| Random Forest | Email classification |
| Support Vector Machine | Email classification |
| TF-IDF | Text feature extraction |

## Future Improvements

- Explainable AI for understanding prediction results.
- Advanced URL and domain reputation analysis.
- Email sender authentication checks.
- Improved phishing threat intelligence.
- Real-time threat monitoring.
- Enhanced analytics and visualization.

## Disclaimer

This project is developed for educational and research purposes. Predictions are based on machine learning models and should not be considered a guarantee that an email is safe or malicious.

---

**Project:** Phishing Email Detection System  
**Domain:** Machine Learning | Cybersecurity
