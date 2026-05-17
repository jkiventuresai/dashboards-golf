# Golf Dashboard

Interactive golf performance dashboard for tracking scoring trends, handicap movement, course performance, shot patterns, club yardages, and course locations.

Repository: `dashboards-golf`

## Live Dashboard

After GitHub Pages is enabled, the dashboard should be available at:

`https://jkiventuresai.github.io/dashboards-golf/`

The live page uses `index.html` in the root of the repository.

## Current Dashboard Version

- Current version: `dashboard-golf-v2.html`
- GitHub Pages entry file: `index.html`
- Data snapshot date: generated from the uploaded CSV files available at the time of dashboard creation

## Folder Structure

```text
/
├── index.html
├── README.md
├── input-data/
│   ├── golf-club-yardage-mapping.csv
│   ├── golf-course-locations-mapping.csv
│   ├── golf-course-par-mapping.csv
│   ├── golf-course-ratings-tracker-2025.csv
│   ├── golf-course-ratings-tracker-2026.csv
│   ├── golf-ghin-formula-mapping.csv
│   ├── golf-score-tracker-2025.csv
│   ├── golf-score-tracker-2026.csv
│   ├── golf-shot-tracker-2025.csv
│   └── golf-shots-tracker-2025.csv
├── output-data/
│   ├── dashboard-golf-v2.html
│   └── dashboard-golf-v2-code.txt
└── docs/
    └── Instructions-GolfDashboardUpdate-v1.md
```

## What This Dashboard Tracks

### Score and Handicap Reporting

- Total rounds played
- Average score
- Best score
- Worst score
- Score trend by date
- Estimated handicap / tracker formula trend
- Course-by-course performance
- Par comparison by course

### Round Pattern Analysis

- Front 9 vs. Back 9 scoring
- Hole-by-hole scoring trends
- 3-hole segment scoring trends
- Late-round fade detection
- Weekday vs. weekend pattern review
- Insights that flag where performance tends to slip during a round

### Shot and Skill Analysis

- Tee, fairway, approach, recovery, and putting shot trends
- Simulator / indoor shot data analysis where available
- Club yardage mapping
- Yardage gap review

### Course Location Map

- Displays course locations geographically
- Shows where rounds have been played
- Uses course-location mapping data from `golf-course-locations-mapping.csv`

## Important Data Note

The dashboard is self-contained. The data is embedded inside the HTML file at the time the dashboard is generated.

This means:

- Updating CSV files in `input-data/` will **not** automatically update the live dashboard.
- The dashboard must be regenerated after new golf data is added.
- Each regenerated version should be saved as a new version, such as `dashboard-golf-v3.html`.

## Correct Update Workflow

1. Add the new round, rating, shot, or course data to the correct CSV file in `input-data/`.
2. Save the CSV file.
3. Ask ChatGPT to regenerate the dashboard using the updated files.
4. Name the new dashboard version sequentially, for example:
   - `dashboard-golf-v3.html`
   - `dashboard-golf-v3-code.txt`
5. Replace the root `index.html` file with the newest dashboard HTML.
6. Add the new dashboard version to `output-data/` for version history.
7. Upload the updated files to GitHub.

## GitHub Upload Instructions

Use this package as the starting upload to the repository.

### Initial Upload

1. Open the GitHub repository.
2. Select **Add file**.
3. Select **Upload files**.
4. Drag the contents of this package into the upload page.
5. Commit the upload to the `main` branch.

### Enable GitHub Pages

1. Open repository **Settings**.
2. Go to **Pages**.
3. Under **Build and deployment**, choose:
   - Source: `Deploy from a branch`
   - Branch: `main`
   - Folder: `/root`
4. Save.
5. Wait for GitHub Pages to publish the site.

## Versioning Rules

Use this naming format:

```text
dashboard-golf-v#.html
dashboard-golf-v#-code.txt
```

Example:

```text
dashboard-golf-v3.html
dashboard-golf-v3-code.txt
```

The root `index.html` should always be a copy of the newest approved dashboard version.

## Future Improvement Ideas

- Add latitude and longitude columns to `golf-course-locations-mapping.csv` for more accurate map plotting.
- Add weather conditions per round.
- Add tee box used per round.
- Add driving accuracy, greens in regulation, putts, penalties, and sand saves.
- Add practice session data and compare it against scoring improvement.
- Add separate dashboard tabs for scoring, course strategy, club distances, and handicap tracking.

## Current Status

This repository is ready for GitHub upload and GitHub Pages publishing.
