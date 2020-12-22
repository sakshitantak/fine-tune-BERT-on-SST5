# Amazon Product Scraper
This is an `Amazon Product Scraper` built using `scrapy` module of `python`

# Features
it scrape various things
- Product Title
- Product Reviews
- Product Brand

By default it scrapes `Mobile Phones` of `7 Pages` from `Amazon`.
In case you want to change it to scrape other product, follow the instructions
1. Open file `/amazon_scraper/spiders/amazon_scraper.py`
2. Change the `urls` list at line `16`
3. Update `no_of_pages` variable to change number of pages to be scraped

# Execute Amazon Scraper
there are two ways to execute scraper
### First one
you can directly execute `run.sh` file using shell
```sh
sh ./run.sh
```

### Second one
you can execute the following command
```bash
scrapy crawl amazon_scraper -o ./data/data.json
```

It will create `data.json` file inside the `data` folder containing all the scraped data in `JSON` format.

# Sample Data
Already fetched sample data is available in `data` folder

# Troubleshooting
If `data.json` file doesn't generate in proper format then just delete `data.json` file.

# Prerequisites
-`scrapy`
-`pillow`

# Description
- scrapy.cfg : scrapy configuration file.
- spider : This directory contains all the spiders in the form of a python class. Whenever Scrapy is requested to run, it will be searched in this folder.
- items.py : Includes container that will be loaded with scraped data. Has the 'Mobile' class with attributes to be extracted.
- middlewares.py : Contains Spider's processing mechanism to handle requests and responses. Has models for spider middleware.
- pipelines.py : Contains a set of Python classes to process scraped data further.
- settings.py : Any customized settings can be added to this file.
- amazon-scraper/spiders/amazon_scraper.py : source code for scraping that has the parse definitions.