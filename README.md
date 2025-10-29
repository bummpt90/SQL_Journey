Mini Project for my Analytics Journey: Week One
# 🎬 Movie Sales Analysis – SQL Mini Project

This repository contains SQL scripts for a mini project focused on cleaning, transforming, and analyzing movie sales data. The goal is to preserve the raw dataset, prepare a cleaned version for analysis, and expose it through a view for reporting and visualization.

## 📁 Project Structure

### 1. `create_cleaned_table.sql`
**Purpose:**  
Creates an empty table `cleaned_movies.movies_sales` to store cleaned movie data. This ensures the raw dataset remains untouched for comparison and audit purposes.

**Highlights:**
- Drops existing cleaned table if it exists
- Defines schema with key fields like title, genre, budget, revenue, ROI
- Includes `Date_Updated` for tracking refreshes

---

### 2. `load_cleaned_data_procedure.sql`
**Procedure:** `cleaned_movies.movies_analysis_ready`  
**Purpose:**  
Transforms and loads cleaned data from the raw `movie.movies_sales` table into the cleaned table.

**Highlights:**
- Filters out low-revenue movies (< $100M)
- Calculates `Profit`, `Return_On_Investment`, and `Revenue_Category`
- Casts financial fields for precision
- Categorizes revenue performance (High, Moderate, Poor)

---

### 3. `create_analysis_view.sql`
**View:** `cleaned_movies.analysis_movie_ready_vw`  
**Purpose:**  
Creates a virtual table for analysts to query cleaned movie data directly.

**Highlights:**
- Exposes key fields for dashboards and reports
- Simplifies access to cleaned and enriched data
- Ideal for Tableau tools and visualizations

---

## 🚀 How to Use

1. Run `create_cleaned_table.sql` to initialize the cleaned table.
2. Execute `load_cleaned_data_procedure.sql` to populate the cleaned table.
3. Create the view using `create_analysis_view.sql` for analysis-ready access.

## 📌 Notes

- All scripts are documented with inline comments for clarity.
- Designed for Microsoft SQL Server.
- Contributions and suggestions are welcome!

---

## 👤 Author

Matthew  
GitHub: [bummpt90]  
Date: 29th October, 2025  
Version: 1.0


