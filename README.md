
# 🎭 Emotion Prediction AI

A full-stack machine learning application that classifies emotions from text using multiple NLP models and provides predictions through a modern web interface.

![Python](https://img.shields.io/badge/Python-3.10+-blue.svg)
![FastAPI](https://img.shields.io/badge/FastAPI-0.104+-green.svg)
![Streamlit](https://img.shields.io/badge/Streamlit-1.28+-red.svg)
![Scikit-learn](https://img.shields.io/badge/Scikit--learn-1.3+-orange.svg)

## 🌟 Features

- **Multi-Model Architecture**: Compare performance of 4 different ML classifiers
- **Real-time Prediction**: Instant emotion analysis from text input
- **RESTful API**: FastAPI backend with proper validation
- **Modern UI**: Streamlit frontend with emojis and responsive design
- **High Accuracy**: Best model achieves 99.53% test accuracy
- **Production Ready**: Model serialization and error handling

## 🏗️ System Architecture

```
Frontend (Streamlit) ←→ Backend (FastAPI) ←→ ML Models (Scikit-learn)
       ↑                      ↑                      ↑
   User Interface        REST API Server      Emotion Classification
```

## 📊 Model Performance

| Model | Test Accuracy | Use Case |
|-------|---------------|----------|
| Linear SVC | 99.53% | **Production** |
| Logistic Regression | 90.88% | Backup |
| Bernoulli Naive Bayes | 90.67% | Comparison |
| Multinomial Naive Bayes | 88.63% | Baseline |

## 🚀 Quick Start

### Prerequisites
```bash
Python 3.10+
pip install -r requirements.txt
```

### Installation

1. **Clone the repository**
```bash
git clone https://github.com/zaryabahmad/emotion-prediction-ai.git
cd emotion-prediction-ai
```

2. **Install dependencies**
```bash
pip install -r requirements.txt
```

3. **Run the backend API**
```bash
python fastapi_backend.py
```

4. **Run the frontend** (in new terminal)
```bash
streamlit run streamlit_frontend.py
```

5. **Access the application**
```
Frontend: http://localhost:8501
Backend: http://localhost:8000
```

## 📁 Project Structure

```
emotion-prediction-ai/
├── 📁 models/
│   ├── emotion_pred.joblib          # Trained ML model
│   └── tfidf.joblib                 # TF-IDF vectorizer
├── 📁 src/
│   ├── fastapi_backend.py           # FastAPI server
│   ├── streamlit_frontend.py        # Streamlit UI
│   └── emotion_detection.ipynb           # Training 
└── README.md
```

## 🎯 Usage Examples

### Input Text & Predictions:
- "I'm so happy today!" → **😄 Joy**
- "This makes me furious!" → **😠 Anger** 
- "I feel scared and alone" → **👻 Fear**
- "Everything feels so heavy" → **😢 Sadness**

### API Usage:
```python
import requests

response = requests.post(
    "http://localhost:8000/predict",
    json={"fellings": "I'm feeling amazing today!"}
)
print(response.json())  # {"prediction": "Joy"}
```

## 🔧 Configuration

### Model Training Features:
- **TF-IDF Vectorization** with 5000 features
- **N-gram range**: (1,2)
- **Stop words**: English
- **Text cleaning**: Automatic preprocessing

### Emotion Labels:
```python
0 = Sadness 😢
1 = Joy 😄
2 = Love ❤️  
3 = Anger 😠
4 = Fear 👻
5 = Surprise 😲
```

## 📈 Performance Metrics

- **Dataset Size**: 416,809 samples
- **Best Accuracy**: 99.53% (Linear SVC)
- **Preprocessing**: TF-IDF with bi-grams
- **Cross-validation**: 80/20 train-test split

## 🛠️ Technical Stack

**Backend:**
- FastAPI (API framework)
- Pydantic (Data validation)
- Uvicorn (ASGI server)

**Frontend:**
- Streamlit (Web interface)
- Requests (API communication)
<img width="1366" height="768" alt="image" src="https://github.com/user-attachments/assets/17c92cf6-c7bc-4d49-8ea2-abb533636c49" />


**Machine Learning:**
- Scikit-learn (ML models)
- Pandas (Data processing)
- Joblib (Model serialization)

**Models Implemented:**
- Linear SVC
- Logistic Regression
- Bernoulli Naive Bayes
- Multinomial Naive Bayes

## 🤝 Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📝 License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details.

## 👨‍💻 Developer

**Zaryab Ahmad**  
- 🎓 BSIT Final Year  
- 🏫 Emerson University, Multan  
- 📧 zaryabahmad983@gmail.com
- 🔗 [LinkedIn](https://www.linkedin.com/in/zaryab-ahmad-56740b295)
- 💻 [GitHub](https://github.com/zaryabahmad)

## 🙏 Acknowledgments

- Emerson University Multan for academic support
- Scikit-learn community for excellent ML tools
- FastAPI and Streamlit teams for fantastic web frameworks

---

**⭐ Star this repo if you find it helpful!**
```


