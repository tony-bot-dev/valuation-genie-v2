# ValuationGenie Data Layer

This directory contains the foundational data for the ValuationGenie MVP.

## Files

### 1. `sba-loans.csv` (Local Only)
- **Source:** SBA Open Data (FOIA) - data.sba.gov
- **Description:** Raw SBA 7(a) loan data FY2020-2026 (135MB)
- **Note:** Too large for GitHub - kept locally only

### 2. `sba-analysis.md`
- **Source:** Derived from SBA data
- **Key Stats:**
  - 310K active/completed loans
  - $164B total dollar volume
  - Average loan: ~$530K
  - Sector breakdowns by NAICS code

### 3. `bizbuysell-insights.json`
- **Source:** BizBuySell Insight Reports (2025-2026)
- **Description:** Market transaction data, median prices, multiples
- **Key Stats:**
  - Median sale price: $350K
  - Median cash flow: $159K

### 4. `industry-multiples.json`
- **Source:** Industry publications
- **Description:** Valuation multiples by business type
- **Coverage:** 14 industries with SDE and revenue multiples

## Data Currency

| File | Last Updated | Refresh Schedule |
|------|--------------|------------------|
| sba-analysis.md | Mar 2026 | Quarterly |
| bizbuysell-insights.json | Mar 2026 | Quarterly |
| industry-multiples.json | Mar 2026 | Annually |

## Known Limitations

1. **SBA Data:** Does not distinguish acquisition vs startup loans
2. **BizBuySell:** No individual transaction-level data (aggregates only)
3. **Multiples:** General ranges - actual valuations depend on specifics

## How to Use in Valuation Engine

1. **Industry identification:** Use NAICS code → sector mapping
2. **Benchmark data:** Pull sector averages from SBA and BizBuySell
3. **Multiple selection:** Reference industry-multiples.json for baseline
4. **Adjustments:** Apply +/- based on risk factors

---
*ValuationGenie Data Layer v1.0 - March 2026*
