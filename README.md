# Literature-mining-and-data-generation-of-material-systems-for-alloy-design-using-Generative-AI
 Flask-based AI platform for extracting materials data from PDFs, building physics-informed HEA datasets, and training explainable machine learning models for hardness prediction.


What this version does:

fetches literature automatically from Crossref and Europe PMC
stores paper metadata and abstracts locally in the app
weakly extracts:
composition strings like Al20Co20Cr20Fe20Ni20
hardness values like 450 HV
builds a derived HEA dataset from the fetched literature
trains a model and shows:
model comparison
SHAP
RAG-style evidence search
browser dashboard


Purpose of this program

This program is a single-file Flask dashboard for HEA literature mining and modeling.

It does five main things:

fetches papers from public scholarly APIs
stores titles and abstracts locally
weakly extracts:
alloy composition strings
hardness values
converts those into a derived tabular dataset
trains ML models and serves a dashboard with:
prediction



# 🚀 HEA PDF Extraction + Materials AI Platform

## 📌 Overview

This project is a **production-style Materials AI system** that extracts data directly from research PDFs and builds **physics-informed machine learning models** for high-entropy alloy (HEA) property prediction.

It demonstrates a complete pipeline from **raw scientific documents → structured dataset → deployable ML models → explainable predictions**.

---

## 🔥 Key Features

### 🔍 PDF-Based Data Extraction

* Full-text extraction using **PyMuPDF**
* Table extraction using **pdfplumber**
* Works directly on research papers (not limited to metadata/abstracts)

---

### ⚙️ Physics-Informed Feature Engineering

Automatically computes key HEA descriptors:

* **VEC (Valence Electron Concentration)**
* **Atomic size mismatch (δ)**
* **Mixing entropy (ΔSmix)**
* **Mixing enthalpy (ΔHmix)**
* Derived interaction features

---

### 🤖 Machine Learning Models

* Gradient Boosting Regressor
* Random Forest
* Extra Trees

Includes:

* Model comparison (R², MAE)
* Data filtering + augmentation
* Robust training pipeline

---

### 🔬 Explainable AI

* SHAP-based feature importance
* Interpretable prediction insights

---

### 🌐 Web API + Dashboard

* Built with **Flask**
* Upload PDFs via browser
* Extract datasets automatically
* Train models interactively
* Predict material properties in real-time

---

## 🏗️ System Architecture

```text
PDF Papers
   ↓
Text + Table Extraction
   ↓
Weak Data Parsing (composition + hardness)
   ↓
Physics Feature Engineering
   ↓
Dataset Generation
   ↓
ML Training + Comparison
   ↓
API + Dashboard + SHAP Explainability
```

---

## 📂 Project Structure

```text
hea-pdf-materials-ai-platform/
├── app/
│   └── hea_pdf_webapi_singlefile.py
├── data/
│   ├── pdf_uploads/
│   └── pdf_outputs/
├── artifacts_pdf_api/
├── requirements.txt
├── run.sh
├── run.bat
├── LICENSE
└── README.md
```

---

## ⚙️ Installation

```bash
pip install -r requirements.txt
```

---

## ▶️ Run the Application

```bash
python app/hea_pdf_webapi_singlefile.py
```

Open in browser:

```text
http://127.0.0.1:5000
```

---

## 🧪 Usage Workflow

1. Upload research PDFs
2. Click **Extract from PDFs**
3. Preview generated dataset
4. Train ML models
5. Input alloy composition
6. Get predicted hardness + SHAP explanation

---

## 📊 Example Input

```text
Al20Co20Cr20Fe20Ni20
```

---

## 📈 Output

* Predicted hardness (HV)
* Feature contributions (SHAP)
* Physics-informed descriptors

---

## ⚠️ Limitations

* Works best on **machine-readable PDFs**
* Scanned PDFs require OCR (future enhancement)
* Weak supervision → noisy labels possible

---

## 🚀 Future Enhancements

* OCR integration (Tesseract / PyMuPDF OCR)
* RAG + LLM-based scientific extraction
* Multi-property prediction (elastic constants, phase)
* Autonomous materials discovery pipeline

---

## 💡 Why This Project Matters

This project demonstrates:

* End-to-end AI system design
* Materials science + ML integration
* Real-world data extraction (not toy datasets)
* Deployment-ready API
* Explainable AI in scientific workflows

---

## 📜 License

MIT License

SHAP
RAG-style literature search
model comparison plots
