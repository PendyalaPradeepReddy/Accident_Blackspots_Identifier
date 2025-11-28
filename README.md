# Accident Locations on India Roads

A Streamlit web application that visualizes accident locations across different states in India using interactive maps and data visualizations.

## Features

- Interactive map visualization of accident locations using Plotly
- State-wise accident data analysis
- Multiple visualization options (Bar Plot, Data Frame, Meta Data)
- Color-coded maps based on death counts
- Responsive wide layout design

## Prerequisites

Before running this application, make sure you have:

- Python 3.8 or higher installed
- pip (Python package installer)
- Git (optional, for cloning the repository)

## Step-by-Step Installation and Setup

### Step 1: Navigate to Project Directory

Open your terminal/command prompt and navigate to the project directory:

bash
cd "C:\Users\91934\OneDrive\Desktop\Project"


### Step 2: Create Virtual Environment (if not already created)

Create a virtual environment to isolate project dependencies:

*For Windows (PowerShell):*
powershell
python -m venv venv


*For Windows (Command Prompt):*
cmd
python -m venv venv


*For macOS/Linux:*
bash
python3 -m venv venv


### Step 3: Activate Virtual Environment

Activate the virtual environment:

*For Windows (PowerShell):*
powershell
.\venv\Scripts\Activate.ps1


*For Windows (Command Prompt):*
cmd
venv\Scripts\activate


*For macOS/Linux:*
bash
source venv/bin/activate


> *Note:* If you encounter an execution policy error in PowerShell, run:
> powershell
> Set-ExecutionPolicy -ExecutionPolicy RemoteSigned -Scope CurrentUser
> 

### Step 4: Install Required Packages

Install all required packages from the requirements.txt file:

bash
pip install -r requirements.txt


This will install:
- streamlit - Web application framework
- plotly - Interactive visualization library
- pandas - Data manipulation library

### Step 5: Verify Installation

Verify that all packages are installed correctly:

bash
pip list


You should see streamlit, plotly, and pandas in the list.

## Running the Application

### Step 1: Ensure Virtual Environment is Activated

Make sure your virtual environment is activated (you should see (venv) in your terminal prompt).

### Step 2: Run the Streamlit Application

Run the following command to start the application:

bash
streamlit run main.py


### Step 3: Access the Application

After running the command, Streamlit will:
- Start a local server
- Automatically open your default web browser
- Display the application at http://localhost:8501

If the browser doesn't open automatically, you can manually navigate to:

http://localhost:8501


### Step 4: Using the Application

1. *Select a State*: Use the dropdown menu in the sidebar to choose a state from the list
2. *View Map*: The interactive map will display accident locations for the selected state
3. *Visualizations*: Select visualization options from the sidebar:
   - *Bar Plot*: View bar chart of accidents by address
   - *Data Frame*: View the raw data in a table format
   - *Meta Data*: View information about the dataset

### Step 5: Stop the Application

To stop the application, press Ctrl + C in your terminal.

## Project Structure


Project/
│
├── main.py                 # Main Streamlit application file
├── functions.py            # Helper functions for data processing
├── requirements.txt        # Python package dependencies
├── README.md              # This file
│
├── data/                  # CSV data files directory
│   ├── indiads.csv        # India dataset
│   ├── apdataset.csv      # Andhra Pradesh dataset
│   ├── gujarathds.csv     # Gujarat dataset
│   ├── hrds.csv           # Haryana dataset
│   ├── mhds.csv           # Maharashtra dataset
│   ├── mpds.csv           # Madhya Pradesh dataset
│   ├── rajds.csv          # Rajasthan dataset
│   ├── tnds.csv           # Tamil Nadu dataset
│   ├── upds.csv           # Uttar Pradesh dataset
│   └── wbds.csv           # West Bengal dataset
│
└── venv/                  # Virtual environment (not included in git)


## Troubleshooting

### Issue: ModuleNotFoundError

*Solution:* Make sure the virtual environment is activated and all packages are installed:
bash
pip install -r requirements.txt


### Issue: FileNotFoundError for CSV files

*Solution:* Ensure the data files are in the correct directory path. Update the file path in main.py line 72 if your data is stored in a different location.

### Issue: Streamlit command not found

*Solution:* 
1. Verify virtual environment is activated
2. Reinstall streamlit: pip install streamlit

### Issue: Port 8501 already in use

*Solution:* Streamlit will automatically use the next available port, or you can specify a different port:
bash
streamlit run main.py --server.port 8502


## Requirements

- Python 3.8+
- streamlit
- plotly
- pandas

## Notes

- The application requires CSV data files to be present in the specified directory
- Make sure the data files contain columns: Longitude, Latitude, Deaths, and Address
- The file path in main.py may need to be adjusted based on your system configuration

## License

This project is for educational purposes.
