# PREDIX HER2 longitudinal acquired resistance

Analysis and visualization code for the PREDIX HER2 longitudinal acquired resistance project.

## Project structure

```text
src/
  functions/             Reusable R functions
  preprocessing/         Data cleaning and preparation scripts
  analysis/              Main analysis scripts
  plotting/              Figure generation scripts
analysis/
  longitudinal/          Longitudinal analysis scripts and notes
  acquired_resistance/   Acquired resistance analysis scripts and notes
  exploratory/          Exploratory analyses
  sensitivity/          Sensitivity analyses
data/
  raw/                  Original input data (keep unchanged)
  processed/            Derived analysis data
  metadata/             Local sample and clinical annotations
figure/                 Generated figures
table/                  Generated tables
config/                 Shareable analysis settings, without credentials
docs/                   Methods, data dictionaries, and project notes
logs/                   Local execution logs
```

Use `src/` for the main workflow and reusable code. Use `analysis/` for focused analyses; create a descriptive subfolder for each additional analysis. Store generated figures and tables in the top-level output folders, optionally grouped by analysis name.

## R workflow

- Run scripts from the repository root and use relative paths, such as `data/raw/` and `figure/`.
- Name scripts in execution order where relevant, for example `01_prepare_data.R`, `02_fit_models.R`, and `03_plot_results.R`.
- Keep reusable functions in `src/functions/` and document inputs, outputs, package requirements, and random seeds in each analysis.
- Record R and package versions when analysis code is added. A future `renv.lock` can be committed to capture dependencies.

The `.gitkeep` files allow empty code and documentation folders to appear in GitHub.

## Data
Patient-level and raw sequencing data are not included.

`data/`, `figure/`, `table/`, and `logs/` are local folders excluded from Git. Review figures and tables before explicitly sharing selected outputs. Put shareable data-format descriptions in `docs/`, rather than patient annotations in version control.
