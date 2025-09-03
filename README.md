
# MSc. Dissertation: Developing NLP Approaches to Extract Medical Information from Schizophrenia Clinical Summaries

This repository contains the code, supporting files, and documentation for my MSc Computing dissertation at **Cardiff University**.  
The project explored how **Natural Language Processing (NLP)** techniques can be used to extract treatment-related information, disease progression, and outcomes from schizophrenia clinical notes.

---

## 📖 Abstract

Schizophrenia is a complex mental health disorder characterized by diverse symptoms and treatment responses. A significant challenge in predicting outcomes is the lack of structured clinical information beyond the initial diagnosis.  

This project develops and validates NLP methods to extract clinically relevant details from free-text clinical summaries. The focus is on identifying:

- Symptoms and premorbid symptoms  
- Prescribed medications and side effects  
- Disease course and hospitalizations  
- Treatment response and outcomes  

Validation was performed through manual review and comparison with existing variables. The results provide insights into the use of NLP for mental health research and support the ongoing work of the **Schizophrenia Research Group at Cardiff University**.

---

## 🎯 Aim and Objectives

**Aim:**  
To design and validate an NLP model capable of accurately extracting and interpreting treatment-related information, disease progression, and clinical outcomes from schizophrenia clinical summaries.

**Objectives:**
1. Implement NLP techniques to answer targeted clinical questions.  
2. Validate the model against existing datasets and manual inspection.  
3. Identify limitations of NLP in clinical notes and propose improvements for future use.

---

## ⚙️ Methods & Approach

- **Exploratory Data Analysis (EDA):** Word count distribution, missing values, and term frequency analysis.  
- **Symptom–Medication Analysis:** Extraction of co-occurring symptoms and prescribed drugs using regex + predefined medication lists.  
- **Model Choice:** Meta’s **LLaMA-3.2–1B** language model, selected for its efficiency in handling nuanced text. Alternative models (GPT-3, BERT) were considered.  
- **Evaluation:** Manual review of outputs + metrics (accuracy, precision, recall, F1 score).  

The model was tested by asking targeted clinical questions, e.g.:
- What symptoms are recorded?  
- Are there premorbid symptoms?  
- What medications are prescribed?  
- Any side effects noted?  
- Signs of improvement or worsening?  
- Any hospitalizations recorded?

---

## 📊 Key Results

- **Strengths:** High accuracy in extracting hospitalization history and symptom progression.  
- **Moderate performance:** For symptoms and prescribed medications, responses were sometimes incomplete or repetitive.  
- **Limitations:** The model struggled with side effects, occasionally “hallucinating” details. Performance was sensitive to question phrasing.  
- **Overall:** Reliable for structured information (hospitalizations, improvement) but requires refinement for nuanced details (medications, side effects).

---

## 📂 Repository Structure

```

├── data/                       # Dummy schizophrenia dataset (anonymized for demo)
├── notebooks/                  # Jupyter notebooks for EDA & analysis
├── EDA\_analysis.ipynb          # Exploratory Data Analysis
├── Symptom\_med\_analysis.py     # Symptom–medication pair analysis
├── llama\_model1.py             # LLaMA model implementation
├── requirements.txt            # Dependencies
├── README.md                   # This file
└── docs/                       # Supporting charts & visuals

````

---

## 🚀 Getting Started

### 1. Set up environment
```bash
python3 -m venv venv
source venv/bin/activate   # On Windows: .\venv\Scripts\activate
pip install -r requirements.txt
````

### 2. Run Exploratory Data Analysis

```bash
jupyter notebook EDA_analysis.ipynb
```

### 3. Run NLP model

```bash
python llama_model1.py
```

Select a **Patient ID** and enter clinical questions to extract responses.

---

## 📦 Requirements

Key Python libraries (full list in `requirements.txt`):

* `transformers==4.45.2`
* `torch==2.5.0`
* `pandas==2.2.3`
* `scikit-learn==1.5.2`
* `numpy==2.1.2`

---

## 🔮 Future Enhancements

* Expand dataset to improve generalizability.
* Fine-tune **domain-specific models** (e.g., ClinicalBERT, BioBERT).
* Enhance preprocessing (abbreviations, misspellings, shorthand).
* Explore integration with electronic health records (EHRs) as a decision-support tool.

---

## 📬 Contact

* Author: **Dhanushree Motanalira Somaiah**
* Supervisor: Prof. Jose Camacho Collados
* Cardiff University, School of Computer Science & Informatics
* LinkedIn: [linkedin.com/in/dhanushreemsomaiah](https://www.linkedin.com/in/dhanushreemsomaiah)



<img width="452" alt="EDA" src="https://github.com/user-attachments/assets/6ec490af-adff-49c6-abdc-2e2da8f3fff0" />
