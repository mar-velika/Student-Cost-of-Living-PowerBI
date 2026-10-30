# Cost of Living for International Students (Malaysia)

An interactive Power BI dashboard showing how far a monthly allowance goes in Malaysia,
in the student's own currency.

## Questions it answers
- How far does my allowance go after rent, food and other costs?
- Have living costs gone up, and what does my allowance buy now?
- Which states are cheaper?

## Preview
![Budget simulator](docs/page1-budget-simulator.png)
![Prices over time](docs/page2-prices-over-time.png)
![Where is cheaper](docs/page3-where-is-cheaper.png)

## Data sources
| Data | Source |
|---|---|
| CPI by state and category | OpenDOSM via data.gov.my |
| Exchange rates (monthly) | Bank Negara Malaysia via data.gov.my |
| Grocery prices | PriceCatcher via data.gov.my |
| Rent and accommodation | My own table (`data/student_assumptions.xlsx`), each row with a source link |

## How it was built
Power Query for cleaning, a star-schema model, DAX measures (Allowance in MYR,
Real Allowance, Basket Cost), and a selectable currency.

## Limitations
- PriceCatcher is a price-monitoring survey, not an official inflation measure.
- The rent table is a small sample, not statistically representative.
- Basket quantities are my own assumptions.
- Listing prices are a snapshot and may no longer be available.

## How to open it
Download `student-cost-of-living.pbix`, open it in Power BI Desktop, and update the
data folder parameter to where you saved the raw data files.
