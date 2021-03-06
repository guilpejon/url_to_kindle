Article to Kindle
====================

Intro
-----

Send your favorite medium articles to kindle as .pdfs!

Installation
------------

* Install [Docker](https://www.docker.com/get-started)
* Create a new gmail account
  * Make sure two factor authentication is **disabled**
  * [Enable](https://support.google.com/accounts/answer/6010255?hl=en) less secure app access
* [Allow](https://www.amazon.com/gp/help/customer/display.html?nodeId=201974240) your amazon account to receive emails from that account
* Download this project and create an `.env` file on its root with the following content:
  * GMAIL_USER=YOUR_GMAIL_ACCOUNT
  * GMAIL_PASSWORD=YOUR_GMAIL_PASSWORD
  * KINDLE_EMAIL=YOUR_KINDLE_EMAIL

Usage
------------

```bash
docker build -t article_to_kindle .
```

Then, anytime you want a new article sent to your kindle, you just have to
run:

```bash
docker run article_to_kindle MEDIUM_ARTICLE_URL
```
