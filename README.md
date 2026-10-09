# Rental Deposit Calculator

A responsive calculator for property rental move-in charges. All calculations run in the browser; it does not save or upload tenant records.

## Features

- Monthly rent = base rate + RM40 utilities + optional RM50 for one additional pax + selected parking
- Prorated advance rental based on base rate, move-in date and the number of days in that month
- Security deposit: 1 or 2 months of base rate, less RM3.33
- Utilities deposit: 0.5 month of base rate, less RM3.33
- Tenancy agreement fee (RM220), parking admin fee (RM100), parking deposit, building access card deposit, key & key tag deposit
- Configurable SST rate and selectable taxable items
- Copy payment breakdown and print/save as PDF
- No login and no database

## Free GitHub Pages deployment

The repository includes `.github/workflows/pages.yml`.

**Important:** GitHub Free supports GitHub Pages for public repositories. This repository is currently private; publishing with GitHub Pages on a free personal plan requires changing it to public. That makes the source code visible to everyone. No tenant records are stored in this repository.

After deciding to make the repository public:

1. Open **Settings → General → Danger Zone → Change repository visibility** and change visibility to **Public**.
2. Open **Settings → Pages** and set **Build and deployment → Source** to **GitHub Actions**.
3. The workflow deploys when changes are pushed to `main`. After a successful run, the site URL appears under **Settings → Pages** and should use the pattern `https://roger9777.github.io/rental-deposit-calculator/`.

## Calculation notes

- The RM3.33 deduction is applied separately to security deposit and utilities deposit as requested. Verify this with the billing rules you actually use.
- Prorated advance rental counts the move-in date as a chargeable day when calculating through the end of the month. There is also a manual chargeable-days option.
- SST is not determined automatically from tax law. The rate and taxable items are user-controlled settings, so confirm which charges should be taxed before sending a statement.
- Monthly total rent is displayed separately and is excluded from the move-in total.
