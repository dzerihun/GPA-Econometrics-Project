# GPA Predictor Project

**Authors:** Dagmawi Zerihun, Khushi Mohapatra  
**Institution:** Denison University, Department of Economics  
**Course:** ECON 307-01 - Intro to Econometrics  
**Instructor:** Dr. Ngwunui Azenui  
**Date:** May 5, 2023

## Project Overview

This project aims to predict college GPA (COLLGPA) using various independent variables that reflect a student's background, habits, and activities. The project leverages econometric methods to identify the most significant predictors of college GPA.

## Variables Used

- **COLLGPA:** Overall college grade point average (Dependent Variable)
- **SAT:** Aggregate math and critical reading SAT score
- **HSGPA:** Overall high school grade point average
- **SAT_HSGPA:** Interaction term between SAT score and high school GPA
- **HRSTD:** Average number of hours spent studying per week
- **HRSTD_SQ:** Squared term of hours spent studying per week
- **HREXTRA:** Average number of hours spent in extracurricular activities per week
- **DOUBLE:** Dummy variable indicating if the student is pursuing a double major
- **FEMALE:** Dummy variable indicating if the student is female
- **SLEEP:** Average hours of sleep per week
- **INTERNATIONAL:** Dummy variable indicating if the student is an international student
- **INTERNATIONAL_DOUBLE:** Interaction term between being an international student and having a double major
- **SCHOLAR:** Dummy variable indicating if the student has received scholarship money
- **GREEK:** Dummy variable indicating if the student is affiliated with Greek life
- **DRINK:** Average number of alcoholic drinks consumed per week
- **GREEK_DRINK:** Interaction term between Greek affiliation and the average number of alcoholic drinks per week
- **ATHLETE:** Dummy variable indicating if the student is an intercollegiate athlete
- **FRIEND:** Percentage of time spent with a significant other while in college
- **DECISION:** Dummy variable indicating if the student applied to Denison using Early Decision
- **DECISION_SCHOLAR:** Interaction term between applying Early Decision and having received scholarship money
- **HELP:** Average number of hours per week spent obtaining help outside of class

## Model Specifications

### Model 1
Initial regression model with the following equation:
![Model 1 Equation](https://latex.codecogs.com/png.latex?%5Ctext%7BCOLLGPA%7D%20%3D%20%5Cbeta_0%20%2B%20%5Cbeta_1%20%5Ctext%7BSAT%7D%20%2B%20%5Cbeta_2%20%5Ctext%7BHSGPA%7D%20%2B%20%5Cbeta_3%20%5Ctext%7BSAT%7D%20%5Ctimes%20%5Ctext%7BHSGPA%7D%20%2B%20%5Cldots%20%2B%20%5Cepsilon)

### Model 2
Adjusted model after addressing multicollinearity and transforming some variables:
![Model 2 Equation](https://latex.codecogs.com/png.latex?%5Ctext%7BCOLLGPA%7D%20%3D%20%5Cbeta_0%20%2B%20%5Cbeta_1%20%5Ctext%7BSAT%7D%20%2B%20%5Cbeta_2%20%5Ctext%7BHSGPA%7D%20%2B%20%5Cbeta_3%20%5Cln%28%5Ctext%7BHRSTD%7D%29%20%2B%20%5Cldots%20%2B%20%5Cepsilon)

### Model 3
Final model with additional modifications to improve fit and significance:
![Model 3 Equation](https://latex.codecogs.com/png.latex?%5Ctext%7BCOLLGPA%7D%20%3D%20%5Cbeta_0%20%2B%20%5Cbeta_1%20%5Ctext%7BSAT%7D%20%2B%20%5Cbeta_2%20%5Ctext%7BHSGPA%7D%20%2B%20%5Cbeta_3%20%5Cln%28%5Ctext%7BHRSTD%7D%29%20%2B%20%5Cbeta_4%20%5Cln%28%5Ctext%7BHREXTRA%7D%29%20%2B%20%5Cldots%20%2B%20%5Cepsilon)

## Key Findings

- The final model explains 33.23% of the variation in college GPA.
- Significant predictors include SAT score, high school GPA, hours studied, and scholarship status.
- Interaction terms such as SAT \times HSGPA and GREEK \times DRINK provide additional insights into the relationships between variables and college GPA.

## Conclusion

Model 3 is identified as the best model for predicting college GPA, with most variables being statistically significant and an improved overall fit. Future work can explore additional variables or alternative models to further enhance predictive accuracy.

## How to Use

1. **Clone the repository:**
    ```bash
    git clone <repository_url>
    cd <repository_directory>
    ```

2. **Install required packages:**
    Ensure you have the necessary Python packages installed. You can use the following command to install them:
    ```bash
    pip install -r requirements.txt
    ```

3. **Run the analysis:**
    Execute the provided scripts to reproduce the analysis and results. Detailed instructions are provided in the scripts.

## Repository Structure

- `data/`: Contains the dataset used for the analysis.
- `scripts/`: Contains the analysis scripts.
- `results/`: Contains the output results from the models.
- `README.md`: This file.

## Acknowledgements

We would like to thank Dr. Ngwunui Azenui for her guidance and support throughout this project.

## License

This project is licensed under the MIT License. See the LICENSE file for details.
