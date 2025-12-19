# Data Analysis Plan Template for PhD-Level Statistics Coursework

## 1. Project Title
How winter storm risk and severity effects spatial insurance risk and loss.

---

## 2. Research Questions & Objectives
- Does extreme weather risk, particularly winter storm severity, significantly effect geospatial insurance risk and loss.

---

## 3. Background & Motivation
- Brief overview of the context and significance of the problem.
- Summary of relevant literature or prior work.
- Theoretical or methodological frameworks guiding the analysis.

---

## 4. Data Description
### 4.1 Data Source(s)
- Origin of data (e.g. observational study, experiment, simulation, publicly available dataset).
- Data collection methods.

### 4.2 Variables & Measurements
- List key variables, including:
  - Variable name
  - Type (continuous, categorical, ordinal, etc.)
  - Units of measurement
  - Expected distributions or characteristics

### 4.3 Data Structure
- Number of observations and variables.
- Data format (wide/long, hierarchical, time series, etc.).
- Any grouping or clustering structures.

### 4.4 Data Quality Considerations
- Missing data patterns.
- Outliers or influential observations.
- Measurement error.
- Data cleaning or preprocessing steps anticipated.

---

## 5. Proposed Analyses
### 5.1 Overview of Analytical Strategy
- High-level description of analytical flow.
- Justification for methods based on research questions and assumptions.

### 5.2 Exploratory Data Analysis (EDA)
- Descriptive statistics.
- Visualization plans (e.g., histograms, boxplots, scatterplots).
- Initial diagnostics for distributional assumptions.

### 5.3 Statistical Models & Methods
- Spatial Clustering:

- Spatial Prediction:

For each proposed method or model:
- Model name and purpose (e.g., linear regression, generalized linear model, survival analysis, mixed-effects model, Bayesian model).
- Model specification (equations if appropriate).
- Assumptions and how they will be checked.
- Estimation methods (e.g., MLE, Bayesian inference).
- Model selection or comparison strategies.

### 5.4 Additional or Alternative Analyses
- Sensitivity analyses.
- Robustness checks.
- Nonparametric or machine learning models.

### 5.5 Validation & Diagnostics
- Residual analysis.
- Goodness-of-fit measures.
- Cross-validation or out-of-sample evaluation.

---

## 6. Software, Programs, and Packages Required
### 6.1 Statistical Software
- R, RStudio.

### 6.2 Required Packages or Libraries
For each package:
- Package name
- Purpose (e.g., data manipulation, visualization, modeling)
- Version requirements (optional)

### 6.3 Computational Requirements
- Expected runtime or computing constraints.
- Need for parallelization or high-performance computing.

---

## 7. Data Management & Reproducibility
- Version control through Github.

- File organization strategy.
- Version control (e.g., GitHub).
- Reproducible workflow tools (e.g., R Markdown, Jupyter notebooks).
- Data privacy or ethical considerations.

---

## 8. Expected Outcomes & Deliverables
### 8.1 Plots
- Sample of swe, prcp, tmin, tmax plots for census tract in each state
  - 5 curves for each plot (winter 2019 - winter 2023)
- cloropleth of landcover, impervious land, acs variables (the one with the highest weight)
- plots of fpca dimensions 1, 2, 3 for sample of winter seasons (probably 3)
- 

### 8.2 Tables
- acs table-one without grouping by census tract


---

## 9. Timeline
- 08-Dec-2025: Background research completed.
- 10-Dec-2025: Data acquired.
- 11-Dec-2025: In-class presentation. **(Project proposal/in-progress report)**
- 13-Dec-2025: EDA completed.
- 14-Dec-2025: Initial model results.
- 18-Dec-2025: Project report due.


- Milestones for data cleaning, EDA, modeling, diagnostics, and writing.

---

## 10. References
- List of academic references supporting methodological choices.

---

## 11. Notes From Presentation
- Do I need to scale time in the copula model? Most likely not as all the functional covariates are being measured on the same time scale. Curve alignment may be necessary, but unlikely as it would remove the variablility in both space in time.
- R(s) components are largely static.
- Comparison, not evaluation, on earlier time window 2013-2018.
- Potential Hierarchical, Fixed-Effects model to account for the variation that being in different states
  * Hierarchical model can't be easily validated on a different set of states.
- Start with basic gaussian copula model with matern covariance and improve from there.
  * CV hyper-parameters for covariance.
  * Could evaluate robustness to different copula specifications (Matern vs. Exp vs. Spherical) [covariance mis-specification]
- Bayesian or Frequentist? Bayesian, much easier for spatial statistics.


- How robust are copula models to model mis-specification?
- Evaluate Isotropy.
