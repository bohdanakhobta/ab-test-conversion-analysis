# A/B Test Conversion Analysis

## Project Overview

This project analyses the results of A/B tests to evaluate the impact of a new product variant on user conversion behaviour.

The analysis focuses on key funnel metrics and applies statistical testing to determine whether observed differences between control and test groups are significant.

## Business Problem

The goal of this analysis is to understand:

* Does the new product variant improve conversion rates?
* Which steps in the funnel are affected?
* Are the observed changes statistically significant?
* Do different user segments respond differently to the experiment?

## Data Source

Data was extracted from Google BigQuery and includes:

* Session data (date, device, country, channel)
* A/B test data (test ID, test group)
* Event data (user actions in the funnel)
* Order and account-related data

## Key Metrics

Conversion rates calculated as:

* Add Payment Info / Sessions
* Add Shipping Info / Sessions
* Begin Checkout / Sessions
* New Account / Sessions

## Methodology

1. Aggregated event data by test group
2. Calculated conversion rates for control and test groups
3. Measured relative uplift (%)
4. Applied statistical testing (two-proportion z-test)
5. Evaluated significance using p-value (< 0.05)

## Segmentation Analysis

Metrics were analysed across different segments:

* Device (desktop, mobile, tablet)
* Country
* Traffic channel

A minimum sample size threshold was applied to ensure reliable results.

## Key Results

* Conversion rates between the control and test groups are very similar
* Most differences are small and inconsistent across metrics
* The majority of p-values are above 0.05 → results are not statistically significant
* Some segments show variation, but results are not reliable due to small sample sizes

## Conclusions

* The new variant does not show a statistically significant impact on conversion rates
* Observed differences are likely due to random variation
* More data is required to make a confident decision
* Further experiments or stronger product changes are recommended

## Tools Used

* SQL (BigQuery)
* Python (Pandas, NumPy)
* Statistical analysis (SciPy)

## Output

* Final dataset with conversion rates and statistical test results
* Exported results for visualisation in Tableau
