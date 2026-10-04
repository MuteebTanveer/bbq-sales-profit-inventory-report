# bbq-sales-profit-inventory-report
Power BI report tracking daily sales, expenses, profit, cash flow and stock for a small BBQ business. Data entry in Google Sheets with Apps Script.

A Power BI report for a small BBQ food business. It shows daily sales, expenses, profit, cash flow and how much stock is left. The data is entered in Google Sheets and Power BI reads it from there.

## Why I made this

The business was tracking sales on paper, so it was hard to know the real profit or how much stock was left. I made a Google sheet for daily entry and a report on top of it.

## Tools used

- Google Sheets and Apps Script for data entry
- Power BI for the data model, DAX measures and visuals
- Power Query for loading the data

## How it works

The Google Sheet has these sheets: Items List, Items Entry, Cost, Inventory, Expense, Bags, Payment Paid, Roti_Pani, Bottles and Labour.

When an item is picked in Items Entry, an Apps Script saves its cost, price and weight in that row. If a rate changes later, old rows keep their old values, so past profit does not change.

Stock purchases (meat, naan) go in Inventory. (Bottles) go in Bottles. Expense is for running costs( Koila, Dahi, etc) and cost of  inventory used and labour.
Payment Paid is for how much we paid the vendor about our purchase
Bottles are getting bought on cash so thatswhy in seperate sheet 

Each sheet is published as a CSV link and loaded into Power BI. A separate date table made ant then connected to the sales and expense tables.

## Main measures

- Total Sale
- Total Expense
- Cost Total
- Profit = Total Sale - Total Expense - Cost Total
- Total Bought Kg, Total Sold Kg and Total Item Left

## What the report shows

- Daily sales, expense and profit
- Cash flow
- Money tied up in stock
- Stock left in kg for each item
- Most Selling items
- Sale vs cost comparison of each item
- Overall Sale trend 

## What I learned

- Built a data model in Power BI with a separate date table linked to the sales and expense tables, so every report can be filtered by      day, week or month.
- Wrote DAX measures for profit, total sales, expenses and stock left in kg, and checked them against the Google Sheet to make sure the     numbers matched.
- Solved a real problem: when item prices changed, old sales rows changed too and past profit became wrong. I fixed it with an Apps         Script that saves the price, weight and cost in the row at the time of entry, so history stays correct.
- Separated stock purchases from running costs, so profit is not mixed up with money spent on inventory.
- Worked with a real business, which meant the data was messy and the requirements changed along the way.

## Files

- `report.pdf` is a PDF export of the Power BI report
- `Screenshot.png` is a screenshots

## Data privacy

The Power BI file and the Google Sheet are not shared in this repository. The data belongs to a real business and the owner did not agree to make it public, so I am only sharing the report as a PDF. All figures in the PDF are from the real business, and nothing here can be used to identify customers and business.
