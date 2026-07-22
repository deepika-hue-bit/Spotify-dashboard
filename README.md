# Spotify Music Analytics Dashboard

An end-to-end Power BI dashboard analyzing 85,000 Spotify tracks (2015–2025) to surface streaming trends, genre performance, top artists/labels, and audio-feature patterns — built from a raw CSV through data cleaning, modeling, DAX measures, and a two-page interactive report.

## Overview
85,000 tracks | 62,000 artists | 18.2B total streams
Coverage: 2015–2025, 12 genres, 10 countries, 8 record labels
Fully filterable by Country, Year, and Genre across both report pages

## Problem → Solution

Raw streaming data (release dates, genres, artists, labels, popularity, audio features) is hard to interrogate in flat file form — no way to quickly see trends, 
top performers, or feature-performance relationships. This project cleans and models that data, then builds a self-service Power BI dashboard so anyone can filter, 
explore, and pull answers instantly instead of manually querying a spreadsheet.
Power BI dashboard analyzing 85,000 tracks (2015-2025) — streams, genres,
artists, labels, and audio characteristics.

## Contents
- `spotify_analysis.pbix` — the Power BI report
- `spotify_cleaned.csv` — cleaned source data
- `spotify_2015_2025_85k.csv` — source dataset
- `page1.png` — preview_1
- `page2.png` — preview_2

## Key metrics
- 18.2B total streams, 85K tracks, 62K artists
- Avg popularity: 48.16/100

## Dashboard pages

Page 1 — Overview KPI cards (Total Streams, Tracks, Artists, Avg Popularity), Streams Over Time, Popularity Tier breakdown, Genres by Streams, Danceability vs Energy scatter.

Page 2 — Labels, Artists & Audio Profile Streams by Label (treemap), Top 20 Artists table, Audio Profile comparison (danceability/energy/instrumentalness by genre).

## Key techniques used
Data cleaning & feature engineering in Python (nulls handled, calculated columns added) before import
Power Query type correction on import
Custom Date table (CALENDAR()) for accurate time-based filtering
DAX measures: Total Streams, Total Tracks, Total Artists, Avg Popularity, Explicit %, Streams YoY %, Streams per Track, Top Genre by Streams
Organized measures in a disconnected _Measures table
Cross-page synced slicers (Country / Year / Genre)

## Key findings
Streams held steady between 1.4B–1.9B per year across the decade — no growth trend, but no decline either
51% of tracks fall into the "Moderate" popularity tier; only 3.5% are "Viral"
Genre performance is closely bunched — no single genre dominates the catalog
Danceability and energy show no strong relationship to stream volume

## Tools

Power BI Desktop · DAX · Power Query · Python (pandas, for pre-cleaning)
