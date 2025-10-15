# README: Aspect-Based Sentiment Analysis of Glassdoor Reviews

## Project Overview
This project applies Natural Language Processing (NLP) techniques to analyze employee-written Glassdoor reviews. Our aim is to detect sentiment (positive, neutral, or negative) toward five key workplace aspects:

- Work-Life Balance
- Company Culture
- Compensation & Benefits
- Career Opportunities
- Management

The project was developed by Master of Business Analytics (MBusA) students at Melbourne Business School as part of the Natural Language Processing subject. Our solution automates the classification of sentiment toward specific workplace dimensions and evaluates model performance against human-labeled ground truth.

---

## Files Included in This Archive

- `NLP Project.ipynb` – The main Python notebook containing all analysis code
- `filtered_glassdoor_reviews.csv` – The cleaned dataset used in the analysis
- `README.md` – This file, explaining how to run the code
- (Optional) Output or evaluation CSV files generated during execution

---

## How to Run This Project

### Requirements
The code is written in Python and can be run on any standard Jupyter Notebook environment. Required Python libraries:

- `pandas`
- `spacy` (with loaded `en_core_web_lg` model)
- `vaderSentiment`
- `scikit-learn`
- `statsmodels`
- `matplotlib`, `seaborn`
- `tqdm`

### Step-by-Step Instructions

1. **Open the Jupyter Notebook**  
   Launch JupyterLab or Jupyter Notebook, and open `NLP Project.ipynb`.

2. **Install the Required Packages (if not already installed)**  
   You can install the packages by running:
   ```bash
   pip install pandas spacy vaderSentiment scikit-learn statsmodels matplotlib seaborn tqdm
   python -m spacy download en_core_web_lg



3. **Run the Notebook Cells Sequentially**
   Execute each code cell in order from top to bottom. The notebook:
   - Loads the dataset
   - Preprocesses text (tokenization, lemmatization, filtering)
   - Maps frequent keywords to workplace aspects
   - Assigns sentiment using the VADER model
   - Evaluates against a gold-standard set of 200 human-annotated reviews
   - Reports precision, recall, F1-score, accuracy, and AUC
   - statistical analysis (Tukey HSD) across companies

## Notes
   This solution is fully automated and replicable. You may replace the CSV with another review dataset that has the same format
   The system does not require manual labeling beyond the provided 200-sample evaluation set.
   Evaluation is based on established sentiment classification metrics and benchmarks.
