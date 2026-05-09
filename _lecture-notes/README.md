# Research Plan Replication Code

This folder contains a compact replication script for the research-plan statistics.

## Files

- `replicate_research_plan.py`: reproduces the main mediation-style regressions, Sobel test, leave-one-out robustness, and the 15-34 age-window robustness check.

## Data Requirement

The main analysis uses the final 9-country panel reported in the proposal. The 15-34 robustness check additionally reads:

- `BL_v3_MF.csv`

Set `DATA_DIR` near the top of the Python script to the folder containing the source data files.

## Notes

- The `success / ongoing / trap` labels are used only for interpretation and plotting. They are not included in the regression model.
- The main regressions use continuous variables only: `QA-HC`, manufacturing employment share at the Lewis turning point, and manufacturing employment share ten years later.
- Some education-quality values in the proposal rely on supplemented sources where Lee & Lee does not provide direct country rows. For the 15-34 robustness check, the script keeps the proposal's implied quality multiplier fixed and changes only the Barro-Lee age window.
