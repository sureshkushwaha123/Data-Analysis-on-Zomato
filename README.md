# Zomato Restaurant Data Analysis

A concise, end‑to‑end exploratory data analysis (EDA) of the Zomato restaurant dataset using **Python (pandas, matplotlib, seaborn)**. This project explores restaurant distribution, cuisines, ratings, and platform features like online delivery and table booking.

---

## 📁 Project Structure
```
Data Analysis on Zomato Dataset/
├─ Data Analysis on  zomato dataset.ipynb   # Jupyter notebook with the analysis
├─ zomato (1) (2).csv                       # Main dataset (9,551 rows × 21 columns)
└─ Zomato_Country-Code.xlsx                 # (Expected) Country code mapping (add to root)
```
> If `Zomato_Country-Code.xlsx` is missing, add a mapping file with columns **Country Code** and **Country** to enable country name level charts.

---

## 🎯 Objectives
- Understand dataset shape, coverage (countries, cities), and data quality.
- Analyze distribution of **ratings** and **votes**.
- Identify most common **cuisines** and those with **highest average ratings**.
- Explore **online delivery** and **table booking** availability by country.
- Spotlight top **cities** by restaurant count.
- <img width="359" height="370" alt="{12F9EC1B-41C2-4BDA-A2D5-06DE483A5C2A}" src="https://github.com/user-attachments/assets/d2a741e9-579b-4c44-914e-efa85d9207e6" />


---

## 🧰 Tech Stack
- **Python**: pandas, numpy, matplotlib, seaborn
- **Jupyter Notebook** for reproducible EDA

---

## 📊 Dataset Snapshot
- **Rows**: `9,551`
- **Columns**: `21`
- **Unique countries (by code)**: `15`
- **Unique cities**: `141`

**Selected columns**
```
Restaurant ID, Restaurant Name, Country Code, City, Address, Locality, Locality Verbose, Longitude, Latitude, Cuisines, Average Cost for two, Currency, Has Table booking, Has Online delivery, Is delivering now, Switch to order menu, Price range, Aggregate rating, Rating color, Rating text, Votes
```

---

## 🔎 Key Findings (from the current CSV)
### Top Countries (by Country Code)
> Mapping file not found; showing top **Country Code** values.
| Country Code | Restaurants |
|---|---|
| 1 | 8652 |
| 216 | 434 |
| 215 | 80 |
| 30 | 60 |
| 214 | 60 |

### Top Cities (by restaurant count)
| City | Restaurants |
|---|---|
| New Delhi | 5473 |
| Gurgaon | 1118 |
| Noida | 1080 |
| Faridabad | 251 |
| Ghaziabad | 25 |
| Bhubaneshwar | 21 |
| Amritsar | 21 |
| Ahmedabad | 21 |
| Lucknow | 21 |
| Guwahati | 21 |

### Rating Distribution
- By text label:
| Rating text | Count |
|---|---|
| Average | 3737 |
| Not rated | 2148 |
| Good | 2100 |
| Very Good | 1079 |
| Excellent | 301 |
| Poor | 186 |

- By numeric bucket:
| Aggregate rating bin | Count |
|---|---|
| 0 | 2148 |
| (0,1] | 0 |
| (1,2] | 10 |
| (2,3] | 1891 |
| (3,4] | 4388 |
| (4,5] | 1114 |

### Online Delivery (Top 5 Country Codes)
| index | Country Code | No (count) | Yes (count) |
| --- | --- | --- | --- |
| 0 | 1 | 6229 | 2423 |
| 1 | 216 | 434 | 0 |
| 2 | 215 | 80 | 0 |
| 3 | 30 | 60 | 0 |
| 4 | 214 | 32 | 28 |

### Most Common Cuisines
| index | Cuisine | Restaurants | Avg rating | Votes |
| --- | --- | --- | --- | --- |
| 0 | North Indian | 3017 | 3.3 | 595194 |
| 1 | Chinese | 2184 | 3.28 | 363890 |
| 2 | Fast Food | 1563 | 3.26 | 183665 |
| 3 | Mughlai | 794 | 3.27 | 151784 |
| 4 | Italian | 726 | 3.75 | 329230 |
| 5 | Continental | 699 | 3.71 | 288213 |
| 6 | Cafe | 634 | 3.68 | 177494 |
| 7 | Desserts | 543 | 3.58 | 105781 |
| 8 | Bakery | 536 | 3.39 | 57513 |
| 9 | South Indian | 485 | 3.24 | 80822 |

### Highest‑Rated Cuisines (min 100 restaurants)
| index | Cuisine | Restaurants | Avg rating | Votes |
| --- | --- | --- | --- | --- |
| 0 | Mediterranean | 110 | 4.02 | 80532 |
| 1 | European | 146 | 3.96 | 103305 |
| 2 | Seafood | 171 | 3.93 | 74254 |
| 3 | Asian | 228 | 3.9 | 104298 |
| 4 | Mexican | 174 | 3.87 | 74737 |
| 5 | Japanese | 134 | 3.83 | 34607 |
| 6 | American | 380 | 3.76 | 183106 |
| 7 | Italian | 726 | 3.75 | 329230 |
| 8 | Thai | 229 | 3.74 | 65922 |
| 9 | Continental | 699 | 3.71 | 288213 |

### Missing Values (Top 10 columns)
| Column | Missing |
|---|---|
| Cuisines | 9 |
| Restaurant ID | 0 |
| Currency | 0 |
| Rating text | 0 |
| Rating color | 0 |
| Aggregate rating | 0 |
| Price range | 0 |
| Switch to order menu | 0 |
| Is delivering now | 0 |
| Has Online delivery | 0 |

> **Note:** Cost comparisons across countries are not normalized for currency; any cross‑country “Average Cost for two” insights should be interpreted cautiously.

---

## 📈 Visualizations in the Notebook
The notebook includes:
- Bar plots of **rating counts** and **online delivery by country**.
- Count plot(s) of **rating text**.
- Pie charts for **city** and **cuisine** distributions.

> Plots are generated using `matplotlib`/`seaborn`. Ensure `%matplotlib inline` is enabled in Jupyter.

---

## 🚀 How to Run
1. Clone/download the repo and open the notebook:
   ```bash
   jupyter notebook "Data Analysis on Zomato Dataset/Data Analysis on  zomato dataset.ipynb"
   ```
2. Place `zomato (1) (2).csv` and (optionally) `Zomato_Country-Code.xlsx` in the same folder as the notebook.
3. Run cells top‑to‑bottom.

---

## 📦 Suggested Repo Layout (nice-to-have)
```
.
├─ data/                 # raw data
├─ notebooks/            # analysis notebooks
├─ reports/figures/      # exported charts
├─ src/                  # reusable helpers (if you add scripts)
└─ README.md
```

---

## 🙌 Acknowledgements
- Dataset inspired by public Zomato samples widely used in EDA tutorials.


