# -Data-Cleaning-and-Preprocessing
# Netflix Data Cleaning Project

## 📌 Project Overview
This repository contains a data cleaning pipeline for Netflix movie and TV show data. The raw dataset includes information about titles, directors, cast, countries, release years, ratings, and more. This project transforms the raw data into a clean, analysis-ready format.

## 📂 Dataset Source
**Original Dataset**: [Netflix Movies and TV Shows on Kaggle](https://www.kaggle.com/datasets/shivamb/netflix-shows)  
**File**: `netflix_titles.csv`  
**Size**: ~350KB (approx. 8,800 records as of 2021)

## 🧹 Data Cleaning Steps

### 1. Handling Missing Values
- Filled missing `country` values with the most frequent country (mode)
- Dropped rows with missing `date_added` or `rating`
- Standardized missing representations (converted "" and "NA" to NaN)

### 2. Column Standardization
- Converted `date_added` to datetime format
- Split `duration` into numeric value and unit (seasons vs minutes)
- Normalized text columns (lowercase, removed special characters)

### 3. Structural Changes
- Dropped unnecessary columns: `show_id`, `description`
- Exploded `cast` and `listed_in` into separate rows for analysis
- Created new features: `is_movie` flag, `title_length`

### 4. Quality Checks
- Validated date ranges (no future dates)
- Ensured consistent rating categories
- Removed duplicate titles

## 🛠️ Tools Used
- Python 3.8+
- Pandas (data manipulation)
- NumPy (numerical operations)
- Matplotlib/Seaborn (visual verification)

# 📜 License  
**Dataset**: [CC0 1.0 Universal (Public Domain)](https://creativecommons.org/publicdomain/zero/1.0/)  
✅ No copyright restrictions  
✅ Free to use, modify, and distribute  
✅ No attribution required (though appreciated)  


