Download Link: https://assignmentchef.com/product/solved-homework-3-a-datareader-application
<br>
5/5 - (6 votes)

This is an individual homework assignment. Compress your complete VB project folder into a .zip file. Upload the .zip file to our homework submission site.

In this assignment, you will implement an electronic stock trading system. Your system will accept trading orders and based on those orders, it will keep track of pending orders, and execute trades when possible.

1. Database design (20 points)

Use Microsoft Access to design a database for the stock trading system. You should determine the tables to be created, the attributes in each table, and the primary key in each table. DO NOT define foreign keys in this assignment even they do exist. It will be easier for you to debug your VB program when foreign keys are absent.

The system maintains common stocks records. Each stock is described by a ticker symbol (e.g., BAC), a company name, exchange venue (e.g., NYSE), listing date, sector, and industry.

The system also keeps track of stocks’ daily closing records. Each closing record consists of a ticker symbol, a date, opening price, highest price of the day, lowest price of the day, the closing price, trading volume on that day, and 1 day price change %.

Users can use the system to place market order requests for stock trading. A market order is a request to purchase or sell a stock at the current market price. Each order request should include a ticker symbol, date and time of the request, type of order (buy or sell), quantity of stock to be traded, and order status (pending, completed, or cancelled).

2. Database population (10 points)

Use Microsoft Access to populate at least 10 records into each of the database tables created above. You must pick at least 10 stocks from this web site: <a href="http://www.1stock1.com/1stock1_112.htm" rel="nofollow">http://www.1stock1.com/1stock1_112.htm</a> , where you can find last year’s return rate % for each stock. For other stock information, please use the Yahoo! Finance (<a href="https://finance.yahoo.com/stock-center/" rel="nofollow">http://finance.yahoo.com/stock-center/</a>) and search by the stock ticker symbol. The sector and industry information can be found from the company profile page on Yahoo! Finance. Please make sure that you have at least 2 sectors and 2 industries per sector, and that each industry has at least 2 stocks.

After you populate the stocks table, you should populate daily records and trading requests based on either true market data or your imagination. Please make sure that you have a mixture of different order types and statuses for different stocks. A minimum of 10 records is required for each table.

3. SimpleBroker v1.0: A DataReader Application (70 points).

MB v1.0 is a DataReader application for placing stocking trading request. You must use aDataReader object to retrieve records from the database and a Command object to update the database. The following describes the components needed for the development.

<ol>

 <li>(1)  User interface: You should design your user interface to support the following functions. Label objects should be used appropriately to make your interface user-friendly. (10 points)</li>

 <li>(2)  Populate the stock ticker ComboBox control: The user should start with a ComboBox control (StocksComboBox) that displays the complete list of stock tickers retrieved from the database. (15 points)</li>

 <li>(3)  Populate the stock closing price ListBox control: After the user selects a stock ticker fromStocksComboBox, a ListBox control (ClosingPricesListBox) should display a list of past closing prices of the selected stock. Each past closing price should indicate both a date and a closing price (e.g., “03/20/2013-$90.23”). The list should be ordered by descending dates. (15 points)</li>

 <li>(4)  Populate a ListBox control: After the user selects a stock ticker from StocksComboBox, another ListBox control (TradingRequestsListBox) will display a list of currently pending stock trading requests for the selected stock. Each request should indicate the order type and stockquantity (e.g., “BUY-2000”). The list is ordered by the order type first and then by quantity. (15 points)</li>

 <li>(5)  Placing a new order request (15 points):

  <ul>

   <li>  The user selects an order type (buy or sell) from another ComboxBox control(TradeTypeComboBox), and enters a stock quantity to be traded in a TextBoxcontrol (QuantityTextBox).</li>

   <li>  By clicking a Button control (SubmitButton), add a new stock request record tothe database.4. Bonus questions (20 points):</li>

  </ul></li>

</ol>

<ol start="6">

 <li>(6)  Sector selection: Another ComboBox control (SectorsComboBox) should be used todisplay all sectors in the database. The user starts with selecting a specific sector fromSectorsComboBox. StocksComboBox will then only display those stock stickers in the selected sector. (10 points)</li>

 <li>(7)  Error handling: Use data validation or exception handling to prevent the following runtime errors from interrupting the program execution:</li>

</ol>

a. Non-numeric values in QuantityTextBox (5 points)

b. OleDbException when populating the ListBox and ComboBox controls.