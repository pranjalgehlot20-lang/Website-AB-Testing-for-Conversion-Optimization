Website A/B Testing for Conversion Optimization

Project Overview

This project demonstrates how A/B testing can be used to compare the conversion performance of two website variants using statistical analysis.

The experiment uses simulated website visitor data to compare Variant A and Variant B. Python is used to calculate conversion rates, estimate 95% confidence intervals, perform a two-proportion Z-test, and visualize how experimental results change as more visitors participate.

The project also includes a batch-wise simulation to demonstrate how conversion differences and statistical significance evolve as data accumulates.

Note: This project uses simulated data rather than real website visitor data. The two variants represent hypothetical website experiences with different assumed conversion probabilities. No specific website element or design change is defined in the experiment.

Business Problem

Businesses frequently experiment with different versions of their websites to improve user engagement and conversion rates.

However, a higher observed conversion rate does not automatically mean that one version performs better. The difference could occur due to random variation.

A/B testing helps businesses evaluate whether the observed difference between two alternatives is statistically significant before making decisions.

This project demonstrates a statistical approach to comparing two hypothetical website variants and evaluating their conversion performance.

Project Objectives

* Simulate visitor and conversion data for two website variants.
* Calculate and compare conversion rates.
* Estimate 95% confidence intervals for conversion rates.
* Formulate and test statistical hypotheses.
* Apply a two-proportion Z-test to evaluate the difference in conversion rates.
* Visualize conversion performance and confidence intervals.
* Simulate visitors arriving in batches to observe how conversion lift and p-values evolve over time.

Tools and Technologies

* Python – Overall analysis and simulation.
* NumPy – Random data generation and numerical calculations.
* Pandas – Organizing and displaying analytical results.
* SciPy – Statistical computing library.
* Statsmodels – Two-proportion Z-test.
* Matplotlib – Data visualization.

Project Workflow

1. Data Simulation

Since real website visitor data was not available, conversion data was generated using NumPy’s binomial distribution.

The initial experiment assumes:

Parameter	Variant A	Variant B
Visitors	10,000	10,000
Assumed conversion probability	10%	12%

A random seed was used to make the simulation reproducible.

2. Conversion Rate Calculation

Conversion rate measures the proportion of visitors who complete the desired action.

Formula:

Conversion Rate = (Number of Conversions / Total Visitors) × 100

The conversion rates of both variants were calculated and compared.

3. Confidence Interval Analysis

A 95% confidence interval was calculated for each variant to estimate the uncertainty around its observed conversion rate.

The results were visualized using a bar chart with error bars.

4. Hypothesis Testing

A two-proportion Z-test was performed to determine whether the observed difference between the conversion rates was statistically significant.

Hypotheses:

* Null Hypothesis (H₀): There is no difference in the conversion rates of Variant A and Variant B.
* Alternative Hypothesis (H₁): There is a difference in the conversion rates of Variant A and Variant B.

The significance level was set at 0.05.

5. Batch-wise Simulation

A second simulation was conducted to demonstrate how A/B testing results evolve as visitors arrive in batches.

The experiment used:

* 60 batches.
* 1,000 visitors per variant in each batch.
* 60,000 total visitors per variant.

After each batch, the analysis updated:

* Total visitors.
* Total conversions.
* Conversion rates.
* Absolute conversion lift.
* P-value from a one-sided two-proportion Z-test.

Line charts were used to visualize how the p-value and conversion lift changed as the experiment progressed.

Key Findings

Initial A/B Test Results

The initial simulation produced the following results:

Metric	Variant A	Variant B
Visitors	10,000	10,000
Conversions	973	1,134
Conversion Rate	9.73%	11.34%
95% CI Lower Bound	9.15%	10.72%
95% CI Upper Bound	10.31%	11.96%

Variant B achieved a higher observed conversion rate than Variant A.

Statistical test results:

* Z-statistic: -3.7082
* P-value: 0.0002
* Significance level: 0.05

Since the p-value was below 0.05, the null hypothesis was rejected. The simulated experiment provides statistically significant evidence of a difference between the two conversion rates.

Conversion Lift

The observed conversion rate increased from 9.73% to 11.34%.

* Absolute lift: 1.61 percentage points.
* Relative lift: Approximately 16.55%.

Batch-wise Simulation Results

After 60 batches, the simulation produced:

Metric	Variant A	Variant B
Total Visitors	60,000	60,000
Total Conversions	5,837	7,127
Conversion Rate	9.73%	11.88%

The final absolute conversion lift was approximately 2.15 percentage points.

The final p-value was below 0.05, indicating a statistically significant difference in the simulated results.

Business Insights

Based on the simulated experiment:

1. Variant B achieved a higher conversion rate than Variant A.
2. Statistical hypothesis testing helped distinguish an observed difference from random variation.
3. Confidence intervals provided an estimate of uncertainty around the conversion rates.
4. The batch-wise simulation demonstrated how accumulated observations can change the estimated conversion lift and statistical evidence.

In a real business experiment, these results could help decision-makers evaluate whether a proposed website change should be considered for implementation.

Important Statistical Considerations

* The dataset is simulated and does not represent actual customer behaviour.
* The assumed conversion probabilities are 10% for Variant A and 12% for Variant B.
* The batch-wise simulation performs repeated significance tests as data accumulates. Repeatedly checking p-values at a 0.05 threshold can increase the false-positive risk. Therefore, this simulation is illustrative and should not be treated as a validated sequential testing or stopping procedure.
* Results from simulated data should not be interpreted as evidence of actual business improvement.

Skills Demonstrated

* A/B Testing
* Statistical Hypothesis Testing
* Two-Proportion Z-Test
* Confidence Interval Calculation
* Conversion Rate Analysis
* Data Simulation
* Statistical Interpretation
* Python Data Analysis
* Data Visualization

Project Structure

Website-A-B-Testing-for-Conversion-Optimization/
│
├── Website A-B Testing for Conversion Optimization.ipynb
└── README.md

How to Run the Project

1. Clone or download this repository.
2. Install the required Python libraries:

pip install numpy pandas scipy statsmodels matplotlib

3. Open the Jupyter Notebook:

jupyter notebook

4. Run the notebook cells in sequence to reproduce the simulation, statistical analysis, and visualizations.

Execution note: Before running the notebook from a fresh kernel, add from math import sqrt to the imports, or replace sqrt() with np.sqrt() in the confidence interval function. The current import cell does not define sqrt.

Conclusion

This project demonstrates the application of statistical methods to a hypothetical website A/B testing experiment.

By combining conversion rate calculations, confidence intervals, hypothesis testing, and batch-wise simulation, it illustrates how Python can support data-driven evaluation of alternative website experiences.
