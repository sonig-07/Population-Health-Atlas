# Population & Health Atlas

A little dashboard I built to practice pulling a story out of public health data - life expectancy, health spending, child mortality, and doctor availability across 20 countries, 2000–2022.

**Live dashboard:** https://population-health-atlas.vercel.app/

This started as a learning/visualization project - mainly to practice picking the right chart for a question and actually saying something with the data instead of just plotting it. I later rebuilt the same dataset and story in **Power BI** and **SQL**, to practice the same analysis with a proper BI tool and querying instead of hardcoded JS.

## What it's trying to answer

- How has life expectancy moved since 2000, and where does COVID show up in the trend?
- Does spending more on healthcare actually buy longer life expectancy, or does it plateau?
- Which countries have cut child mortality the most since 2000, and which are still way behind?
- How does doctor availability compare across countries?

## What I found

- Spending helps a lot at the low end, then flattens hard. Life expectancy climbs fast as spending goes from near $0 to ~$2,000 per person, then barely moves after that — a country spending $12,000/person isn't living dramatically longer than one spending $5,000.
- COVID shows up as a real dip around 2020 for almost every country, and recovery by 2022 was uneven — some bounced back, some (US, Mexico) hadn't fully by the end of the dataset.
- Child mortality has dropped everywhere since 2000, even in countries with almost no health spending — probably the best news story in the whole dataset. Still, Nigeria's rate is over 30x Japan's.

## Built with

- Plain HTML/CSS/JS.

Everything's in one `.html` file, data included, so it just opens in a browser.

## Files here

- `population-health-atlas.html` — the dashboard itself
- `population_health_data.csv` — same data, for Power BI/Tableau/Excel/Pandas

## A note on the data

The numbers are realistic but **approximate** — compiled from general knowledge of World Bank/WHO-style figures, not pulled live from an API. Fine for practicing visualization and storytelling; swap in real numbers from [World Bank Open Data](https://data.worldbank.org) or [Our World in Data](https://ourworldindata.org) before using this for anything that actually matters.

## Other versions of this project

- **Power BI:** same CSV, rebuilt with a Power Query unpivot step for the trend chart, slicers instead of checkboxes for filtering
- **SQL:** same dataset queried directly for the same questions (trend over time, spend-vs-outcome, mortality ranking)

Doing the same analysis three ways (code, BI tool, SQL) was the actual point of the exercise - same questions, same data, different tools.
