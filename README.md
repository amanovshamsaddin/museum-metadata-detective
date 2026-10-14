# Museum Metadata Detective

A simple R-based data science project for identifying and prioritising possible metadata-quality issues in the Museum of Modern Art (MoMA) collection.

## Project goal

Large museum collections can contain missing, inconsistent or unusual metadata. Manually checking every record is inefficient.

This project asks:

> Can simple and interpretable data-science methods reduce a large museum catalogue to a smaller set of records for human review?

## Data

Source: Museum of Modern Art (MoMA) open collection data

- 160,705 artwork records
- 15,934 artist records

Official dataset:
https://github.com/MuseumofModernArt/collection

## Methods

The project uses four transparent screening signals:

1. Missing core metadata
2. Medium formatting inconsistencies
3. Logical date contradictions
4. Extreme artwork dimensions

The signals are combined into review-priority tiers.

## Main findings

- 17,165 records had at least one missing core field
- 1,205 records had Medium formatting inconsistencies
- 254 records had extreme-size flags
- 10 records had strong chronological contradictions
- 65 records were placed in the two highest-priority tiers
- These 65 records represent about 0.04% of the full collection

A known Johan Thorn Prikker metadata inconsistency was also successfully identified by the logical-date rule.

## Tools

- R
- RStudio
- tidyverse
- ggplot2
- R Markdown

## Important limitation

A flag does not mean that a museum record is definitely wrong.

Different departments, object types and historical cataloguing practices can naturally produce unusual metadata. The system is designed to support human review, not replace curators.

## Files

- `museum_metadata_analysis.Rmd` — full R analysis
- `museum_metadata_report.pdf` — project report

## Future improvements

Possible next steps include:

- validating flagged records manually
- expanding standardisation to more metadata fields
- comparing ranked review against random review
- applying the method to other museum collections
- building a simple review dashboard
