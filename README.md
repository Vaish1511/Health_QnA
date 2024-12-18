# HealthQnA Project

## Overview
HealthQnA is a healthcare-focused chatbot application designed to assist users with medical concerns by:

1. Classifying user-reported symptoms.
2. Generating targeted medical interview questions.
3. Conducting detailed interviews and analysis.
4. Creating root-cause analyses (Ishikawa diagrams).
5. Analyzing health report images.

The project is specifically focused on four disease categories:
- Diabetes
- Blood Pressure (Hypertension)
- Stomach-related issues
- Skin conditions

The application utilizes state-of-the-art AI technologies, including LLMs (Llama and Gemini), machine learning, and OCR for extracting text from images.

## Features

1. **Symptom Classification**
   - Utilizes a Sentence Transformer to classify medical intents based on user-provided symptoms.

2. **Medical Interview Generation**
   - Generates a sequence of questions to gather more information about a user's condition.

3. **Comprehensive Analysis**
   - Provides potential diagnoses, recommended tests, lifestyle advice, and warning signs requiring immediate attention.

4. **Root-Cause Analysis**
   - Generates enhanced fishbone diagrams for visualizing potential causes of a medical condition.

5. **Health Report Analysis**
   - Extracts and analyzes text from health reports using OCR and the Gemini model.

## Requirements

### Libraries
The following Python libraries are required:

- `langchain==0.1.0`
- `langchain-community==0.0.10`
- `transformers==4.36.2`
- `scikit-learn==1.3.2`
- `google-generativeai==0.3.1`
- `matplotlib==3.8.2`
- `seaborn==0.13.0`
- `streamlit==1.29.0`
- `torch==2.1.2`
- `numpy==1.26.2`
- `faiss-cpu==1.7.4`
- `chromadb==0.4.18`
- `sentence-transformers==2.2.2`
- `python-dotenv==1.0.0`
- `Pillow`
- `pytesseract`

### Environment Configuration

- Set up the following environment variables:
  - `HUGGINGFACEHUB_API_TOKEN`
  - `GEMINI_API_KEY`

### External Dependencies

- **Tesseract OCR**: Install Tesseract OCR using your package manager (e.g., `sudo apt install tesseract-ocr`).

## Files

### 1. `HealthCareChatBot.py`
   - Main backend script for:
     - Symptom classification
     - Medical interview generation
     - Root-cause and comprehensive analysis

### 2. `updated_app2.py`
   - Streamlit-based web interface for:
     - Chatbot interactions
     - Uploading health reports
     - Displaying analyses and fishbone diagrams

### 3. `health_report_analyzer.py`
   - Command-line utility for analyzing health report images.

## Installation

1. Clone the repository.
2. Install Python dependencies:
   ```bash
   pip install -r requirements.txt
   ```
3. Ensure Tesseract OCR is installed:
   ```bash
   sudo apt install tesseract-ocr
   ```

## Usage

### Web Interface
1. Run the Streamlit app:
   ```bash
   streamlit run updated_app2.py
   ```
2. Interact with the chatbot and upload health reports.

### Command-Line Tool
1. Analyze a health report image:
   ```bash
   python health_report_analyzer.py <path_to_image>
   ```

### Development
1. Use the `HealthCareChatBot.py` for backend development.
2. Update the UI via `updated_app2.py`.

## Updated `requirements.txt`
```plaintext
langchain==0.1.0
langchain-community==0.0.10
transformers==4.36.2
scikit-learn==1.3.2
google-generativeai==0.3.1
matplotlib==3.8.2
seaborn==0.13.0
streamlit==1.29.0
torch==2.1.2
numpy==1.26.2
faiss-cpu==1.7.4
chromadb==0.4.18
sentence-transformers==2.2.2
python-dotenv==1.0.0
Pillow==10.0.0
pytesseract==0.3.10
```


---
**Note**: Replace `<path_to_image>` with the path to your health report image when using the CLI tool.


