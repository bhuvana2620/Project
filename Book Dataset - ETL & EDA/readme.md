# **Book Dataset - ETL & EDA**

## **1. Project Overview**
This project involves **Extracting, Transforming, and Loading (ETL) a book dataset** into an SQLite database, followed by **Exploratory Data Analysis (EDA)** to uncover meaningful insights about book ratings, languages, publishers, and trends over time.

## **2. Dataset Overview**
- **Source:** [Specify dataset source, e.g., Kaggle, Open Library, etc.]
- **File Used:** `transform_book.csv`
- **Size:** [Number of records & columns]
- **Key Columns:**
  - `book_id`: Unique identifier for books
  - `title`: Title of the book
  - `authors`: Author(s) of the book
  - `average_rating`: Average user rating
  - `ratings_count`: Number of user ratings
  - `num_pages`: Number of pages
  - `language_code`: Language code of the book
  - `publisher`: Publisher name
  - `publication_date`: Date of book release

## **3. ETL Process**
### **Extract**
- Loaded data from `transform_book.csv` into a Pandas DataFrame.

### **Transform**
- Handled missing values and incorrect data types.
- Converted `publication_date` to datetime format.
- Grouped ratings into bins for better analysis.

### **Load**
- Stored the cleaned data in an SQLite database (`AAK_test.db`).
- Created a table named `books` and inserted transformed data.

## **4. Exploratory Data Analysis (EDA)**
### **Univariate Analysis**
- **Distribution of Ratings**
  - Majority of books have ratings between **3.0 - 4.5**, suggesting most users rate books positively.
  - Grouped ratings into intervals for better visualization.
- **Language Distribution**
  - English dominates the dataset, with significantly fewer books in other languages.

### **Bivariate Analysis**
- **Correlation Between Ratings & Number of Reviews**
  - Books with higher `ratings_count` tend to have **more stable and higher ratings**.
- **Effect of Number of Pages on Ratings**
  - No strong correlation between `num_pages` and `average_rating`, indicating book length does not affect how well a book is rated.

### **Publisher & Author Analysis**
- **Top Publishers by Number of Books**
  - A few publishers dominate book production.
- **Top Authors by Number of Books**
  - Some authors have a significantly higher number of published books.

### **Trends Over Time**
- **Yearly Publication Trends**
  - The number of books published has **increased over time**, with fluctuations in certain years.

## **5. Key Insights**
- ✅ Users tend to give books positive ratings** (mostly between 3.0-4.5).\
- ✅ Books with more ratings tend to have higher and stable ratings**.\
- ✅ English is the most common language** in the dataset.\
- ✅ Book length does not strongly affect its rating**.\
- ✅ A few publishers and authors dominate the dataset**, influencing book availability.\
- ✅ The number of books published has increased over time**, indicating market growth.

## **6. Repository Structure**
```bash
/project-directory
│── books.csv                # Actual Uncleaned file
│── AAK-EDA.ipynb            # Jupyter notebook for analysis
│── AAK-test.ipynb           # Jupyter notebook for ETL
│── transform_book.csv       # Cleaned dataset
│── AAK_test.db              # SQLite database
│── README.md                # Project documentation (this file)
```

## **7. How to Run**
1. Clone this repository  
   ```bash
   git clone https://github.com/bhuvana2620/Project.git
   cd Book Dataset - ETL & EDA
   ```
2. Install dependencies  
   ```bash
   pip install pandas numpy matplotlib seaborn sqlite3
   ```
3. Open the Jupyter Notebook and execute the steps  

## **8. Future Improvements** 
- 🔹 Develop a **recommendation system** using collaborative filtering.
- 🔹 Develop a **interactive dashboard** using any visualization platforms.
---

