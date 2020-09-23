# Portfolio position tracker
Tracks stock, funds, crypto asset portfolio including gains / losses, dividends etc using python. Can track any assets listed on [yfinance](https://github.com/ranaroussi/yfinance), [investpy](https://github.com/alvarobartt/investpy) and [binance](https://github.com/sammchardy/python-binance)

See my [Medium post](https://medium.com/@gerard_syd/python-stock-portfolio-tracker-4bf6d082f564) for information on how to use:

## Update 23 September 2020
- Included bootstrap across app
- Added login structure
- Added database migration config (using flask-migrate)
- Updated templates for bootstrap

## Update 13 September 2020
- Updated Flask app structure using Miguel Grinberg format (https://blog.miguelgrinberg.com/post/the-flask-mega-tutorial-part-i-hello-world)
- Updated Flask to include login

## Update 24 August 2020
- Added dashboard for each stock 
- Added support for crypto with conversion into AUD, EUR, GBP, USD and ZAR (using Binance API)

## Installation
- Clone the repository and install using pipfile (if using pipenv) or requirements.txt (for other virtual environments)
- Required ENV variables (via .env file or any other method):
    FLASK_APP='pftracker.py'
    SECRET_KEY='anylongstringtouseasflasksecretkey'
- If you want to use the crypto pricing functionality, sign up for a Binance account and get the API key / secret and store them in a .env file as follows:
    BINANCE_API_KEY='{your API Key}'
    BINANCE_API_SECRET='{your API Secret}'

## Known bugs
- If quantity / price / fees are blank when providing trade data, portfolio calculations do not work as expected (when using Load Portfolio)

## To be built / implemented
- Add trades to SQL dbase linked to user
- Move portfolio actions to separate user profile page
- Allow add trades via CSV
- Allow multiple portfolios?
- Add support for exchange rates
- Include edit / add trades in each stock's section
- Add functionality for divdends to be manually entered
- dashboard for each stock to include performance over time incl buys, sells, divs; trade history; current position / p&l; overview position / p&l
- Dashboard for portfolio: change in val over time; overview position / p&l
- allow hiding certain stocks on portfolio + recalculate position
- Automate entering trade data? 
