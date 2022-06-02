# Investment Analysis

### Project Brief
You work for Spark Funds, an [asset management company](http://www.wallstreetmojo.com/what-is-asset-management-company-amc/). Spark Funds wants to make investments in a few companies. The CEO of Spark Funds wants to understand the global trends in investments so that she can take the investment decisions effectively.

### Business and Data Understanding
Spark Funds has two minor constraints for investments:

1. It wants to invest between 5 to 15 million USD per round of investment
2. It wants to invest only in English-speaking countries because of the ease of communication with the companies it would invest in

- For your analysis, consider a country to be English speaking only if English is one of the official languages in that country
- You may use this list: Click [here](https://en.wikipedia.org/wiki/List_of_territorial_entities_where_English_is_an_official_language) for a list of countries where English is an official language.

These conditions will give you sufficient information for your initial analysis. Before getting to specific questions, let’s understand the problem and the data first.

1. **What is the strategy?**<br>
Spark Funds wants to invest where most other investors are investing. This pattern is often observed among early stage startup investors.
2. **Where did we get the data from?**<br>
We have taken real investment data from crunchbase.com, so the insights you get may be incredibly useful. For this project, I have divided the data into the following files:
You have to use three main data tables for the entire analysis (available for **download on the next page):**
3. **What is Spark Funds’business objective?**<br>
The business objectives and goals of data analysis are pretty straightforward.
    1. **Business objective:** The objective is to identify the best sectors, countries, and a suitable investment type for making investments. The overall strategy is to invest where others are investing, implying that the 'best' sectors and countries are the ones 'where most investors are investing'.
    2. **Goals of data analysis:**  Goals are divided into three sub-goals:
    	  1. **Investment type analysis:** Comparing the typical investment amounts in the venture, seed, angel, private equity etc. so that Spark Funds can choose the type that is best suited for their strategy.
    	  2. **Country analysis:** Identifying the countries which have been the most heavily invested in the past. These will be Spark Funds’ favourites as well.
    	  3. **Sector analysis:** Understanding the distribution of investments across the eight main sectors. (Note that we are interested in the eight **'main sectors'** provided in the mapping file. The two files — **companies and rounds2** — have numerous sub-sector names; hence, you will need to map each sub-sector to its main sector.)


### Structure:

	-- data
	 	-- companies.csv
	 	-- mapping.csv
	 	-- rounds2.csv
	 -- INVEST.pdf
	 -- Investment Analysis.ipynb
	 -- Investments.xlsx
	 

### Detail about datafile(csv)
1. **Company details** <br>
**companies:** A table with basic data of companies.

| Attribute      | Description                                    |
| -------------- | ---------------------------------------------- |
| Permalink      | Unique ID of company                           |
| name           | Company name                                   |
| homepage\_url  | Website URL                                    |
| category\_list | Category/categories to which a company belongs |
| status         | Operational status                             |
| country\_code  | Country Code                                   |
| state\_code    | State                                          |

2. **Funding round details:**  <br>
**rounds2:** The most important parameters are explained below:

| Attributes                 | Description                                           |
| -------------------------- | ----------------------------------------------------- |
|  company\_permalink        | Unique ID of company                                  |
|  funding\_round\_permalink | Unique ID of funding round                            |
|  funding\_round\_type      | Type of funding – venture, angel, private equity etc. |
|  funding\_round\_code      | Round of venture funding (round A, B etc.)            |
|  funded\_at                | Date of funding                                       |
|  raised\_amount\_usd       | Money raised in funding (USD)                         |


3. **Sector Classification:**<br>
**mapping.csv:** This file maps the numerous category names in the companies table (such 3D printing, aerospace, agriculture, etc.) to eight broad sector names. The purpose is to simplify the analysis into eight sector buckets, rather than trying to analyse hundreds of them.
4. **Excel File (Investments.xlsx):**<br>
This file has all the checkpoints, Understanding of the Data Set, and Analysis.
5. **Presentation template (INVEST.pdf):** <br>
This has the finding and explanation of what I have analyzed and the results.

### Conclusions:
1. **Spark Funds** should invest in **venture type companies** because average venture type companies had raised the funding around **5 million USD**. And our constraints for the investment is **5 to 15 million USD.**
2. We should invest in the **USA venture type companies** because the USA carries **75%** of the total raised amount in venture type companies. And **80% in the top ten countries.**
3. Most companies invested in **Others(8243) and Cleantech/Semiconductors(7849)** sectors in the USA.
4. However, if we check the amount raised in USD in both the sectors, we can see **Cleantech/Semiconductors has increased 59%** more than the Others sector.
5. In the Cleantech/Semiconductors sector, we can see **"Freescale Semiconductor"** company has the highest USD amount raised, which is around **13% of the total investment** in the Cleantech/Semiconductors sector, and **77% in top10 Cleantech/Semiconductors** sector in the USA.
