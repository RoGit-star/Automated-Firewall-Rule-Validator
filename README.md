
# Automated-Firewall-Rule-Validator
Automated Firewall Rule Validator project using Python and Jupyter
=======
# Automated Firewall Rule Validator

## Overview
The Automated Firewall Rule Validator is a Python-based tool that analyzes firewall rules to identify overly permissive configurations, such as open ports and unrestricted source IP addresses. All code is contained within a **Jupyter Notebook**, making it easy to follow, run step-by-step, and generate reports.

---

## Project Structure

Automated-Firewall-Rule-Validator/ ├── data/ # Example firewall rule files (CSV/JSON) ├── reports/ # Generated validation reports (CSV) ├── notebook/ # Jupyter Notebook containing all code └── README.md
- `data/` – Store sample firewall configuration files, e.g., `sample_firewall_rule.csv`.  
- `reports/` – Stores validation output reports.  
- `notebook/` – Contains `firewall_rule_validator.ipynb` with all validation scripts and analysis.  

---

## Requirements

- **Python 3.8+**  
- Recommended: **virtual environment** for dependency isolation

# Create and activate virtual environment
python3 -m venv venv
source venv/bin/activate   # macOS/Linux

# Install dependencies
pip install pandas jsonschema jupyter tabulate

How to Run
1. Launch Jupyter Notebook:
jupyter notebook

1. Open the notebook:
notebook/firewall_rule_validator.ipynb

1. Run cells in order:
* Load firewall data (CSV or JSON)
* Validate rules for overly permissive configurations
* Flag sensitive ports (SSH 22, RDP 3389)
* Add Severity levels to each finding
* Generate summary report

1. Output reports are automatically saved to:
reports/firewall_validation_report.csv

Severity Levels
Each finding is assigned a severity ranking:
Severity	Description
High	Critical exposure (e.g., SSH/RDP open to all)
Medium	General over-permissive rule
Low	Minor deviation
Sample Output (tabulated view)
+--------+-------------------------+----------+----------------------------------------+
| RuleID | Issue                   | Severity | Description                            |
+--------+-------------------------+----------+----------------------------------------+
| 1      | Overly permissive rule  | Medium   | Rule 1 allows traffic from any source. |
| 3      | Sensitive port open to all | High  | Port 3389 is exposed globally.         |
+--------+-------------------------+----------+----------------------------------------+

References
* CIS Controls – Security best practices
* OWASP – Security guidelines for applications

Terminal Commands to Commit README.md to GitHub
After creating and saving this README.md file in the root of your project folder, run the following commands in Terminal:
# Navigate to your project folder
cd path/to/Automated-Firewall-Rule-Validator

# Stage the README.md file for commit
git add README.md

# Commit with a descriptive message
git commit -m "Add polished README.md with instructions and sample output"

# Push changes to the main branch on GitHub
git push origin main
Once done, your GitHub repository will display this README automatically on the main page.

Notes
* All validation logic is contained in the notebook; no separate Python scripts are required.
	•	You can extend this tool by adding JSON input, custom severity rules, or compliance mapping for CIS/OWASP.


Final Submission Super-Short Checklist
1. Project Structure
Make sure your folder looks like this in your local repo:
Automated-Firewall-Rule-Validator/
├── data/                  # sample CSV/JSON firewall rules
├── reports/               # generated reports (can include a sample report)
├── notebook/              # firewall_rule_validator.ipynb
└── README.md              # with instructions and terminal commands

2. Check Notebook
* All cells run top-to-bottom without errors.
* Validation logic works for both CSV and JSON.
* Severity levels are included in findings.
* Example outputs are correct and match your README table.

3. Check Sample Data
* Ensure data/sample_firewall_rule.csv is present.
* The column names match your notebook (RuleID, SourceIP, DestinationIP, Port, Protocol, Action).

4. Generate Report
* Run notebook to make sure reports/firewall_validation_report.csv is created.
* Open it to verify results make sense.

5. Commit Changes
From your project folder in Terminal:
git add .
git commit -m "Final project submission: Notebook, README, sample data, and report"
git push origin main

6. Verify GitHub Repo
* Go to: https://github.com/RoGit-star/Automated-Firewall-Rule-Validator
* Confirm:
    * README.md displays properly.
    * notebook/ folder is visible with firewall_rule_validator.ipynb.
    * data/ and reports/ folders are visible.

7. Optional Final Check
* Export the notebook as PDF (File → Download as → PDF via LaTeX or HTML → PDF) and include it in reports/ if your submission requires it.

