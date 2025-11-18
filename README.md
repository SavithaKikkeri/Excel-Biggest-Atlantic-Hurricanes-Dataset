# Biggest Atlantic Hurricanes Analysis 🌀

## Project Overview
This Excel project provides a comprehensive dataset and analysis of the most significant hurricanes in Atlantic history. The workbook tracks historical storm data, including dates, financial impact, and intensity categories.

## 📂 Dataset Structure
The main dataset includes the following key metrics for each hurricane:
* **Name:** The official name of the hurricane.
* **Start Date:** The date the storm began.
* **Damage (USD Millions):** The estimated financial impact of the storm at the time.
* **Category:** The Saffir-Simpson hurricane scale rating (1-5).
* **Max Wind Speed:** The maximum sustained wind speeds recorded.

## 🌪️ Data Preview
Here is a sample of the data contained in the spreadsheet:

| Name | Start Date | Damage (USD Millions) | Category | Max Wind Speed (mph) |
| :--- | :--- | :--- | :--- | :--- |
| **San Marcos** | October 5, 1870 | 12 | 3 | 129 |
| **Sea Islands** | August 15, 1893 | 1 | 3 | 129 |
| **Chenier Caminanda** | September 27, 1893 | 5 | 4 | 156 |
| **San Ciriaco** | August 3, 1899 | 20 | 4 | 156 |
| **Galveston** | August 27, 1900 | 20 | 4 | 156 |

## ⚡ Key Excel Features

### The `SWITCH` Function
This project utilizes the **`SWITCH`** function to streamline complex logic, replacing older, messier nested `IF` statements.

In this context, `SWITCH` is likely used to automatically determine the **Wind Speed Range** or a **Severity Label** based on the Hurricane Category.

<img width="382" height="155" alt="image" src="https://github.com/user-attachments/assets/052d2a17-88f3-4a17-8d2b-3bb1422a0e69" />


**Example Logic:**
Instead of writing multiple `IF` statements, the `SWITCH` function evaluates the Category (e.g., cell `D2`) and returns the corresponding Wind Speed:

```excel
=SWITCH(D2, 
   1, "74-95 mph", 
   2, "96-110 mph", 
   3, "111-129 mph", 
   4, "130-156 mph", 
   5, "157 mph or higher", 
   "Unknown"
)
