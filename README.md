# Flax Growth Modelling — *Linum usitatissimum* L.

> **Logistic model reveals early sowing as key to maximizing flax vegetative growth under subtropical conditions**
> *Submitted to Agronomy Journal (2025)*

## 📖 Overview

This repository contains all data, R code, and a Quarto-based website that fully reproduce the analyses presented in the manuscript.

Three vegetative growth traits — **leaf area**, **plant height**, and **leaf number** — were modelled as a function of accumulated growing degree-days (GDD) using three-parameter logistic functions, evaluated across two sowing seasons and two flax cultivars.

## 🌐 Website

The fully rendered analysis is available at:
👉 **https://nepem-ufsc.github.io/paper_flax_growth**

## 📂 Repository structure

```
paper_flax_growth/
├── _quarto.yml               # Quarto website configuration
├── index.qmd                 # Landing page
├── about.qmd                 # Research group & citation
├── styles/
│   └── custom.scss           # Custom theme
├── analysis/
│   ├── 01_climate.qmd        # Climate data import & GDD computation
│   ├── 02_leaf_area.qmd      # Leaf area logistic model
│   ├── 03_plant_height.qmd   # Plant height logistic model
│   ├── 04_leaf_number.qmd    # Leaf number logistic model
│   ├── 05_correlations.qmd   # Pearson correlation matrix
│   └── 06_supplementary.qmd  # Consolidated supplementary tables
├── results/                  # Pre-computed analysis objects (.rds)
├── figs/                     # Generated figures (auto-created on render)
├── clima.csv                 # Hourly weather station data
├── df_model_cresc.xlsx       # Field measurements (raw plant data)
└── df_model_cresc_medias.xlsx # Plot means
```

## 🔁 Reproducing the analysis

### Prerequisites

- [R](https://www.r-project.org/) ≥ 4.3
- [Quarto](https://quarto.org/) ≥ 1.4
- R packages (install once):

```r
install.packages(c(
  "rio", "tidyverse", "metan", "lubridate", "broom",
  "emmeans", "AgroR", "patchwork", "ggridges", "hydroGOF", "gt"
))
```

### Render the website locally

```bash
quarto preview
```

### Build for GitHub Pages

```bash
quarto render
```

Then push the `docs/` folder to GitHub and enable Pages from that directory.

## 📄 Citation

> **Authors.** (2025). Logistic model reveals early sowing as key to maximizing flax (*Linum usitatissimum* L.) vegetative growth under subtropical conditions. *Agronomy Journal*. doi: pending

## 📜 License

Code: [MIT](LICENSE) · Data: [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/)
