# Little Flower's Blooms Pricer

Wedding quote calculator for The Little Flower's Blooms by Amelie, a floral design business in Lafayette, Louisiana.

A one-page calculator for pricing wedding flower orders. Pick a flower style, tap in the pieces, set an hourly rate, and it shows the quote, the hourly pay after costs, a stem shopping list, deposit dates, and a client text ready to copy.

## How the price is built

For each piece:

- **Flowers:** stems × cost per stem for the chosen style × (1 + extra-stem buffer), plus the holiday bump when the date is within 2 weeks of Valentine's Day or Mother's Day
- **Supplies:** ribbon, pins, wristlets, vessels
- **Time:** minutes to make it, plus a share of the non-arranging hours (client meeting, buying and pickup, prepping stems, cleanup), × the hourly rate

Each piece rounds up to the nearest $1 under $30 and the nearest $5 above. Delivery is its own line: drive and setup hours × rate, plus gas.

## Starting numbers

| Setting | Default | Source |
|---|---|---|
| Cost per stem: Simple / Classic / Luxe | $1.00 / $1.75 / $3.00 | Blended from Sam's Club bulk roses ($1.05 to $1.80) and Whole Blossoms (carnations $0.35 to $1.00, garden roses about $5.56) |
| Extra stems | 15% | Fabulous Florals recommends 10% |
| Holiday bump | 20% | Estimate; Boston wholesale data showed about a 10% jump before Valentine's Day 2024 |
| Sales tax | 9% | Published Lafayette rates conflict (9% to 11%); confirm when registering |
| Deposit / balance due | 50% / 21 days before | Hana Florist POS contract guidance |
| Minutes per piece | Estimates | Replace with real times from a practice run |

All numbers are editable in the app under "Fine-tune my numbers" and save in the browser on that device.

## Running it

Static site, no build step. Open `index.html` in a browser, or deploy the folder as-is. It is hosted on Vercel and redeploys on every push to `main`.
