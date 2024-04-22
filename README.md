# Yad2 Scraper API

[![Oxylabs promo code](https://user-images.githubusercontent.com/129506779/250792357-8289e25e-9c36-4dc0-a5e2-2706db797bb5.png)](https://oxylabs.go2cloud.org/aff_c?offer_id=7&aff_id=877&url_id=112)


[![](https://dcbadge.vercel.app/api/server/eWsVUJrnG5)](https://discord.gg/GbxmdGhZjq)

Oxylabs’ [Yad2 Scraper](https://oxylabs.io/products/scraper-api/web/yad2?utm_source=github&utm_medium=repositories&utm_campaign=product) is a data gathering solution allowing you to extract real-time information from an Yad2 website effortlessly. This brief guide explains how an Yad2 Scraper works and provides code examples to understand better how you can use it hassle-free.

### How it works

You can get Yad2 results by providing your own URLs to our service. We can return the HTML for any Yad2 page you like.

#### Python code example

The example below illustrates how you can get HTML of Yad2 page.

```python
import requests
from pprint import pprint

# Structure payload.
payload = {
    'source': 'universal',
    'url': 'https://www.yad2.co.il/vehicles/cars'
}

# Get response.
response = requests.request(
    'POST',
    'https://realtime.oxylabs.io/v1/queries',
    auth=('user', 'pass1'),
    json=payload,
)

# Instead of response with job status and results url, this will return the
# JSON response with the result.
pprint(response.json())
```
Find code examples for other programming languages [**here**](https://github.com/oxylabs/yad2-scraper/tree/main/code%20examples)

#### Output Example
```json
{
  "results": [
    {
      "content": "<!doctype html>\n<html data-n-head-ssr class=\"first-entrance    vehicles cars category-subcategory md ... </html>",
      "created_at": "2023-12-18 11:20:07",
      "updated_at": "2023-12-18 11:20:08",
      "page": 1,
      "url": "https://www.yad2.co.il/vehicles/cars",
      "job_id": "7142473600249924609",
      "status_code": 200
    }
  ]
}
```
With our Yad2 Scraper, you can seamlessly collect public data from any Yad2 webpage. Conveniently gather the essential details of houses for sale or rent, such as the price, location, number of rooms, and property descriptions. This valuable information can help you study the housing market and get ahead of your competitors. Should you have any queries, feel free to reach out to our support team via live chat or email us at hello@oxylabs.io.
