# mega-scraper

scrape a website's content.

> built-in support for amazon product reviews.

```
npm i -g mega-scraper

mega-scraper https://www.amazon.com/PlayStation-4-Slim-1TB-Console/dp/B071CV8CG2/
```

## requirements

- running redis instance on host 0.0.0.0 port 6379 (or with `$REDIS_HOST` and `$REDIS_PORT`) or spin it up with docker

- on debian/ubuntu, install additional required libraries via `sudo apt install -y gconf-service libasound2 libatk1.0-0 libc6 libcairo2 libcups2 libdbus-1-3 libexpat1 libfontconfig1 libgcc1 libgconf-2-4 libgdk-pixbuf2.0-0 libglib2.0-0 libgtk-3-0 libnspr4 libpango-1.0-0 libpangocairo-1.0-0 libstdc++6 libx11-6 libx11-xcb1 libxcb1 libxcomposite1 libxcursor1 libxdamage1 libxext6 libxfixes3 libxi6 libxrandr2 libxrender1 libxss1 libxtst6 ca-certificates fonts-liberation libappindicator1 libnss3 lsb-release xdg-utils wget`

## cli options

### `--headless` [default: true]

set to `false` to run the scraper in "headful" mode (non-headless)

e.g.

```
mega-scraper https://www.amazon.com/PlayStation-4-Slim-1TB-Console/dp/B071CV8CG2/ --headless false
```

### `--screenshot` [default: true]

set to `false` to avoid taking a screenshot of each scraped page

e.g.

```
mega-scraper https://www.amazon.com/PlayStation-4-Slim-1TB-Console/dp/B071CV8CG2/ --headless false
```

### `--proxy` [default: true]

set to `false` to avoid proxying each request through a free proxy service (currently the module [`get-free-https-proxy`](https://www.npmjs.com/package/get-free-https-proxy) is used)

e.g.

```
mega-scraper https://www.amazon.com/PlayStation-4-Slim-1TB-Console/dp/B071CV8CG2/ --proxy false
```

### `--timeout` [default: 5000]

set the timeout to a desired number in milliseconds (5000 = 5 seconds)

e.g.

```
mega-scraper https://www.amazon.com/PlayStation-4-Slim-1TB-Console/dp/B071CV8CG2/ --timeout 10000
```

### `--images` [default: true]

set to `false` to avoid loading images

e.g.

```
mega-scraper https://www.amazon.com/PlayStation-4-Slim-1TB-Console/dp/B071CV8CG2/ --images false
```

### `--stylesheets` [default: true]

set to `false` to avoid loading stylesheets

e.g.

```
mega-scraper https://www.amazon.com/PlayStation-4-Slim-1TB-Console/dp/B071CV8CG2/ --stylesheets false
```

### `--javascript` [default: true]

set to `false` to avoid loading javascript

e.g.

```
mega-scraper https://www.amazon.com/PlayStation-4-Slim-1TB-Console/dp/B071CV8CG2/ --javascript false
```


### `--blocker` [default: true]

set to `false` to avoid blocking requests like images, stylesheets, javascript, fonts, etc.

e.g.

```
mega-scraper https://www.amazon.com/PlayStation-4-Slim-1TB-Console/dp/B071CV8CG2/ --blocker false
```


### `--blocker` [default: true]

set to `false` to avoid blocking useless resources

e.g.

```
mega-scraper https://www.amazon.com/PlayStation-4-Slim-1TB-Console/dp/B071CV8CG2/ --blocker false
```

### `--monitor` [default: true]

set to `false` to avoid opening the web dashboard on localhost:4000

e.g.

```
mega-scraper https://www.amazon.com/PlayStation-4-Slim-1TB-Console/dp/B071CV8CG2/ --monitor false
```

### `--exit` [default: false]

set to `true` to exit the program with success or failure status code once done scraping.

e.g.

```
mega-scraper https://www.amazon.com/PlayStation-4-Slim-1TB-Console/dp/B071CV8CG2/ --exit
```

### `--cookie` [default: none]

set to a desired cookie to further prevent detection

e.g.

```
mega-scraper https://www.amazon.com/PlayStation-4-Slim-1TB-Console/dp/B071CV8CG2/ --cookie 'my=cookie'
```