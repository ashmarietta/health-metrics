# Softball vs. Half Marathon Health Metrics Training Analysis

## Overview

This project analyzes personal Apple Health data to explore changes in health, recovery, and activity across three distinct training periods:

- **Off-Season Softball:** August 26, 2025 – February 5, 2026
- **In-Season Softball:** February 6, 2026 – May 6, 2026
- **Half Marathon Running:** June 8, 2026 – September 19, 2026

The goal is to compare key health and fitness metrics across these periods and examine how different types of physical training may relate to recovery, cardiovascular health, and daily activity.

## Methodology

### Data Collection

Data was exported from Apple Health and processed using Python. The XML export contained approximately 6.9 million health records and workout entries.

The data was parsed using Python's `ElementTree` library and organized into structured datasets using `pandas`.

The following datasets were generated:
- `daily_summary.csv`
- `hrv_readings.csv`
- `workouts.csv`

Only relevant Apple Watch data was included in the analysis.

### Feature Engineering

The analysis focused on several health and fitness metrics:

- Active Energy Burned
- Basal Energy Burned
- Heart Rate Variability (HRV)
- Resting Heart Rate (RHR)
- Step Count
- VO2 Max
- Sleep Duration
- Sleeping Wrist Temperature
- Workout Frequency and Duration

Seven-day rolling averages were calculated for HRV and resting heart rate to help identify longer-term trends and reduce daily fluctuations.

### Analysis Approach

The analysis compared average health metrics across the three training periods.

Visualizations were created to examine:
- Changes in HRV over time
- Changes in resting heart rate over time
- Daily activity and energy expenditure
- Step count trends
- VO2 Max changes
- Sleep duration and sleeping wrist temperature
- Workout frequency and duration

Sleep duration and sleeping wrist temperature were also compared to explore potential relationships between sleep and recovery.

## Key Findings

### Average Health Metrics by Training Period

| Metric | Off-Season Softball | In-Season Softball | Half Marathon Running |
|---|---:|---:|---:|
| Active Energy Burned | 592.07 | 667.77 | 695.65 |
| Basal Energy Burned | 1384.51 | 1418.81 | 1420.28 |
| HRV (ms) | 83.20 | 80.99 | 84.38 |
| Resting Heart Rate (bpm) | 47.91 | 49.83 | 46.14 |
| Step Count | 13,117.98 | 14,849.48 | 16,268.27 |
| VO2 Max | 39.88 | 40.75 | 47.96 |

### Heart Rate Variability (HRV)

HRV averages varied across the three training periods:

| Training Period | Days with HRV Data | Average HRV |
|---|---:|---:|
| Off-Season Softball | 153 | 83.2 ms |
| In-Season Softball | 90 | 81.0 ms |
| Half Marathon Running | 104 | 84.4 ms |

The half marathon training period had the highest average HRV, while the in-season softball period had the lowest.

### Resting Heart Rate

The average resting heart rate was highest during in-season softball and lowest during half marathon training.

This pattern provides an opportunity to examine how resting heart rate changed alongside training demands and activity levels.

### Activity and Energy Expenditure

Daily active energy expenditure and step count increased across the three periods.

The half marathon training period had the highest average active energy expenditure and step count.

### VO2 Max

Average VO2 Max increased across the three periods, with the highest average occurring during half marathon training.

This provides an additional metric for examining changes in cardiovascular fitness over time.

## Practical Implications

Comparing these periods provides a way to evaluate how different training styles correspond with changes in daily activity, cardiovascular fitness, and recovery-related measurements.

The results highlight several areas worth monitoring during future training cycles:

- HRV as a measure of changes in recovery patterns
- Resting heart rate as a cardiovascular trend
- VO2 Max as an indicator of aerobic fitness
- Daily steps and active energy as measures of overall activity
- Sleep duration and wrist temperature as additional recovery-related measurements

These metrics are most useful when considered together rather than interpreted individually.

## Limitations

Several limitations should be considered when interpreting the results:

- **Single-person dataset:** The analysis reflects one individual's health and training history and cannot be generalized to a larger population.
- **Different period lengths:** The three training periods do not contain the same number of days.
- **Missing data:** Apple Health measurements were not recorded consistently every day, and the number of available observations varies by metric.
- **Time gap:** There is a gap of recovery time between the in-season softball period and half marathon training period.
- **Potential confounding factors:** Sleep, nutrition, stress, illness, and other lifestyle factors may influence the metrics.
- **Correlation vs. causation:** Changes observed across training periods do not establish that a particular training style caused those changes.

## Future Work

Potential next steps include:

- Comparing weekly training volume with HRV and resting heart rate.
- Examining relationships between sleep duration and recovery metrics.
- Investigating changes in VO2 Max alongside running volume.
- Expanding the analysis to include future training cycles.

## Repository Structure

```text
├── metrics_code.html
└── README.md
