# India-Stocks-571-600-Historical-Data

Institutional Historical 1-Minute Market Data Archive for **India Equities (Constituents 571 to 600)** with automated daily cloud capture via GitHub Actions.

---

## 🏛️ Directory Hierarchy

```text
India-Stocks-571-600-Historical-Data/
├── .github/workflows/daily_ingest.yml
├── fetch_batch.py
├── README.md
├── <SYMBOL>/
│   └── 1m/
│       ├── README.md
│       └── <YYYY>/
│           └── <MM>/
│               ├── <SYMBOL>_1m_<YYYY-MM-DD>.csv
```

---

## ⏰ 4-Tier Automated Schedule (Mon–Fri)

| Trigger | Time (IST) | Cron (UTC) | Role |
|:---|:---:|:---:|:---|
| **Primary Trigger** | **15:45 IST** | `15 10 * * 1-5` | 15 mins post-market close |
| **Backup Trigger 1** | **16:45 IST** | `15 11 * * 1-5` | 1 hour safety net |
| **Backup Trigger 2** | **17:45 IST** | `15 12 * * 1-5` | 2 hours safety net |
| **Backup Trigger 3** | **18:45 IST** | `15 13 * * 1-5` | 3 hours safety net |

---

## 📦 Constituents (571 to 600)

| # | Symbol | Company Name | Yahoo Ticker |
|---|---|---|---|
| 571 | `AGROPHOS` | Agro Phos India Limited | `AGROPHOS.NS` |
| 572 | `AGSTRA` | AGS Transact Technologies Limited | `AGSTRA.NS` |
| 573 | `AHCL` | Anlon Healthcare Limited | `AHCL.NS` |
| 574 | `AHLADA` | Ahlada Engineers Limited | `AHLADA.NS` |
| 575 | `AHLEAST` | Asian Hotels (East) Limited | `AHLEAST.NS` |
| 576 | `AHLUCONT` | Ahluwalia Contracts (India) Limited | `AHLUCONT.NS` |
| 577 | `AHLWEST` | Asian Hotels (West) Limited | `AHLWEST.NS` |
| 578 | `AIRAN` | Airan Limited | `AIRAN.NS` |
| 579 | `AIROLAM` | Airo Lam limited | `AIROLAM.NS` |
| 580 | `AJAXENGG` | Ajax Engineering Limited | `AJAXENGG.NS` |
| 581 | `AJMERA` | Ajmera Realty & Infra India Limited | `AJMERA.NS` |
| 582 | `AJOONI` | Ajooni Biotech Limited | `AJOONI.NS` |
| 583 | `AKASH` | Akash Infra-Projects Limited | `AKASH.NS` |
| 584 | `AKCAPIT` | AK Capital Services Limited | `AKCAPIT.NS` |
| 585 | `AKG` | Akg Exim Limited | `AKG.NS` |
| 586 | `AKI` | AKI India Limited | `AKI.NS` |
| 587 | `AKSHAR` | Akshar Spintex Limited | `AKSHAR.NS` |
| 588 | `AKSHARCHEM` | AksharChem India Limited | `AKSHARCHEM.NS` |
| 589 | `AKSHOPTFBR` | Aksh Optifibre Limited | `AKSHOPTFBR.NS` |
| 590 | `AKUMS` | Akums Drugs and Pharmaceuticals Limited | `AKUMS.NS` |
| 591 | `ALANKIT` | Alankit Limited | `ALANKIT.NS` |
| 592 | `ALBERTDAVD` | Albert David Limited | `ALBERTDAVD.NS` |
| 593 | `ALEMBICLTD` | Alembic Limited | `ALEMBICLTD.NS` |
| 594 | `ALFREDHE` | Alfred Herbert India Limited | `ALFREDHE.NS` |
| 595 | `ALGOQUANT` | Algoquant Fintech Limited | `ALGOQUANT.NS` |
| 596 | `ALICON` | Alicon Castalloy Limited | `ALICON.NS` |
| 597 | `ALIVUS` | Alivus Life Sciences Limited | `ALIVUS.NS` |
| 598 | `ALKALI` | Alkali Metals Limited | `ALKALI.NS` |
| 599 | `ALKYLAMINE` | Alkyl Amines Chemicals Limited | `ALKYLAMINE.NS` |
| 600 | `ALLCARGO` | Allcargo Logistics Limited | `ALLCARGO.NS` |


---

## ⚡ 1-Line Pandas Stream Loader

```python
import pandas as pd

# Example: Stream AGROPHOS 1m data
url = "https://raw.githubusercontent.com/parshant65-lang/India-Stocks-571-600-Historical-Data/main/AGROPHOS/1m/2026/10/AGROPHOS_1m_2026-10-12.csv"
df = pd.read_csv(url)
print(df.head())
```
