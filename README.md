# Coral hard cover

## Overview

This project investigates the relationship between Hard Coral Cover (HCC) and thermal stress (measured as Degree Heating Weeks, DHW) across the Great Barrier Reef. It was conducted as part of the Statistical Consulting unit at the University of Sydney. The analysis spans multiple statistical methods to evaluate coral resilience, predict future coral cover, and model reef-specific ecological responses.

## Objectives

- Assess how coral morphotypes recover under different levels of DHW-induced stress.
- Forecast short-term changes in HCC using time series models.
- Develop reef-specific predictive models using mixed-effect modeling.

## Data

- **Source**: Great Barrier Reef  data
- **Scope**: HCC data across various coral morphotypes and maximum annual DHW values
- **Granularity**: Sector and reef level
- **Preprocessing**:
  - Interpolation used for limited missing values
  - Excluded transects with more than 2 consecutive missing observations

## Methods

### 1. Two-Way ANOVA
- Explored the interaction between DHW severity (Low, Medium, High) and coral morphotype on HCC percentage change.
- Significant interaction effect observed (p = 0.04), indicating that morphotype responses vary by DHW level.

### 2. ARIMAX Model
- Time series model incorporating DHW as an exogenous variable.
- Evaluated different model configurations, selecting the best based on diagnostics.
- Best suited for short-term forecasting due to dependency on future DHW estimates.

### 3. Mixed-Effect Models
- Accounts for non-independence among geographically clustered reefs.
- Modeled HCC as a polynomial function of DHW (linear, quadratic, and cubic terms).
- Generated reef-specific equations using random effects.

## Key Results

- **ANOVA**: Morphotypes respond differently to varying DHW levels; Top Heavy coral shows resilience under low to moderate stress.
- **ARIMAX**: Provides accurate short-term forecasts; limitations include reliance on future DHW values and external factors.
- **Mixed Model**: Reveals nonlinear relationships and reef-specific trends; Conditional R² = 0.354 indicates moderate model fit.

## Conclusion

This analysis highlights the complex interplay between coral types and thermal stress, providing insights into reef health under climate change. The modeling approach enables better-informed conservation strategies and forecasting tools.
