# AUTOMATED-REPORT-GENERATION

**COMPANY**:CODTECH IT SOLUTIONS
**NAME**:SHEEZ MUHAMMED C
**INTERN ID**:CT08NAH
**DOMAIN**:PYTHON
**BATCH DURATION**:January 15th/2025 to February 15th/2025

**DESCRIPTION**

Data Analysis Report Generator

Overview

This Python script is designed to read data from a CSV file, analyze it, and generate a well-formatted PDF report. It leverages the pandas library to process and analyze the dataset and the fpdf library to create a structured PDF report. The script is useful for automating data analysis and report generation, making it ideal for professionals and researchers who work with structured data.

How It Works

1. Reading and Analyzing Data

The script first reads the input CSV file using the pandas library. The function analyze_data() loads the dataset into a DataFrame and then computes summary statistics using describe(). This provides insights into the dataset, such as mean, standard deviation, minimum, and maximum values. The summary includes all data types, ensuring both numerical and categorical columns are considered.

2. Generating a PDF Report

Once the data analysis is complete, the script generates a structured PDF report using the FPDF library. The generate_pdf_report() function performs the following tasks:
	•	Creates a new PDF document: A fresh PDF file is initialized with auto page breaks enabled to prevent text overflow.
	•	Adds a title: The title “Data Analysis Report” is centered at the top of the page using a bold font.
	•	Generates table headers: The column names from the summary statistics are used as table headers, formatted in bold.
	•	Populates the table: The computed summary statistics are added row by row, ensuring numerical values are rounded for readability.
	•	Saves the PDF: The final formatted report is saved as a PDF file in the specified location.

Installation and Dependencies

To run this script, ensure that Python and the required dependencies are installed. Install the necessary libraries using:

pip install pandas fpdf

Usage
	1.	Prepare a CSV File
	•	Ensure you have a CSV file (data.csv) containing structured data in the same directory as the script.
	2.	Run the Script
	•	Execute the script using:

python script.py


	3.	View the Generated Report
	•	The script will create a file named report.pdf containing the data analysis summary.

Code Structure

1. analyze_data(file_path)
	•	Reads the CSV file into a pandas DataFrame.
	•	Computes summary statistics using df.describe(include="all").
	•	Returns the original dataset and summary statistics.

2. generate_pdf_report(summary, output_file)
	•	Initializes an FPDF object.
	•	Adds a title and formatted table to the PDF.
	•	Iterates through the summary statistics and writes data into table cells.
	•	Saves the output as a PDF file.

3. Main Execution Block
	•	Specifies the input CSV file (data.csv) and output PDF file (report.pdf).
	•	Calls analyze_data() to process the data.
	•	Calls generate_pdf_report() to create the report.
	•	Handles potential errors gracefully using a try-except block.

Error Handling

The script includes basic error handling to catch and display errors related to file reading and data processing. If an invalid file path is provided or the CSV file is not properly formatted, the script will print an error message and exit gracefully.

Future Enhancements
	•	Add Data Visualization: Generate charts/graphs using matplotlib and embed them in the PDF report.
	•	Customizable Report Format: Allow users to specify font styles, colors, and layouts.
	•	Dynamic File Input: Accept CSV file paths via command-line arguments.
	•	Support for Large Datasets: Implement pagination in the PDF report for better readability.

Conclusion

This script automates the process of analyzing a dataset and generating a professional PDF report. It is a simple yet powerful tool for data analysis, providing quick insights in a structured format. By integrating additional features, such as visualization and customization options, this script can be extended to handle more complex reporting needs.
