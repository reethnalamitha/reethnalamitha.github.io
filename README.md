📊 iCognative Mini Scraper

A Python-based automation tool to log in to the iCognative Mini application, fetch case data, run analysis using selected engines, and export results in structured formats like Excel and JSON.

🚀 Features:

  🔐 Secure login using user credentials
  📋 Fetches all available cases from the application
  🎯 Flexible case selection:
  Single case (5)
  Range of cases (5-10)
  Multiple cases (5,7,9)

⚙️ Supports 7 analysis engines (user-selectable)
🔄 Automatically processes all trials in selected cases

📈 Extracts key analysis metrics:
  Determination
  Confidence score
  Number of trials

📤 Export options:
  Excel (.xlsx)
  JSON (.json)
  Both / None

🧠 How It Works
  Login
  User enters email and password manually.
  Script authenticates and retrieves access token.
  Fetch Cases
  Retrieves all cases associated with the logged-in user.
  Case Selection
  User specifies which cases to analyze (single/range/multiple).
  Engine Selection
  Choose an analysis engine (1–7).
  Data Processing

Fetches:
  Test setups
  Trial data
  Runs analysis API for each trial.
  Includes retry logic for timeouts.
  Result Structuring
  
Collects:
  Trial number
  Determination
  Confidence (%)
  Presentation count
  
Export
  Excel:
    Case Details Sheet
    Analysis Results Sheet
  JSON:
    Structured nested output
    
📂 Output Format
  📘 Excel Sheets
  
1. Case Details
  Field	Description
  Case #	Case number
  Case Name	Name of the case
  Setup Name	Test setup
  Subject	Subject name
  Total Trials	Number of trials

2. Analysis Results
  Field	Description
  Trial #	Trial index
  Case #	Case number
  Test ID	Trial ID
  Number of Trials	Presentation count
  Determination	Abbreviated result
  Confidence (%)	Confidence score

🧾 Determination Mapping
Full Value	                        Abbreviation
Present	                                 P
Absent	                                 A
Indeterminate Present	                   IP
Indeterminate Absent	                   IA

🛠️ Installation

pip install requests pandas openpyxl

⚠️ pandas is required for Excel export.

▶️ Usage
python scraper.py

Inputs Required:

Email & Password (inside script)
Case selection (e.g., 1, 1-5, 1,3,7)
Engine number (1–7)
Export option:
1 → Excel
2 → JSON
3 → Both
4 → Skip

📦 Example Output Files
cases_1_2_3_engine_1_analysis.xlsx
cases_1_2_3_engine_1_analysis.json
