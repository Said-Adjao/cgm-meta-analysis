# CGM vs. Blood Glucose Monitoring in Non-Insulin-Treated Type 2 Diabetes

A reproducible meta-analysis of HbA1c outcomes from randomized controlled trials, built in R with the `meta` package and reported with Quarto.

## Summary

This project synthesizes randomized evidence on continuous glucose monitoring (CGM) versus blood glucose monitoring (BGM) in adults with type 2 diabetes **not treated with insulin** — the population for which CGM coverage is most often restricted. Pooling 8 trials using a random-effects model, CGM was associated with a mean HbA1c reduction of **−0.42% (95% CI −0.59 to −0.25)**, with no detectable between-study heterogeneity (I² = 0%).

The result independently reproduces a published 2025 meta-analysis (Aronson et al., −0.37%), validating the pipeline against a peer-reviewed benchmark.

## Methods

- **Study set:** 8 RCTs of non-insulin-treated T2DM, harvested from a documented 2025 systematic review
- **Data extraction:** combination of direct extraction from primary papers and standard back-calculation of standard errors from reported statistics; one trial converted from mmol/mol to % (DCCT/NGSP units)
- **Analysis:** inverse-variance random-effects model (mean difference), `meta` package in R
- **Reporting:** fully reproducible Quarto document — every figure and statistic computed from code

## Files

- `cgm_meta_report.qmd` — Quarto source (the reproducible analysis)
- `cgm_meta_report.html` — rendered report

## Limitations

Small evidence base (8 small, mostly open-label trials); several effect estimates back-calculated; some interventions bundled CGM with structured education. Findings are interpreted cautiously and framed as hypothesis-supporting rather than definitive.

## Tools

R · `meta` · `tidyverse` · Quarto

---
*Author: Said Adjao. Analysis built from published trial data only.*
