# Fast-food protein and calories, US menus (259 items)

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.24541968.svg)](https://doi.org/10.5281/zenodo.24541968)

This file has protein, calories and other nutrition values for 259 menu items at five US chains: McDonald's, Burger King, Subway, Starbucks and Chipotle. We copied every number from the chain's own published nutrition data on the date shown in the file.

It is the data behind the free [Protein Finder](https://health.dailyappslab.com/macroscout/protein-finder/), where you can filter the same items by protein and calories in a browser.

## The file

`fast-food-protein-us.csv` has one row per menu item.

| Column | Meaning |
|---|---|
| `chain` | The restaurant chain |
| `item` | The item's name as the chain writes it |
| `meal` | `main`, `breakfast` or `drink` |
| `calories` | Calories per item (kcal) |
| `protein_g` | Protein in grams |
| `protein_g_per_100_kcal` | Protein divided by calories, times 100. This column is our calculation |
| `carbs_g`, `fat_g`, `sodium_mg`, `sugars_g`, `caffeine_mg` | Filled only where we copied the value (see Limits) |
| `note` | Serving details, such as "Sharing box" or "At participating locations" |
| `source`, `source_url` | The chain's nutrition page the numbers came from |
| `date_read` | The date we read the numbers from that page |

## Where the numbers come from

| Chain | Items | Source | Date read |
|---|---|---|---|
| McDonald's | 43 | [McDonald's Nutrition Calculator (US)](https://www.mcdonalds.com/us/en-us/about-our-food/nutrition-calculator.html) | 2026-10-22 |
| Burger King | 84 | [Burger King Nutrition Explorer (US)](https://www.bk.com/nutrition-explorer) | 2026-10-22 |
| Subway | 90 | [Subway U.S. Nutrition Information, October 2026 (PDF)](https://media.subway.com/dam/urn:aaid:aem:f20a4541-8c88-496b-940d-4aa8318cae26/original/as/us-nutrition-en.pdf) | 2026-10-22 |
| Starbucks | 31 | [Starbucks Protein Beverages (US menu)](https://www.starbucks.com/menu/drinks/protein-beverages) | 2026-10-22 |
| Chipotle | 11 | [Chipotle Nutrition Calculator, Burrito Bowl (US)](https://www.chipotle.com/nutrition-calculator/burrito-bowl) | 2026-10-17 |

## What we added

- Protein per 100 calories is protein divided by calories, times 100, rounded to one decimal.
- Subway footlong rows are Subway's 6-inch values doubled, which is how Subway says to work out a footlong. The `note` column says "Subway's 6-inch values doubled" on each of those rows.
- Chipotle rows marked "our build" are bowls we added up from Chipotle's own ingredient values. The `note` column lists the ingredients so you can rebuild them.

## Limits

- US menus only. The same item can have different numbers in other countries.
- Chains change recipes and menus. Treat `date_read` as the date the row was true, and check the chain's page before relying on a value.
- Calories and protein are filled for all 259 rows. Carbs are filled for 65 rows, fat for 77, sodium for 165, sugars for 68 and caffeine for 26.
- Nothing here is medical or dietary advice.

## Use and credit

The nutrition numbers are facts published by the chains. Our compilation and the calculated column are free to reuse under CC BY 4.0. Please credit "MacroScout by Daily Apps Lab" and link the [Protein Finder](https://health.dailyappslab.com/macroscout/protein-finder/).

To cite it: Iqbal, J. (2026). *Fast-food protein and calories, US menus* (Version 1.0.0) [Data set]. Zenodo. https://doi.org/10.5281/zenodo.24541968

The same data, with a preview table, is at [dailyappslab.github.io/data/fast-food-protein-us](https://dailyappslab.github.io/data/fast-food-protein-us/).

## Who made this

Javed Iqbal, an independent developer at [Daily Apps Lab](https://dailyappslab.com/), publishes this dataset and makes MacroScout, a calorie and macro tracker that scans restaurant menus. If you find a wrong number, tell us through the [contact page](https://dailyappslab.com/contact/) and we'll check it against the chain's page.
