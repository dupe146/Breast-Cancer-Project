# 🔬 Breast Cancer Classification Web Application

A machine learning-based web application for breast cancer tumor classification using the Wisconsin Breast Cancer Dataset.

**Live Application**: https://breastcancerprojectjimoh-alabiislamiatmodupe250000033-rscb8pl8.streamlit.app/

---

## 📋 Table of Contents

- [Project Overview](#project-overview)
- [Features](#features)
- [Technologies Used](#technologies-used)
- [Project Structure](#project-structure)
- [Installation & Setup](#installation--setup)
- [Running Locally](#running-locally)
- [Deployment (Streamlit Cloud)](#deployment-streamlit-cloud)
- [Model Information](#model-information)
- [Disclaimer](#disclaimer)

---

## 📊 Project Overview

This project implements a complete machine learning pipeline for breast cancer classification:

1. **Data Processing**: Loading and preprocessing the Wisconsin Breast Cancer Dataset
2. **Feature Selection**: Using 5 carefully selected features for classification
3. **Model Training**: Training a Logistic Regression classifier
4. **Web Application**: Streamlit-based interactive web interface
5. **Deployment**: Production-ready deployment on Streamlit Cloud

### Key Achievements
- ✅ **High Accuracy**: 95%+ classification accuracy
- ✅ **5-Feature Model**: Optimized feature selection
- ✅ **Real-time Predictions**: Instant classification results
- ✅ **User-Friendly Interface**: Modern, intuitive Streamlit UI

---

## ✨ Features

- 🔍 **Tumor Classification**: Binary classification (Benign/Malignant)
- 📊 **5 Feature Analysis**: radius_mean, texture_mean, perimeter_mean, area_mean, concavity_mean
- 💯 **Confidence Scores**: Probability estimates for predictions
- 🎨 **Modern UI**: Clean, responsive Streamlit interface
- 🚀 **Fast Predictions**: Near-instant results
- 📱 **Mobile Friendly**: Responsive design for all devices
- 📈 **Visual Feedback**: Progress bars and color-coded results

---

## 🛠️ Technologies Used

### Backend & ML
- **Python 3.11**
- **Streamlit** - Web framework
- **scikit-learn 1.3.0** - Machine learning
- **NumPy 1.24.3** - Numerical computing
- **Pandas** - Data manipulation

### Model
- **Algorithm**: Logistic Regression
- **Persistence**: Pickle (`.pkl` files)
- **Preprocessing**: StandardScaler for feature normalization

### Deployment
- **Streamlit Cloud** - Free cloud hosting
- **Git/GitHub** - Version control

---

## 📁 Project Structure

```
Breast-Cancer-Project/
│
├── app.py                              # Main Streamlit application
├── requirements.txt                    # Python dependencies
├── README.md                          # This file
├── BreastCancer_hosted_webGUI_link.txt # Deployment information
│
└── model/                             # Model artifacts
    ├── model_building.ipynb          # Training notebook
    ├── breast_cancer_model.pkl       # Trained model
    ├── scaler.pkl                    # Feature scaler
    └── model_metadata.json           # Model information
```

---

## 🚀 Installation & Setup

### Prerequisites
- Python 3.11 or 3.10
- pip (Python package manager)
- Git

### Step 1: Clone Repository

```bash
git clone https://github.com/yourusername/Breast-Cancer-Project.git
cd Breast-Cancer-Project
```

### Step 2: Create Virtual Environment (Recommended)

```bash
# Create virtual environment
python3.11 -m venv venv

# Activate virtual environment
# On macOS/Linux:
source venv/bin/activate

# On Windows:
venv\Scripts\activate
```

### Step 3: Install Dependencies

```bash
pip install -r requirements.txt
```

### Step 4: Verify Model Files

Ensure these files exist in the `model/` directory:
- ✅ `breast_cancer_model.pkl`
- ✅ `scaler.pkl`
- ✅ `model_metadata.json` (optional)

---

## 💻 Running Locally

### Start the Application

```bash
streamlit run app.py
```

### Access the Application

The app will automatically open in your browser at:
```
http://localhost:8501
```

### Testing the Application

1. Enter tumor feature values in the input fields
2. Click **" Predict"**
3. View the prediction results with:
   - Classification (Benign/Malignant)
   - Confidence score
   - Probability breakdown
   - Color-coded visual feedback

### Stopping the Application

Press `Ctrl + C` in the terminal

---

## 🌐 Deployment (Streamlit Cloud)

### Prerequisites
- GitHub account
- Streamlit Cloud account (free - sign up at [share.streamlit.io](https://share.streamlit.io))
- Project pushed to GitHub

### Step-by-Step Deployment

#### 1. Prepare for Deployment

Ensure your `requirements.txt` contains:
```txt
streamlit
numpy
scikit-learn
```

#### 2. Push to GitHub

```bash
git add .
git commit -m "Ready for deployment"
git push origin main
```

#### 3. Deploy on Streamlit Cloud

1. **Go to [share.streamlit.io](https://share.streamlit.io)** and sign in with GitHub
2. **Click "New app"**
3. **Configure the deployment:**
   - Repository: `yourusername/BreastCancer_Project_...`
   - Branch: `main`
   - Main file path: `app.py`
4. **Click "Deploy"**
5. **Wait 2-3 minutes** for deployment
6. **Your app is live!** Copy the URL

### Your Live URL Format
```
https://your-app-name.streamlit.app
```

### Streamlit Cloud Settings Summary

| Setting | Value |
|---------|-------|
| **Python Version** | 3.11 (auto-detected) |
| **Main File** | `app.py` |
| **Requirements** | `requirements.txt` |
| **Deployment Time** | 2-3 minutes |
| **Cost** | Free |

### Updating Your Deployed App

Any push to your GitHub repository will automatically redeploy the app:

```bash
git add .
git commit -m "Update message"
git push
```

Streamlit Cloud will detect changes and redeploy automatically.

### Troubleshooting Deployment

**Issue: Build fails**
- Check `requirements.txt` has only 3 lines (no version numbers)
- Ensure all model files are committed to Git
- Check GitHub repository has all files

**Issue: App crashes on start**
- Verify model files exist in `model/` folder
- Check file paths in `app.py` are correct
- View logs in Streamlit Cloud dashboard

**Issue: File not found errors**
- Ensure folder structure matches code
- Check that `model/` folder contains all `.pkl` files

---

## 🧠 Model Information

### Dataset
- **Source**: Wisconsin Breast Cancer Dataset (UCI Repository)
- **Samples**: 569 (357 benign, 212 malignant)
- **Features Used**: 5 selected features from 30 available

### Selected Features
1. **radius_mean** - Mean of distances from center to points on perimeter
2. **texture_mean** - Standard deviation of gray-scale values
3. **perimeter_mean** - Mean size of core tumor
4. **area_mean** - Mean area of tumor
5. **concavity_mean** - Mean severity of concave portions of contour

### Model Architecture
- **Algorithm**: Logistic Regression
- **Solver**: lbfgs
- **Max Iterations**: 10,000
- **Random State**: 42 (for reproducibility)
- **Persistence**: Pickle

### Performance Metrics
- **Accuracy**: ~95%
- **Precision**: High precision for both classes
- **Recall**: High recall for both classes
- **F1-Score**: Balanced performance

### Data Preprocessing
1. **Feature Selection**: 5 features from available 8 options
2. **Train-test Split**: 80-20 ratio
3. **Feature Scaling**: StandardScaler (zero mean, unit variance)
4. **Stratified Sampling**: Maintains class distribution

### Model Files
- **breast_cancer_model.pkl**: Trained Logistic Regression model
- **scaler.pkl**: Fitted StandardScaler for feature normalization
- **model_metadata.json**: Model information and metrics

---

## 📊 Usage Examples

### Example 1: Benign Tumor
```
Radius Mean: 13.5
Texture Mean: 18.2
Perimeter Mean: 87.5
Area Mean: 566.0
Concavity Mean: 0.08

Expected Result: BENIGN (High Confidence)
```

### Example 2: Malignant Tumor
```
Radius Mean: 20.5
Texture Mean: 25.3
Perimeter Mean: 135.0
Area Mean: 1200.0
Concavity Mean: 0.25

Expected Result: MALIGNANT (High Confidence)
```

---

## ⚠️ Disclaimer

**IMPORTANT: This application is for EDUCATIONAL PURPOSES ONLY.**

- ❌ NOT intended for actual medical diagnosis
- ❌ NOT a substitute for professional medical advice
- ❌ NOT validated for clinical use
- ❌ NOT approved by any medical regulatory body

**Always consult qualified healthcare professionals for medical concerns.**

This project demonstrates:
- Machine learning classification techniques
- Feature selection and model optimization
- Web application development with Streamlit
- Model deployment best practices

It should **NEVER** be used to make real medical decisions.

---

## 📝 Development Notes

### Local Development

```bash
# Activate virtual environment
source venv/bin/activate  # macOS/Linux
# or
venv\Scripts\activate     # Windows

# Run the app
streamlit run app.py

# The app will open at http://localhost:8501
```

### Clearing Streamlit Cache

If you encounter issues:
```bash
# Clear Streamlit cache
rm -rf ~/.streamlit

# Or use the UI: Click "☰" → "Clear cache"
```

---

## 🎓 Academic Information

**Course Project**: Artificial Intelligence
**Algorithm**: Logistic Regression  
**Persistence**: Pickle  
**Framework**: Streamlit  
**Deployment**: Streamlit Cloud  

---

## 📚 Learning Outcomes

This project demonstrates proficiency in:

1. ✅ Loading and preprocessing medical datasets
2. ✅ Feature selection and engineering
3. ✅ Training machine learning classification models
4. ✅ Model evaluation and validation
5. ✅ Model persistence using Pickle
6. ✅ Web application development with Streamlit
7. ✅ Cloud deployment and hosting
8. ✅ Creating user-friendly interfaces
9. ✅ Documentation and version control

---

## 📄 License

This project is created for educational purposes as part of academic coursework.  
All code is available for educational use and learning.

---
