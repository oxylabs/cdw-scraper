# Cdw Scraper API

[![Oxylabs promo code](https://user-images.githubusercontent.com/129506779/250792357-8289e25e-9c36-4dc0-a5e2-2706db797bb5.png)](https://oxylabs.go2cloud.org/aff_c?offer_id=7&aff_id=877&url_id=112)

Oxylabs' [Cdw Scraper](https://oxylabs.io/products/scraper-api/ecommerce/cdw?utm_source=github&utm_medium=repositories&utm_campaign=product) is a data gathering solution allowing you to extract real-time information from an Cdw website effortlessly. This brief guide showcases how Cdw Scraper works, along with code examples to help you better understand how to use it hassle-free.

### How it works

You can get Cdw results by providing your own URLs to our service. We can return the HTML for any page you like.

#### Python code example

The example below illustrates how you can get HTML of Cdw page.

```python
import requests
from pprint import pprint

# Structure payload.
payload = {
    'source': 'universal_ecommerce',
    'url': 'https://www.cdw.com/search/cables/?key=&w=b'
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
Find code examples for other programming languages [**here**](https://github.com/oxylabs/cdw-scraper/tree/main/code%20examples)

#### Output Example
```json
{
  "results": [
    {
      "content": "\r\n<!DOCTYPE html>\r\n<html lang=\"en\">\r\n<head>\r\n    <meta content=\"text/html; charset=utf-8\" http-equiv ... </html>",
      "created_at": "2024-02-20 12:31:09",
      "updated_at": "2024-02-20 12:31:11",
      "page": 1,
      "url": "https://www.cdw.com/search/cables/?key=&w=b",
      "job_id": "7165684299969071105",
      "status_code": 200
    }
  ]
}
```
With our Cdw Scraper, you can effortlessly harvest public data from any Cdw web page. Compile the needed product specifics, like tech specs, customer reviews, or warranty details, to feed your market research and outsmart your competitors. Should you require any assistance, our support team is readily available via live chat or you can email us at hello@oxylabs.io.