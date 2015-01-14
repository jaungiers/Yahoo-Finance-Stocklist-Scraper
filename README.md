# Yahoo Finance Stocklist Scraper

Provided is a Python file for converting a fetched XML file of stocks/industries into a .csv file and mapping each stock to it's country/exchange.

The script requires a *full_stocklist_xml.xml* file to be provided which can be fetched via [This Yahoo Finance Query][1]

[1]: http://query.yahooapis.com/v1/public/yql?q=select%20*%20from%20yahoo.finance.industry%20where%20id%20in%20(select%20industry.id%20from%20yahoo.finance.sectors)&env=store%3A%2F%2Fdatatables.org%2Falltableswithkeys

I have also manually created a JSON mapping file that maps the various exchanges and their host countries to their Yahoo Finance extension as [Detailed Here](http://finance.yahoo.com/exchanges)

The output is a .csv file called *yahoo_stocklist.csv* which has the first row containing the headings: YAHOO TICKER, COMPANY NAME, INDUSTRY, COUNTRY TRADED, EXCHANGE