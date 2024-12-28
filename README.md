SMOTE Data Generator

This tool generates synthetic data using the SMOTE (Synthetic Minority Oversampling Technique) to balance imbalanced datasets. It supports both Excel (.xlsx) and CSV (.csv) files and dynamically detects numeric and binary columns for feature synthesis. The results are displayed in a table on the webpage.
Features

    File Support: Accepts both Excel and CSV files.
    Target Column Specification: Allows users to specify the target class column by name.
    Synthetic Sample Generation: Users can define the number of synthetic samples to generate for the minority class.
    Automatic Column Detection:
        Numeric columns are interpolated.
        Binary columns (e.g., 0/1 or 1/2) are rounded to maintain valid values.
    Results Display: Synthetic data is shown in a dynamic HTML table on the webpage for easy review.

Installation

    Download the HTML file for the SMOTE Data Generator tool.
    Ensure you have an up-to-date browser (e.g., Chrome, Firefox, Edge).

How to Use
1. Open the Tool

    Open the HTML file in your preferred browser.

2. Upload a File

    Click on the "Upload Your File (Excel or CSV)" button and upload a dataset containing numeric features and a target class column.

3. Specify Inputs

    Target Class Column Name: Enter the name of the column representing the target class (e.g., Class, Target, or Label).
    Number of Synthetic Samples: Enter the number of synthetic data rows you want to generate.

4. Generate Synthetic Data

    Click the "Generate Synthetic Data" button to start the process.

5. View Results

    The synthetic data will be displayed in a table on the webpage:
        Numeric Features: Interpolated between random samples.
        Binary Features: Rounded to ensure valid binary values.
        Target Class: The synthetic samples are assigned the minority class value.

Input Descriptions
Input	Description
Upload File	Upload an Excel or CSV file containing your dataset.
Target Column Name	Enter the name of the target column (e.g., Class). The tool dynamically detects the column by name.
Number of Samples	Enter the desired number of synthetic samples to generate for the minority class.
Output Description

The generated synthetic data is displayed in a table format with the following details:

    Numeric Columns: Values interpolated between two random samples from the minority class.
    Binary Columns: Values rounded to maintain valid binary representation (e.g., 0 or 1, 1 or 2).
    Target Column: All synthetic rows are assigned the minority class label.

Example Usage
Input Example:
Feature 1	Feature 2	Feature 3	Class
2.3	4.5	1	0
1.8	3.9	0	1
2.1	4.0	1	0

    Target Column Name: Class
    Number of Synthetic Samples: 5

Output Example:
Feature 1	Feature 2	Feature 3	Class
2.3	4.5	1	0
1.8	3.9	0	1
2.1	4.0	1	0
1.9	4.2	0	1
2.0	4.1	1	1
Limitations

    The tool assumes the dataset contains at least one numeric column for interpolation.
    Binary columns are identified dynamically but must have exactly two unique values (e.g., 0/1 or 1/2).

Technologies Used

    HTML/CSS: For creating the user interface.
    JavaScript: For implementing SMOTE and processing data.
    XLSX.js: For parsing Excel files.
    Math.js: For mathematical operations like interpolation.

License

This project is open-source and available for modification and reuse. Attribution to the original developer is appreciated.
