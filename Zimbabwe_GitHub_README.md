# Zimbabwe Dual War Shock Trilogy

## Economic Impact of the Russia-Ukraine and Iran-US-Israel Wars on Zimbabwe's Economy

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.placeholder.svg)](https://doi.org/10.5281/zenodo.placeholder)
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)
[![ORCID](https://img.shields.io/badge/ORCID-0000--0001--6119--9234-green)](https://orcid.org/0000-0001-6119-9234)

**Author:** Dr Tafadzwa Luke Mupingashato
**Affiliation:** Postdoctoral Research Fellow, Thabo Mbeki African School of Public and International Affairs (TM-School), UNISA | Director, TAFMUP PTY LTD (Reg. 2025/461781/07)
**Contact:** mupingatl@gmail.com | mupintl@unisa.ac.za | **Date:** March 2026

---

## The Trilogy

| # | Title | Target Journal | Method |
|---|-------|---------------|--------|
| 1 | *War at a Distance: Russia-Ukraine Impact on Zimbabwe* | SAJEMS | GVAR + ARDL + SCPI Probit |
| 2 | *The Strait That Reaches Harare: Iran War Impact on Zimbabwe* | Resources Policy | BVAR + ARDL |
| 3 | *Double Jeopardy: The Dual War Shock and Zimbabwe's Macroeconomic Threshold* | World Development | SUR + CSIM + DWSF |

## Key Findings

- **Fertiliser Double-Bind:** CSIM amplification factor **1.8–2.1×** on the fertiliser channel
- **Compound Crisis Probability: 61%** at 18 months under continued dual-war conditions (Scenario B)
- **Mining Asymmetry:** Gold/platinum price surges create **net positive** mining outcomes under all scenarios
- **Cape Corridor:** 90% of global shipping now Cape-routed — structural logistics opportunity
- **61% − 38% − 45% = 16 pp** excess = the CSIM interaction effect made numerical

---

## Repository Structure

```
zimbabwe-dual-war-shock/
├── README.md
├── LICENSE
├── CITATION.cff
├── data/
│   ├── zimbabwe_war_shock_annual.csv         # 16 annual observations (2010–2025)
│   ├── zimbabwe_war_shock_quarterly.csv      # 64 quarterly observations (interpolated)
│   └── zimbabwe_war_shock_dataset.xlsx       # Excel with Source_Notes_Verified sheet
├── stata/
│   └── zimbabwe_war_trilogy_master.do        # Complete Stata 17 do-file
├── r/
│   └── zimbabwe_war_trilogy_master.R         # Complete R 4.3+ script
├── visuals/                                  # 9 × 300 DPI publication figures (Python)
│   ├── Fig1_Exploratory_Overview.png
│   ├── Fig2_Exploratory_CorrelationMatrix.png
│   ├── Fig3_Exploratory_Distributions.png
│   ├── Fig4_Explanatory_GDP_Counterfactual.png
│   ├── Fig5_Explanatory_DualCommodityShock.png
│   ├── Fig6_Explanatory_OffsettingForces.png
│   ├── Fig7_Explanatory_CSIM_Heatmap.png
│   ├── Fig8_Explanatory_CrisisProbability.png
│   └── Fig9_FourPanel_PublicationReady.png
└── slides/
    └── Zimbabwe_DualWar_Presentation.pptx    # 20-slide conference presentation
```

---

## Dataset Verification — All 20 Variables Confirmed Against Public Sources

| Variable | Description | Source | Public URL (Verified) |
|----------|-------------|--------|----------------------|
| `gdp_growth` | Real GDP growth (%) | World Bank WDI | data.worldbank.org/indicator/NY.GDP.MKTP.KD.ZG?locations=ZW |
| `inflation` | CPI inflation (%) | ZIMSTAT; RBZ MPS | zimstat.co.zw / rbz.co.zw/publications/monetary-policy-statements |
| `agri_growth` | Agriculture VA growth (%) | World Bank WDI | data.worldbank.org/indicator/NV.AGR.TOTL.ZG?locations=ZW |
| `mining_growth` | Mining VA growth (%) | ZIMSTAT; Chamber of Mines | chamberofmines.org.zw |
| `fertiliser_idx` | Fertiliser price index (2010=100) | World Bank Pink Sheet | worldbank.org/en/research/commodity-markets |
| `brent_crude` | Brent crude (USD/barrel) | World Bank; US EIA | eia.gov/petroleum/data |
| `wheat_price` | Wheat price (USD/tonne) | World Bank Pink Sheet | worldbank.org/en/research/commodity-markets |
| `gold_price` | Gold price (USD/troy oz) | LBMA PM Fix; WGC | lbma.org.uk/prices-and-data/precious-metal-prices |
| `platinum_price` | Platinum price (USD/troy oz) | LPPM; Johnson Matthey; WPIC | platinuminvestment.com/supply-and-demand |
| `remit_usd_m` | Remittances (USD million) | World Bank; RBZ; Bloomberg | data.worldbank.org/indicator/BX.TRF.PWKR.DT.GD.ZS?locations=ZW |
| `ca_balance_gdp` | Current account (% GDP) | World Bank; IMF | data.worldbank.org/indicator/BN.CAB.XOKA.GD.ZS?locations=ZW |
| `forex_receipts` | Forex receipts (USD billion) | RBZ Monetary Policy Statements | rbz.co.zw/publications/monetary-policy-statements |
| `govt_rev_gdp` | Govt revenue (% GDP) | IMF Country Report 25/282 | imf.org/en/countries/zwe |
| `public_debt_gdp` | Public debt (% GDP) | IMF/World Bank | worldbank.org/en/country/zimbabwe/overview |
| `fuel_imp_pct` | Fuel imports (% total) | ZIMSTAT trade statistics | zimstat.co.zw |
| `diesel_price` | Diesel price (USD/litre) | ZERA official | zera.co.zw/petroleum-prices |
| `sa_gdp_growth` | South Africa GDP growth (%) | Stats SA; World Bank | statssa.gov.za |
| `food_insecure_m` | Food insecure (millions) | WFP; FAO GIEWS; FEWS NET | fews.net/southern-africa/zimbabwe |
| `ru_war_idx` | Russia-Ukraine war intensity (0–100) | UCDP GED v24.1 | ucdp.uu.se |
| `iran_war_idx` | Iran war intensity (0–100) | UCDP GED; ACLED; Columbia CGEP | acleddata.com / energypolicy.columbia.edu |

> **Data integrity:** Every data point has been cross-checked against its primary source. Values confirmed against published figures: e.g., $2.45bn remittances (Bloomberg Jan 2026), $23.2bn public debt = 72.9% GDP (World Bank 2026 overview), ZERA diesel $2.05/litre (March 18 announcement). The `iran_war_idx` 2026 value (98) is annualised from 20-day conflict event counts as of March 20, 2026 — the date this paper was written.

---

## Replication

```bash
# Clone
git clone https://github.com/Mupingatl/zimbabwe-dual-war-shock.git
cd zimbabwe-dual-war-shock

# R (installs all packages automatically)
Rscript r/zimbabwe_war_trilogy_master.R

# Python figures
python3 generate_figures.py
```

```stata
* Stata 17+
* Install: ssc install ardl; ssc install estout
cd "path/to/zimbabwe-dual-war-shock"
do stata/zimbabwe_war_trilogy_master.do
```

---

## Citation

```bibtex
@misc{mupingashato2026dwsf,
  author  = {Mupingashato, Tafadzwa Luke},
  title   = {Zimbabwe Dual War Shock Trilogy: Data and Replication Code},
  year    = {2026},
  howpublished = {\url{https://github.com/Mupingatl/zimbabwe-dual-war-shock}},
  orcid   = {0000-0001-6119-9234},
  note    = {Working Papers 1-3. Target journals: SAJEMS, Resources Policy, World Development.}
}
```

## Related Repositories
- [zimbabwe-exports-afcfta](https://github.com/Mupingatl/zimbabwe-exports-afcfta) — Zimbabwe's export basket and AfCFTA signals

---

*Last updated: 20 March 2026 — Day 21 of the US-Israel-Iran War | Year 5 of the Russia-Ukraine War*
