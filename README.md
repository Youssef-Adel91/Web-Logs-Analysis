# 🛡️ Web Server Access Logs Analysis & Security Insights

![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)
![Pandas](https://img.shields.io/badge/Pandas-Data%20Engineering-green.svg)
![Regex](https://img.shields.io/badge/Regex-Data%20Parsing-orange.svg)

## 📌 Project Overview
This project focuses on **Data Engineering and Security Analysis**. It involves parsing unstructured, raw Nginx web server access logs (originally 3.5 GB) into a structured format using Regular Expressions (Regex). The parsed data is then enriched and analyzed to extract actionable cybersecurity and performance insights, such as detecting potential bots, analyzing website health, and identifying peak traffic hours.

## 💾 Dataset
The data used in this project consists of Nginx server logs and client hostnames.
* **Download the dataset here:** [Web Server Access Logs on Kaggle](https://www.kaggle.com/datasets/eliasdabbas/web-server-access-logs)

*(Note: Download both `access.log` and `client_hostname.csv` and place them in the project directory before running the code).*

## 🎯 Business & Security Questions Answered
* **Cybersecurity:** Which IP addresses are making an unusually high number of requests? (Identifying potential bots, crawlers, or scrapers).
* **Website Health:** What is the ratio of successful requests (HTTP 200) to errors (e.g., HTTP 404)?
* **Server Performance:** At what time of day does the server experience the most traffic? (Peak hour analysis for server scaling).

## 🛠️ Tech Stack & Libraries
* **Language:** Python
* **Data Parsing & Extraction:** `re` (Regular Expressions)
* **Data Manipulation & Enrichment:** `pandas`, `numpy`
* **Data Visualization:** `matplotlib`, `seaborn`

## 🚀 Key Features & Workflow

### 1. Data Parsing (Unstructured to Structured)
* Used advanced **Regex** to break down complex log lines into functional columns: `IP Address`, `Timestamp`, `HTTP Method`, `URL`, `Status Code`, and `Response Size`.

### 2. Data Cleaning & Feature Engineering
* Handled data type casting (converting status codes and sizes to integers).
* Converted raw text timestamps into Python `datetime` objects to extract the exact hour of the day.

### 3. Data Enrichment (Joining Datasets)
* Performed a **Left Join** to merge the server logs (`access.log`) with the `client_hostname.csv` dataset based on the IP address. This step was crucial to translate raw IPs into identifiable hostnames (e.g., distinguishing a regular user from `googlebot.com`).

### 4. Exploratory Data Analysis (EDA)
* **Traffic Analysis:** Visualized the top 10 most active IP addresses.
* **Status Code Distribution:** Created a breakdown of server responses to monitor broken links and server health.
* **Time Series Analysis:** Plotted hourly traffic to visualize server load over a 24-hour period.

## 📊 Visualizations & Dashboards

*(Note: Add your screenshots here by dragging and dropping them into the GitHub editor)*

* **Top 10 IP Addresses (Bot Detection):** ![Bar Chart Placeholder](link_to_your_image.png)
* **Website Health (Status Codes):** ![Pie/Bar Chart Placeholder](link_to_your_image.png)
* **Traffic Peak Hours:** ![Line Chart Placeholder](link_to_your_image.png)

## 💻 How to Run This Project
1. Clone the repository:
   ```bash
   git clone [https://github.com/yourusername/web-server-logs-analysis.git](https://github.com/yourusername/web-server-logs-analysis.git)
