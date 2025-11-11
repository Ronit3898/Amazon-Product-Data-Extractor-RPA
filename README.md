# Amazon-Product-Data-Extractor-RPA
UiPath bot that automates Amazon product data extraction for laptops and mobiles, merges results, and sends a consolidated report via email.


# 🤖 Amazon Product Data Extraction Bot | UiPath RPA Project

An end-to-end automation bot built using **UiPath** that extracts product details from **Amazon** for multiple product categories (Laptops and Mobiles).  
The bot reads input data from Excel files, scrapes product information automatically from Amazon, merges the extracted results, and sends the final report to the client via email.

---

## 🚀 Project Overview

This RPA solution automates the process of:
1. Logging into Amazon using stored credentials.
2. Searching for product names (from Excel input files).
3. Extracting product information dynamically.
4. Merging the collected data from multiple sources.
5. Sending the final report via email automatically.

This project demonstrates how UiPath can streamline **data scraping**, **Excel automation**, and **email integration** for real-world business use cases.

---

## 🧠 Workflow Summary

### **Input Files**
The bot uses two Excel files as input:
- `Input_Laptop.xlsx`
- `Input_Mobile.xlsx`

Each input file contains **5 product keywords** (e.g., Model Name, Product Name, Model Type, etc.).  
The bot performs searches for each keyword and extracts **10 product results per search**.

### **Process Steps**
1. Launch **Google Chrome** and navigate to **Amazon.in**.
2. Perform **Login** using stored credentials.
3. For each category (Laptop & Mobile):
   - Read search inputs from the corresponding Excel file.
   - Perform Amazon search for each keyword.
   - Extract top 10 product results including:
     - Product Name  
     - Model  
     - Price  
     - Rating  
     - Brand (and other available attributes)
   - Save all extracted data to a category-specific Excel file:
     - `Output_Laptop.xlsx`
     - `Output_Mobile.xlsx`
4. Merge both output files into one consolidated report:
   - `Master_Output.xlsx` (contains 100 rows in total)
5. Use **SMTP Mail Activity** to send the final Excel report automatically to the client.

---

## 🧰 Tech Stack & Tools

| Component | Description |
|------------|-------------|
| **Tool** | UiPath Studio |
| **Language** | Visual Basic (XAML) |
| **Browser** | Google Chrome |
| **Data Source** | Excel (Laptop & Mobile inputs) |
| **Output Format** | Excel (.xlsx) |
| **Mail Integration** | SMTP Email Activity |
| **Automation Modules** | Data Scraping, Excel Automation, Merge, Email Automation |

---

## 📁 Project Structure

