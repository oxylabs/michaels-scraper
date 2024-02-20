# Michaels Scraper API

[![Oxylabs promo code](https://user-images.githubusercontent.com/129506779/250792357-8289e25e-9c36-4dc0-a5e2-2706db797bb5.png)](https://oxylabs.go2cloud.org/aff_c?offer_id=7&aff_id=877&url_id=112)

Oxylabs' [Michaels Scraper](https://oxylabs.io/products/scraper-api/ecommerce/michaels?utm_source=github&utm_medium=repositories&utm_campaign=product) is a data gathering solution allowing you to extract real-time information from an Michaels website effortlessly. This brief guide showcases how Michaels Scraper works, along with code examples to help you better understand how to use it hassle-free.

### How it works

You can get Michaels results by providing your own URLs to our service. We can return the HTML for any page you like.

#### Python code example

The example below illustrates how you can get HTML of Michaels page.

```python
import requests
from pprint import pprint

# Structure payload.
payload = {
    'source': 'universal_ecommerce',
    'url': 'https://www.michaels.com/shop/papercraft/paper/cardstock-paper'
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
Find code examples for other programming languages [**here**](https://github.com/oxylabs/michaels-scraper/tree/main/code%20examples)

#### Output Example
```json
{
  "results": [
    {
      "content": "<!DOCTYPE html><html lang=\"en_US\"><head><script type=\"text/javascript\" defer src=\"//static.platform. ... </html>",
      "created_at": "2024-02-20 12:37:37",
      "updated_at": "2024-02-20 12:37:38",
      "page": 1,
      "url": "https://www.michaels.com/shop/papercraft/paper/cardstock-paper",
      "job_id": "7165685927149341697",
      "status_code": 200
    }
  ]
}
```
With our Michaels Scraper, you can smoothly pull public data from any Michaels web page. Gather necessary craft supply information, including the cost, customer feedback, or detailed descriptions, to evaluate the arts and crafts market and keep a step ahead of your competitors. If you require any assistance, connect with our support team through live chat or email us at hello@oxylabs.io.