# Resume Analyzer

This project extracts text from a resume PDF and uses Google Generative AI to analyze the resume for strengths, weaknesses, and skill recommendations.

## Features

- Extracts text from PDF resumes using `pdfplumber` and OCR fallback with `pytesseract` and `pdf2image`.
- Integrates with Google Generative AI (Gemini) to provide professional resume analysis.
- Optionally compares the resume against a provided job description.

## Setup

1. **Install dependencies**  
   Run the following commands in your Jupyter notebook cells:
   ```python
   %pip install pdfplumber pytesseract pdf2image google.generativeai python-dotenv
   ```

2. **Google API Key**  
   Add your Google Generative AI API key to a `.env` file:
   ```
   GOOGLE_API_KEY=your_api_key_here
   ```

3. **Add your resume**  
   Place your resume PDF in the project directory and name it `Resume.pdf`.

## Usage

1. **Extract text from PDF**
   ```python
   pdf_path = "Resume.pdf"
   resume_text = extract_text_from_pdf(pdf_path)
   print(resume_text)
   ```

2. **Analyze resume**
   ```python
   print(analyze_resume(resume_text))
   ```

3. **Compare with job description (optional)**
   ```python
   job_description = "Paste job description here"
   print(analyze_resume(resume_text, job_description))
   ```

## File Structure

- `resume_analyzer.ipynb` – Main Jupyter notebook for extraction and analysis.
- `.env` – Stores your Google API key.
- `Resume.pdf` – Your resume file.

## Requirements

- Python 3.13+
- Jupyter Notebook

## License

This project is for educational and personal use.
