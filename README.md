# webcscrapersTools
 Tools that help web crawlers become less unstable



## User Agent

User Agent is a tool that works on behalf of the user and tells the server about which web browser the user is using for visiting the website.


```
user_agent = get_random_ua()
headers = {
        'user-agent': user_agent,
    }

r = requests.get('example.com',headers=headers)
```

## Using Delays

It’s always good to put some delay between requests, like below:

```
import numpy as np

delays = [7, 4, 6, 2, 10, 19]
delay = np.random.choice(delays)
time.sleep(delay)
```

## Proxy IPs

```
import requests

r = requests.get('example.com',headers=headers,proxies={'https': proxy_url})
```

Using Selenium with proxy:

```
from selenium import webdriver
import requests

r = requests.get('example.com',headers=headers,proxies={'https': proxy_url})
proxy = get_random_proxy().replace('\n', '')
        service_args = [
            '--proxy={0}'.format(proxy),
            '--proxy-type=http',
            '--proxy-auth=user:password'
        ]
        print('Processing..' + url)
        driver = webdriver.PhantomJS(service_args=service_args)
```
