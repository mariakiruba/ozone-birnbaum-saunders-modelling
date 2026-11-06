# Ozone Level Modelling with Birnbaum–Saunders-Family Distributions

Which statistical distribution best describes daily ozone readings? This project fits five Birnbaum–Saunders (BS)-family models by maximum likelihood in R and compares them with AIC, BIC and the Kolmogorov–Smirnov (KS) test.

M.Sc. Mathematics project, VIT Vellore. Under the guidance of Dr. K. Sathya Narayana Sharma.

## Models
BS, Log-GBS (logistic parent), Student's-t BS, Delta-BS (power-exponent generalisation of BS) and KM-BS (BS with the Kavya–Manoharan transformation).

## Method
- Maximum likelihood estimation with `optim` (L-BFGS-B), from several starting points
- Model comparison using AIC, BIC and the KS test
- Fitted curves plotted over the histogram, plus an empirical vs fitted CDF plot

## Example result (daily ozone readings, n = 132)
| Model | AIC | BIC | KS p-value |
|---|---|---|---|
| Log-GBS | 1102.0 | 1107.8 | 0.333 |
| t-BS | 1103.5 | 1112.2 | 0.387 |
| Delta-BS | 1103.9 | 1112.5 | 0.340 |
| BS | 1106.1 | 1111.8 | 0.050 |
| KM-BS | 1120.5 | 1126.3 | 0.008 |

Log-GBS had the lowest AIC and BIC; t-BS and Delta-BS were statistically close; KM-BS fitted worst on this dataset.

## How to run
1. Put your ozone data file in the same folder as the `.Rmd` file (the data is not included here).
2. Set `data_file` and `city_name` at the top of the data section.
3. Knit `family_of_bs_distributions_fixed_1.Rmd` in RStudio.

## Files
- `family_of_bs_distributions_fixed_1.Rmd` – analysis code
- `figures/` – fitted-curve plots
- `results/` – model comparison table (CSV)

## Author
Maria Kiruba R · [LinkedIn](https://www.linkedin.com/in/maria-kiruba-r)
