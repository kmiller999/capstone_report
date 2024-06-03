# Capstone Report

This project analyzed how typical experience levels (entry-level, mid-level, senior, or executive) varied between different job subcategories (e.g., data analysis, data engineering) in data science. The results have broader implications for what experience levels may be necessary for each type of data science job, particularly for those in the entry-level, who may have fewer options. Further analyses predicted job salary from available factors (data science job subcategory, experience level, or work setting), which further characerized the field at large. 

The [rendered .html version](https://kmiller999.github.io/ds_portfolio/posts/capstone_report/code/capstone_report.html) of this project is available in my data science portfolio.

## Data Source

The data used in this project ([Jobs and Salaries in Data field 2024](https://www.kaggle.com/datasets/murilozangari/jobs-and-salaries-in-data-field-2024)) was made publicly available on Kaggle by [murilozangari](https://www.kaggle.com/murilozangari). This dataset was licensed under the Apache License, Version 2.0, which is available within the data directory of this project (see [LICENSE-2.0.txt](./data/LICENSE-2.0.txt) for more details.)

## Data Processing

 - Data was filtered to only include U.S. employees, working full-time for U.S.-based companies (*N* = 12,389)
 - Job categories with low expected counts (Cloud and Database, Data Management and Strategy, and Data Quality and Operations) were merged into one category (Data Management) for the Chi-square test
 - Features for the Random Forest model were one-hot encoded 
   - Only features significantly associated with job salary were retained for analysis (fourteen of seventeen)
 - Random Forest data were split into 70:30 train-test split 
 - Grid search cross validation was used to determine optimal model parameters

## Analyses 

 - Chi-square Test of Independence (experience level vs. job category)
 - Random Forest Regression model predicting job salary from experience level, job category, and work setting

## Results

 - Employee experience level composition varied between job categories
 - Executive employees in leadership positions and entry-level employees in data analysis positions had more employees than expected 
   - "Bright spots" for underrepresented experience levels
 - Random Forest features explained 25% of job salary

## Usage

To view this project, please visit the [page](https://kmiller999.github.io/ds_portfolio/posts/capstone_report/code/capstone_report.html) on my portfolio website. For questions or discussion, feel free to reach out to me to discuss further. 

## License

This project is licensed under the MIT License (see [LICENSE](./LICENSE)).

## Disclaimer

This GitHub repository contains work associated with my master's in data analytics capstone from Western Governors University (WGU). As described in the associated files, none of these works were directly submitted to WGU. Instead, these files represent a culmination of my capstone work, and none individually represent any portions of the capstone I submitted. Accordingly, this format of my work was shared in compliance with WGU's academic policy.