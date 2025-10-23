# Education Performance Analysis.

> Is school performance, measured by the average ACT score, predicited more strongly by socioeconomic factors or by the ratio of students to teachers?

---

## Project Overview

> This study investigates whether the student–teacher ratio has as strong an influence on average ACT performance as socioeconomic factors. The analysis examined relationships among socioeconomic factors, school staffing, and academic outcomes. Correlation and regression analyses revealed that socioeconomic variables were far stronger predictors of average ACT scores within the data.

- **Objective:**
  - To determine whether the student–teacher ratio has as strong an influence on ACT performance as socioeconomic factors.
- **Domain:**
  - Education analytics, data science.
- **Key Techniques:**
  - Data cleaning and merging (pandas), exploratory data analysis (EDA), correlation analysis, regression modeling (OLS), and hypothesis testing.

---

## Project Structure

```
├── data/                 # Raw and processed data
├── code/                 # Jupyter notebooks and Python scripts
├── reports/              # Generated reports and visualizations
├── requirements.txt      # Dependencies
└── README.md             # Project documentation
```

---

## Data

- **Source:** https://www.edgap.org/#5/37.875/-96.987
- **Description:**
  - **Features:**
    - NCESSCH School ID: National Center for Education Statistics school identification number
    - CT Unemployment Rate: Census tract unemployment rate
    - CT Pct Adults with College Degree: Census tract percentage of adults with a college degree
    - CT Pct Children In Married Couple Family: Census tract percentage of children in a married couple family
    - CT Median Household Income: Census tract median household income in dollars
    - School ACT average (or equivalent if SAT score): Average ACT score for the school. If the average SAT score is reported by the school, it is converted to an equivalent ACT score. Scores range from 1 - 36, with 36 being the highest.
    - (https://web.archive.org/web/20160123183428/http://act.org/solutions/college-career-readiness compare-act-sat)
    - School Pct Free and Reduced Lunch: Percentage of students at the school eligible for free or reduced price lunch.
  - **Format:** Excel (.xlsx)

- **Source:**

  - https://nces.ed.gov/ccd/pubschuniv.asp
  - https://nces.ed.gov/ccd/files.asp#FileNameId:11,VersionId:24,FileSchoolYearId:31,Page:1
- **Description:**
  - **Partial Features:**
    - SCHOOL_YEAR: Academic year
    - STATENAME: State name
    - SCH_NAME: School name
    - NCESSCH: National Center for Education Statistics school identification number
    - LSTATE: State name abbreviation
    - LZIP: Zip code
    - SCH_TYPE_TEXT: Type of school
    - LEVEL: Level of school (high school, middle school, elementary school)
    - CHARTER_TEXT: Whether the school is a charter school or not (Yes, No)
  - **Format:** .csv

---

## Analysis

- Data Integration: Merging EdGap and CCD datasets using the 12-digit NCESSCH school ID.
- Cleaning & Preparation: Standardizing data types, handling missing values, and verifying merge accuracy.
- Exploratory Data Analysis: Visualizing variable distributions and relationships using seaborn and matplotlib.
- Statistical Modeling: Correlation analysis, single and multiple variable linear regression, ANOVA tests to compare model performance.

-

---

## Results

- **Findings:**
  - Socioeconomic factors, especially the percentage of students receiving free or reduced-price lunch, were the strongest predictors of ACT performance.
  - The student–teacher ratio showed almost no linear correlation with ACT scores.
  - The most robust single-variable model percent lunch achieved an R-squared of 0.614.
  - A reduced multiple regression model using only significant predictors achieved an R-squared of 0.628.
- **Conclusion:**
  - Socioeconomic factors have far stronger influence on average ACT score than student to staff ratio.

---

## Authors

- Travis St Peter - [TravisStPeterSU](https://github.com/TravisStPeterSU)

---

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

## Acknowledgements

- Libraries
  - pandas, numpy, matplotlib, seaborn, calendar, scipy, statsmodels.