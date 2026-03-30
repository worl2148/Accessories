# Men's Accessories Scraper

This module scrapes men's accessories products from Boutiqaat.com.

## Covered Subcategories

- Prayer Beads
- Gift Sets
- Caps & Beanies
- Bands & Gloves
- Pens
- Men Scarves

## Features

- **Async Processing**: Uses asyncio with semaphore (max 3 concurrent) for efficient scraping
- **Playwright Integration**: Handles JavaScript-rendered content and infinite scroll
- **S3 Integration**: Uploads product images and Excel files to AWS S3
- **Excel Generation**: Creates formatted Excel workbooks with product data
- **Date Partitioning**: Stores data in S3 with year/month/day structure

## S3 Storage Path

```
boutiqaat-data/year=YYYY/month=MM/day=DD/men/accessories/
```

## Usage

```bash
python -m men_accessories_sub1.main
```

## Dependencies

- Python 3.11+
- playwright
- beautifulsoup4
- boto3
- openpyxl

## Part of GitHub Actions Workflow

This module runs as part of the automated daily workflow at 4:00 AM UTC.
