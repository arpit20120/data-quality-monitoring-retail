# Retail Data Quality Monitoring Platform

This project is a lightweight, modular Python framework designed to monitor and report data quality issues in retail sales datasets. It automatically detects null values, duplicates, and statistical outliers — with clean logging and Markdown summaries for quick review.

## Features

- Null checks across all columns
- Duplicate detection based on `transaction_id`
- Outlier detection using z-score on `revenue` and `unit_cost`
- Timestamped CSV log of each run
- Markdown summary report (GitHub-friendly)

## Project Structure

data-quality-monitoring-retail/
├── data/                     # Input dataset (fact_sales_clean.csv)  
├── reports/                  # Output logs and summary  
│   ├── dq_log.csv  
│   └── dq_summary.md  
├── scripts/  
│   ├── data_quality_checker.py  
│   ├── rules/  
│   │   ├── null_check.py  
│   │   ├── duplicate_check.py  
│   │   └── outlier_check.py  
│   └── utils/                # Optional utilities (logger, alert system)  
└── README.md

## How to Run

From the project root:

```

python scripts/data\_quality\_checker.py

````

Or from a Jupyter Notebook:

```python
from scripts.rules.null_check import check_nulls
from scripts.rules.duplicate_check import check_duplicates
from scripts.rules.outlier_check import check_outliers
````

# Sample Markdown Output

```
# Data Quality Report – 2025-06-23 20:13:54

- Passed: null_check on `region` – 0 rows affected
- Issue: duplicate_check on `transaction_id` – 8 rows affected
- Issue: outlier_check on `revenue` – 12 rows affected
```

# Skills Demonstrated

* Python scripting and automation
* Modular rule-based validation framework
* Markdown and CSV-based logging
* Real-world ETL and QA logic
* GitHub-ready documentation

# Use Cases

* Health checks for ETL pipelines
* Data warehouse QA
* Demonstrating data engineering skills for interviews

Created and maintained by Arpit Sharma

```
