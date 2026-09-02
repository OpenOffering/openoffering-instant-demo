# OpenOffering Instant — interactive demo

A single-file, no-build demo of the OpenOffering **Instant** console: an issuer
(City of Falls Church, Virginia) draws funds against standing pre-bids in one press.

**Live:** https://openoffering.github.io/openoffering-instant-demo/

Everything is client-side and illustrative — no API, no data leaves the page.

## What works

- **Purpose of the bond** and **borrow amount** (with $25K / $100K / $1M / Max presets)
- **Maturity slider**, 5–30 years — the rate rises linearly with term:
  `4.71% + (years − 10) × 0.03` (4.71% is treated as the 10-year benchmark, +3 bp/yr)
- **First-year interest** recalculates live; **pre-bid capacity bar** tracks the request
- Amounts above the $7,355,317 pre-bid book fall back to a full auction
- **Change account** edits and saves the destination account
- Full issue flow: approvals double-check (bond counsel + municipal advisor, both
  starting *Not approved*) → Matching Buyers / Issuing Bond / Confirming Bond CUSIP
  → confetti confirmation with the bond CUSIP

## Numbers

| Value | Source |
| --- | --- |
| Moody's AAA, $574M outstanding, $7,355,317 pre-bids | given |
| 4.71% | given, treated as the 10-year benchmark |
| Rate curve, +3 bp per year of maturity | illustrative |
| Interest, first year | `amount × rate`, no amortization structure assumed |
| CUSIP `306567RZ3` | a real City of Falls Church CUSIP, used for the demo |

Design system (Castoro + Instrument Sans, #099E83 teal, #0A1B17 dark panels) matches
the OpenOffering site.
