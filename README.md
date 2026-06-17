# Dubai Rental Market Analysis (2020–2026)
### What's driving rental growth across Dubai's key districts?

---

## Overview

This project analyses Dubai's residential rental market using a comprehensive 
dataset spanning January 2020 to April 2026, covering secondary sales, off-plan 
listings, and rental contracts across 84 communities and 52 zones.

The analysis investigates the macroeconomic forces behind Dubai's rental growth 
cycle — from the COVID-era dip through the Expo 2020 rally, the Russian/CIS 
capital influx of 2022, the Golden Visa expansion, the 2023 market peak, and the 
subsequent rate-driven cooling. It is built entirely in Python and structured to 
mirror a professional analytics workflow: raw data through cleaning and feature 
engineering to business-ready findings.

---

## Business Question

**How have Dubai rental prices trended since 2020, and what's driving growth?**

Secondary questions explored:

- Does Dubai's rental growth correlate with macroeconomic indicators —
  mortgage rate cycles, capital inflows, and demand shocks post-2020?
- Which districts are experiencing demand-supply imbalances, and are rental
  prices in those areas outpacing broader market growth?
- Can we identify leading vs lagging districts — communities where price
  signals appear early and predict broader market movement?
- What is the price elasticity pattern across bedroom categories — do larger
  units absorb price shocks differently than studios and 1-beds?
- Is there evidence of a K-shaped recovery post-COVID in Dubai's rental
  market, where luxury and budget segments diverged significantly?
- How does Metro proximity and freehold designation influence rental premiums,
  and have those premiums shifted as infrastructure and policy evolved?

---

## Dataset

- **Source:** [Kaggle — Dubai Real Estate: Sales, Off-Plan & Rentals 2020–2026](https://www.kaggle.com/datasets/sergionefedov/dubai-real-estate-sales-and-rentals-20202026)
- **License:** Apache 2.0 — open for public use and publication
- **Coverage:** January 2020 to April 2026 | 84 communities | 52 zones
- **Total records:** ~93,000 rows across 5 files (~17 MB)

**A note on methodology:** Listing-level records are generated via a hedonic 
pricing model anchored to real DLD/Property Finder base prices per zone, real 
CBUAE mortgage rate timelines, and real Dubai Metro coordinates. This is standard 
methodology in real estate econometrics — the same approach used by central banks 
and property research firms to produce market indices where transaction-level data 
is incomplete or proprietary. Aggregate trends and community-level patterns 
reflect real market dynamics.

### Files used

| File | Rows | Description |
|---|---|---|
| `rentals.csv` | 25,000 | Annual rental contracts — primary analysis file |
| `area_prices_monthly.csv` | 6,384 | Monthly time series: 84 communities × 76 months |
| `secondary_sales.csv` | 50,000 | Secondary market sales — used for K-shaped recovery comparison |
| `metro_stations.csv` | 55 | Dubai Metro stations (Red + Green Line) with coordinates |
| `off_plan.csv` | 12,000 | Off-plan listings — used for market context |

---

## Tools & Libraries

| Tool | Purpose |
|---|---|
| Python 3.11 | Core analysis language |
| Pandas | Data manipulation and cleaning |
| NumPy | Numerical operations and outlier detection |
| Matplotlib / Seaborn | Visualisation |
| Scipy | Pearson correlation, OLS regression, z-score |
| Jupyter Notebook | Development environment |

---

## Project Structure
