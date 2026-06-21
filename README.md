# Deckers Outdoor (DECK) — 3-Statement Financial Model & DCF Valuation

**Built by:** Tirth Patel  
**Model date:** June 2026  
**Ticker:** NYSE: DECK  
**Fiscal year end:** March 31  

---

## What This Is

A three-statement financial model (Income Statement, Balance Sheet, Cash Flow) and DCF valuation for Deckers Outdoor Corporation, built from scratch using primary SEC filings. Historical line items were sourced directly from SEC 10-K filings and cross-checked against reported totals. Projections are driven by a single Assumptions tab and aligned to management guidance where available.

---

## Key Outputs

| Metric | Value |
|---|---|
| DCF Implied Price | ~$109 |
| Current Price (June 2026) | ~$109 |
| Upside / (Downside) | ~0% (fairly valued) |
| WACC | 10.0% (CAPM: Rf 4.5% + β 1.15 × ERP 5.0%) |
| Terminal Growth Rate | 3.0% |
| Shares Outstanding | 141,502K (Q4 FY2026 diluted) |
| Net Cash | $1,889M (debt-free as of FY2025) |

**Sensitivity (implied $/share):**

| WACC ↓ / g → | 2.0% | 2.5% | 3.0% | 3.5% | 4.0% |
|---|---|---|---|---|---|
| 9.0% | ~$105 | ~$112 | ~$120 | ~$129 | ~$140 |
| 9.5% | ~$99 | ~$105 | ~$112 | ~$119 | ~$128 |
| **10.0%** | **~$93** | **~$99** | **~$109** | **~$116** | **~$124** |
| 10.5% | ~$88 | ~$94 | ~$99 | ~$106 | ~$113 |
| 11.0% | ~$83 | ~$88 | ~$94 | ~$100 | ~$107 |
| 11.5% | ~$79 | ~$83 | ~$88 | ~$94 | ~$101 |

---

## Model Structure

### Tabs
| Tab | Contents |
|---|---|
| **Assumptions** | All forecast drivers in one place — revenue growth, margins, working capital days, capex%, D&A%, WACC, terminal growth. Yellow cells = change these to run scenarios |
| **Income Statement** | FY2023–FY2025 historicals + FY2026E–FY2028E projections. All projection formulas link to Assumptions tab |
| **Balance Sheet** | Full balance sheet with working-capital drivers (DSO/DIO/DPO), PP&E roll-forward, equity roll-forward. CHECK row = 0 across all six years |
| **Cash Flow** | Indirect method. Integrates IS and BS — Δ working capital flows from BS changes, ending cash feeds back to BS |
| **DCF** | Unlevered FCF build → terminal value → EV → equity bridge → implied price. 6×5 WACC/growth sensitivity table |

### Three-Statement Integration
- Revenue flows IS → CF (net income) → BS (retained earnings)
- Working capital days (DSO/DIO/DPO) drive AR/Inventory/AP on BS → Δ flows to CF
- PP&E: prior balance + capex − D&A each period
- Cash: CF ending cash → BS cash (projection years)
- Equity: RE += net income + share repurchases; APIC += SBC
- BS check row verifies A = L + E across all historical and projection years

---

## Historical Data Sources

All historical figures pulled line-by-line from SEC EDGAR filings:

| Year | Source |
|---|---|
| FY2023 (ended March 31, 2023) | FY2024 10-K comparative column |
| FY2024 (ended March 31, 2024) | FY2024 10-K (filed July 2024) |
| FY2025 (ended March 31, 2025) | FY2025 Annual Report (filed June 2025) |

**Verification:** Every line item was independently verified to match the filing exactly (51/51 checks passed). Balance sheet cross-foots on every subtotal for all three historical years. Cash flow reconciles beginning + net change = ending cash for all years.

**Accuracy check vs. FY2026 actuals:** The FY2026E revenue projection ($5.484B) came within **0.3%** of the reported FY2026 actual ($5.472B), using only FY2025 10-K data as input.

---

## Projection Assumptions

### Revenue
| | FY2026E | FY2027E | FY2028E |
|---|---|---|---|
| Growth % | 10.0% | 9.0% | 8.0% |

FY2027 guidance from Deckers FY2026 press release (May 2026): revenue $5.86–$5.91B (high-single-digit growth). Model FY2027E ($5.978B) is slightly above the top of guidance range — treat as a mild upside case.

### Margins
| | FY2026E | FY2027E | FY2028E |
|---|---|---|---|
| Gross Margin % | 58.0% | 56.5% | 56.8% |
| SG&A % Revenue | 33.8% | 35.0% | 34.8% |
| EBIT Margin % | 24.2% | 21.5% | 22.0% |
| Tax Rate % | 22.3% | 23.0% | 23.0% |

FY2027 margins aligned to management guidance: GM ~56.5%, SG&A ~35%, operating margin ~21.5%.

### Working Capital
| | FY2026E | FY2027E | FY2028E |
|---|---|---|---|
| DSO (days) | 25 | 25 | 25 |
| DIO (days) | 88 | 87 | 86 |
| DPO (days) | 73 | 73 | 73 |

### Capital Allocation
| | FY2026E | FY2027E | FY2028E |
|---|---|---|---|
| Capex % Revenue | 2.0% | 2.2% | 2.2% |
| D&A % Revenue | 1.4% | 1.4% | 1.4% |
| Share Repurchases | $1,075M (FY2026 actual) | ~80% FCF | ~80% FCF |

---

## Investment View

**Fairly valued at current prices (~$109).** DCF implies ~$109/share at base-case assumptions — essentially no margin of safety at current levels.

**Bull case:** HOKA reaccelerates internationally (company guided low-double-digit HOKA growth for FY2027); gross margin recovers faster than expected from tariff/promotional headwinds. At 9.0% WACC and 3.5% terminal growth, implied price ~$129.

**Bear case:** Gross margin stays pressured (company guided ~56.5% FY2027 vs. FY2025's 57.9% peak); HOKA growth continues decelerating toward mid-single digits; operating deleverage from SG&A investment. At 11% WACC and 2.5% terminal growth, implied price ~$88.

**What would change the view:** HOKA quarterly unit growth data, gross margin trajectory, and DTC channel mix are the three metrics to watch. Deckers' next earnings release is July 23, 2026.

---

## WACC Build

| Input | Value | Source |
|---|---|---|
| Risk-Free Rate | 4.5% | 10Y US Treasury, June 2026 (~4.46%) |
| Beta | 1.15 | DECK 5-year monthly regression |
| Equity Risk Premium | 5.0% | Damodaran US ERP |
| Cost of Equity (CAPM) | 10.25% | 4.5% + 1.15 × 5.0% |
| **WACC** | **10.0%** | Rounded (debt-free, so WACC = cost of equity) |

Deckers carries no traditional long-term debt as of FY2025. WACC equals cost of equity.

---

## Files

| File | Description |
|---|---|
| `DECK_Model_Tirth_Patel_FINAL.xlsx` | The complete model — open in Excel, change yellow Assumptions cells to run scenarios |
| `deck_model_v2.py` | Python script (openpyxl) that builds the full workbook from scratch with all formatting, formulas, and verified historical data |
| `requirements.txt` | Python dependencies |

---

## Limitations

- FY2026E uses estimates, not FY2026 actuals (available May 2026 — next version will incorporate)
- Several balance sheet lines (prepaid, other accrued, lease liabilities) held flat from FY2025; not material to valuation but noted
- Interest income held flat rather than modeled against cash balance × yield
- Three explicit forecast years is shorter than a typical 5-year DCF; terminal value carries ~80% of EV
- Year-end discount convention (not mid-year)
- Share count held constant within each year; does not model intra-year buyback impact on EPS

---

## Requirements

```
openpyxl>=3.1.0
```

```bash
pip install -r requirements.txt
python deck_model_v2.py  # rebuilds DECK_Model_Tirth_Patel_FINAL.xlsx from scratch
```

---

*This model is built for educational and portfolio purposes. Not investment advice.*
