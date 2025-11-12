#  Resume & Career Coach LLM

**Fine-tuned Large Language Model (LLM) that analyzes resumes, identifies strengths and areas for improvement, and suggests ideal career paths and skills — powered by Unsloth LoRA fine-tuning.**

---

##  Project Overview

This project uses **Unsloth + LoRA fine-tuning** to create a lightweight, domain-specific **Career Coach LLM**.  
It is trained on datasets containing resume text and skill–career mappings to provide intelligent, personalized feedback on resumes.

###  Features
-  Analyzes resumes and evaluates them on structure, content, and skills  
-  Suggests ideal job roles and upskilling paths  
-  Provides a resume score out of 100  
-  Fine-tuned using open-source and curated resume datasets  

---

## 📁 Dataset Details

| Dataset | Description |
|----------|--------------|
| **UpdatedResumeDataSet.csv** | Labeled resumes and candidate skill data |
| **Dataset Project 404.xlsx** | Mappings between courses, intelligence types, and career roles |
| **career_coach_dataset.jsonl** | Final formatted dataset used for LoRA fine-tuning |

---

##  Model Architecture

- **Base Model:** `unsloth/mistral-7b-instruct-v0.3-bnb-4bit`  
- **Fine-tuning Framework:** [Unsloth](https://github.com/unslothai/unsloth)  
- **Technique:** LoRA (Low-Rank Adaptation)  
- **Environment:** Google Colab (GPU)  
- **Optimization:** 4-bit quantization for reduced memory usage  

---

##  Tech Stack

| Category | Tools Used |
|-----------|-------------|
| **ML / AI** | Unsloth, Transformers, PyTorch |
| **Data Processing** | Pandas, NumPy |
| **Visualization** | Matplotlib, Seaborn |
| **Deployment / UI (optional)** | Gradio |
| **Environment** | Google Colab, Hugging Face, VS Code |

---

##  Setup Instructions

### 1️. Clone the Repository
git clone https://github.com/anerudhh/resume-guidance-llm.git
cd resume-guidance-llm

2️. Create a Virtual Environment
bash
Copy code
python -m venv venv
Activate it:

Windows: venv\Scripts\activate

Mac/Linux: source venv/bin/activate

3️. Install Dependencies
bash
Copy code
pip install -r requirements.txt
4️. Run the Notebook
Open and execute fine_tune_colab.ipynb in Jupyter or VS Code to:

Prepare datasets

Fine-tune the model using LoRA

Evaluate outputs

💬 Inference Example
python
Copy code
prompt = """
You are an AI career coach.
Analyze the resume below and respond with:
1. Resume score out of 100
2. Career strengths
3. Improvements
4. Ideal roles and skills
ask(prompt)


![WhatsApp Image 2025-11-06 at 23 37 56_f3de6d35](https://github.com/user-attachments/assets/66ced6bf-6d2b-41d2-bcd2-49ac314c5830)
![WhatsApp Image 2025-11-06 at 22 25 33_e5cf49ba](https://github.com/user-attachments/assets/515a0d5a-21f5-409b-9da4-3c645e56ddec)
![WhatsApp Image 2025-11-06 at 22 23 19_03e42d77](https://github.com/user-attachments/assets/f475c063-3088-42ef-b953-d14f09c97985)




Results
Metric	Observation
Dataset Size	~1000 samples
Fine-tuning Epochs	3
Average Response Quality	High contextual accuracy
Memory Usage	Optimized with 4-bit quantization
