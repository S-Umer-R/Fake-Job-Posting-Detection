# Fake Job Posting Detection

## Overview
This GitHub repository contains a machine learning project focused on detecting fake job postings. The project utilizes a RandomForestClassifier and various data visualization techniques to analyze and classify job postings as either fraudulent or non-fraudulent.

## Dataset
The dataset used in this project is loaded from an Excel file (`FakeJobPostings.xlsx`). It includes information about job postings, such as job title, company details, job description, and more.

## Data Preprocessing and Visualization
1. **Handling Null Values:** Columns with no importance or containing many null values are removed. Null values in the remaining columns are replaced with spaces.
2. **Visualization:**
    - The total number of fraudulent and non-fraudulent cases is visualized using a countplot.
    - The distribution of required experience is visualized using a bar chart.
    - Country-wise job postings and education-wise job postings are visualized to gain insights.

## Text Processing and Feature Engineering
1. **Extracting Country Information:** A new 'country' column is created by extracting the country from the 'location' column.
2. **WordClouds:** WordClouds are generated for both fraudulent and non-fraudulent job postings, providing a visual representation of the most frequent words in each category.
3. **Text Cleaning:** Punctuation marks and stop words are removed, and text is lemmatized using spaCy.

## Machine Learning Model
1. **Feature Extraction:** The text data is converted into vectors using TF-IDF Vectorization, resulting in a DataFrame (`main_df`) with the top 100 features.
2. **Model Training:** A RandomForestClassifier is trained on the data with 70% used for training and 30% for testing.
3. **Model Evaluation:**
    - Training accuracy and out-of-bag (OOB) score are calculated.
    - Accuracy, classification report, and confusion matrix are generated for the test dataset.

## Repository Structure
- **fake_job_detection.ipynb:** Jupyter Notebook containing the entire code.
- **FakeJobPostings.xlsx:** Excel file containing the dataset.
- **README.md:** Documentation providing an overview, setup instructions, and explanations.

## Instructions
To run the code locally:
1. Clone the repository.
2. Install the required dependencies mentioned in the notebook.
3. Run the notebook (`fake_job_detection.ipynb`) in a Jupyter environment.

Feel free to explore and enhance the project by experimenting with different algorithms, hyperparameters, or additional features to improve the model's performance. Contributions and feedback are welcome!
