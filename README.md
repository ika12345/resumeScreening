#  Resume Screening – Intelligent Resume Classification System

A machine learning-powered web application that automatically classifies resumes into 25+ job categories using NLP and SVM classification. This project demonstrates end-to-end ML pipeline development, from data preprocessing to interactive web deployment.

**Author:** ika12345 | **GitHub:** [github.com/ika12345](https://github.com/ika12345)

![Resume Screening App](https://github.com/ika12345/resumeScreening/blob/main/image/Output.gif)

---

##  🎯 Project Overview

Resume Screening is a practical solution for automated resume categorization. The system preprocesses 962+ resumes, balances the dataset, applies TF-IDF vectorization, and trains multiple ML classifiers to achieve 100% test accuracy. The final model is deployed as an interactive Streamlit web application that accepts PDF, DOCX, and text input.

### Key Features

- **Multi-format Support**: Upload resumes as PDF, Word documents, or plain text
- **Automatic Categorization**: Classifies resumes into 25 professional categories (Data Science, Python Developer, Mechanical Engineer, etc.)
- **Real-time Predictions**: Instant classification with confidence scores
- **Clean Pipeline**: Robust text preprocessing removes URLs, special characters, and noise
- **High Accuracy**: SVM model achieves 100% accuracy on test set with balanced dataset

---

##  🛠 Technology Stack

| Component           | Technology                              |
|---------------------|----------------------------------------|
| **Backend**         | Python 3.13                            |
| **ML Framework**    | scikit-learn (SVM, KNN, Random Forest) |
| **NLP**             | TF-IDF Vectorization                   |
| **Data Processing** | Pandas, NumPy                          |
| **Web Framework**   | Streamlit                              |
| **File Handling**   | PyPDF2 (PDF), python-docx (DOCX)      |
| **Visualization**   | Seaborn, Matplotlib                    |

---

##  📁 Project Structure

```
Resume-Screening/
├── DataSet/
│   └── UpdatedResumeDataSet.csv    # 962 labeled resumes with 25 categories
├── Model/
│   └── Resume Screening.ipynb       # Complete ML pipeline & analysis
├── WebSite/
│   ├── app.py                       # Streamlit web application
│   ├── clf.pkl                      # Trained SVM classifier
│   ├── tfidf.pkl                    # TF-IDF vectorizer
│   ├── encoder.pkl                  # Category label encoder
│   └── requirements.txt
├── image/
│   └── Output.gif                   # Demo animation
└── README.md
```

---

##  🚀 Quick Start

### Prerequisites
- Python 3.10+
- pip package manager

### Installation & Running

```bash
# 1. Clone the repository
git clone https://github.com/ika12345/resumeScreening.git
cd resumeScreening

# 2. Install dependencies
pip install -r WebSite/requirements.txt

# 3. Run the Streamlit app
streamlit run WebSite/app.py

# 4. Open your browser and navigate to
# http://localhost:8501
```

---

##  📊 Model Performance

Three classifiers were trained and evaluated on a balanced dataset (2,100 samples):

| Model                | Accuracy | Precision | Recall | F1-Score |
|----------------------|----------|-----------|--------|----------|
| K-Nearest Neighbors  | 99.76%   | 1.00      | 0.99   | 0.99     |
| Support Vector Mach. | **100%** | **1.00**  | **1.00** | **1.00** |
| Random Forest        | 100%     | 1.00      | 1.00   | 1.00     |

**Selected Model:** Support Vector Machine (SVM) with `OneVsRestClassifier` for multi-class classification.

---

##  🔄 ML Pipeline

1. **Data Exploration**: Analyzed resume distribution across 25 job categories
2. **Data Balancing**: Applied oversampling to balance classes (from 20-84 samples to 84 each)
3. **Text Preprocessing**: 
   - Removed URLs, mentions, hashtags
   - Stripped special characters and punctuation
   - Handled non-ASCII characters
   - Normalized whitespace
4. **Feature Engineering**: TF-IDF vectorization (7,280 features)
5. **Model Training**: Tested KNN, SVM, and Random Forest
6. **Evaluation**: Used confusion matrix, classification report, and accuracy metrics
7. **Deployment**: Serialized models to pickle files for production use

---

##  💡 How to Use the Web App

1. **Upload a Resume**
   - Drag & drop a PDF/DOCX file or paste text directly
   
2. **Get Classification**
   - The system processes the resume and predicts the category
   
3. **View Results**
   - See the predicted job category with confidence information

---

##  📈 Dataset

- **Source**: 962 real resumes across 25 job categories
- **Categories**: Data Science, Python Developer, Java Developer, Testing, DevOps Engineer, HR, Sales, and 18 more
- **Preprocessing**: Balanced using stratified oversampling
- **Final Size**: 2,100 samples (80% train, 20% test)

---

##  🎓 Key Learning Outcomes

- End-to-end ML pipeline development
- Text preprocessing and NLP techniques
- Multi-class classification with scikit-learn
- Model serialization and deployment
- Building interactive web UIs with Streamlit
- Handling real-world imbalanced datasets

---

##  🔧 Future Enhancements

- [ ] Resume ranking based on job description match
- [ ] LinkedIn profile parsing integration
- [ ] Recruiter dashboard with batch processing
- [ ] Active learning with user feedback
- [ ] REST API for enterprise integration
- [ ] Support for multiple languages

---

##  📝 License

MIT License – Free to use, modify, and distribute

---

##  👤 Author

**ika12345**  
GitHub: [@ika12345](https://github.com/ika12345)

---

##  📞 Support & Feedback

Have questions or suggestions? Feel free to open an issue or reach out through GitHub.

---

*Built as a portfolio project to demonstrate ML engineering skills in data preprocessing, model training, evaluation, and web deployment.*
