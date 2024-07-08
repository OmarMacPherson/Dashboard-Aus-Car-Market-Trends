# Dashboard: Australia Car Market Trends

![Data Analyst Professional](https://github.com/OmarMacPherson/Dashboard-Aus-Car-Market-Trends/blob/main/Figure%201.png)

This dashboard offers a comprehensive visual analysis of the Australian automotive market, utilizing data sourced from Kaggle. The project explores vehicle listings across various Australian states, highlighting patterns in brand preferences, car features, and market distribution. The dashboard aims to provide stakeholders and automotive enthusiasts with detailed insights into the dynamics of the Australian car market as of December 2023.

# Data Source

- 📁 Dataset Updated Dec 2023: This Dashboard was built using [Kaggle](https://www.kaggle.com/datasets/nelgiriyewithana/australian-vehicle-prices/data). 

# Tech Stack Used in this project

![Data Analyst Professional](https://img.shields.io/badge/Microsoft_Excel-217346?style=for-the-badge&logo=microsoft-excel&logoColor=white)
![Data Analyst Professional](https://img.shields.io/badge/Google%20Sheets-34A853?style=for-the-badge&logo=google-sheets&logoColor=white)
![Data Analyst Professional](https://img.shields.io/badge/Todoist-E44332?style=for-the-badge&logo=todoist&logoColor=white)
![Data Analyst Professional](https://img.shields.io/badge/mac%20os-000000?style=for-the-badge&logo=apple&logoColor=white)
![Data Analyst Professional](https://img.shields.io/badge/Safari-FF1B2D?style=for-the-badge&logo=Safari&logoColor=white)
![Data Analyst Professional](https://img.shields.io/badge/Firefox_Browser-FF7139?style=for-the-badge&logo=Firefox-Browser&logoColor=white)

# Techniques Used in this Dashboard

### 1. Data Cleaning Functions:

   * **Trimming:** Utilized the **TRIM** function to clean whitespace.
   * **String Manipulation:** Employed **LEFT**, **MID**, and **RIGHT** functions for string manipulation.
   * **Conditional Logic:** Utilized **IF** statements to handle data exceptions.

### 2. Data Handling:

   * **Lenght Measurement:** Employed the **LEN** function to support the validation and formatting of data entries.
   * **Duplicates and Blanks:** Removed duplicate entries and managed blank spaces or irrelevant symbols to maintain **data integrity**.
   * **Data Type Conversions:** Converted text to numbers where necessary for accurate **data processing**.

### 3. Data Visualization:

   * **Pivot Tables:** Created to aggregate and summarize data, enabling quick **insights into trends**.
   * **Interactive Slicers:** Integrated slicers for **dynamic data exploration**, allowing users to filter data and view specific subsets.

### 3. Advanced Techniques:

   * **Charting:** Utilized various graphical representations such as **bar charts**, **pie charts**, and **scatter plots** for easy data interpretation.
   * **Conditional Formatting:** Applied to enhance **data presentation**, highlighting key figures and **outliers**.

# Formulas Used in this Project:

Data Cleaning in Column "Used or New"

```ruby
=IF(OR(F2="DEMO", F2="nan"), "USED", F2)
```

Data Cleaning in Column "Transmision"

```ruby
=IF(OR(H2="-", H2=""),"Unknown",H2)
```

Data Handling in Column "Cylinders"

```ruby
=IF(J2="-", "", LEFT(J2, FIND(" ", J2) - 1))
```

Data Handling in Column "Liters"

```ruby
=IF(J2="-", "", TRIM(MID(J2, FIND(" ", J2, FIND(" ", J2) + 1) + 1, FIND("L", J2) - FIND(" ", J2, FIND(" ", J2) + 1) - 1)))
```
Data Cleaning in Column "Fuel Type"

```ruby
=IF(OR(N2="", N2="-"),"Unknown",N2)
```

Data Cleaining in Column "Kilometres"

```ruby
=IF(Q2="-", "Unknown", Q2)
```

Data Handling in Column "State"

```ruby
=IF(T2="","Unknown",TRIM(RIGHT(T2, 3)))
```
Data Cleaning in Column "Body Type"

```ruby
=IF(X2="","Unknown",X2)
```

Data Handling in Column "Doors"

```ruby
=IF(Z2="", "", LEFT(Z2, LEN(Z2) - 6))
```

Data Handling in Column "Seats"

```ruby
=IF(AB2="","",LEFT(AB2,LEN(AB2)-5))
```

# Limitations

The primary limitation of this dataset is the lack of actual transaction dates, which constrains the ability to analyse temporal sales trends. This dataset restricts the analysis to static comparisons across different dimensions such as state, car brand, and car features at a single point in time.

# Investigative Questions

### a) What are the most popular car brands in each Australian state?

Our analysis revealed Toyota as the predominant brand across all states, a favourite highlighted by its consistent appearance in purple across our visual charts.

![Figure 2](https://github.com/OmarMacPherson/Dashboard-Aus-Car-Market-Trends/assets/170058206/6056a73c-d8c3-487b-b886-816a8f6134e4)










