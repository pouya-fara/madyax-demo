<h1 style="text-align: center;font-size:50px;">Madyax</h1>

<h1>What is Madyax?</h1>
<p>Madyax is a market dynamics analyzer program currently focused on the crypto market. This project, which is built using the Python language and its libraries, is responsible for looking at the financial market at a micro level. It is built to oversee both the spot and the derivative markets and output a micro-level analysis.</p>


<h1>How is it structured?</h1>
<p>Madyax is built on three broad sub-sectors working in parallel: Data Extraction, Data Analysis, and Data Delivery. Depending on the market and the tool being used, however, there are adaptations and modifications applied as well.</p>

<h1>What exactly does it look into and analyze at a micro level?</h1>
<p>Since this project is based on academic and original models, all the programs are tailored to output the evaluation of the models based on actual data. The range of analysis can be categorized into orderbook-focused and non-orderbook-focused. Examples of orderbook-focused analysis are:</p>
<ul>
<li>Flow Analysis</li>
<li>Maker Aggressiveness Analysis</li>
<li>Taker Aggressiveness Analysis</li>
<li>Supply Analysis</li>
<li>Inventory Imbalance Evaluation</li>
</ul>

<p>Examples of non-orderbook analysis are:</p>
<ul>
<li>Premium Index & Funding Rate Analysis</li>
<li>Cross-Exchange Quotation</li>
<li>Spot Borrowing Interest Analysis</li>
</ul>

<h1>How does it operate?</h1>
<p>Due to the high-frequency nature of this environment, this project is built on both multiprocessing and multithreading concepts. The streamer programs are responsible for retrieving the data (either using WebSockets or the REST API) and storing it in memory for the main programs.</p>
<p>If the data lacks critical information, for example, the timestamp of an update, the streamer tries to estimate the timestamp by getting the required data from other APIs.*</p>

<p>While the data is being stored in memory, the main analyzer programs are responsible for fetching, cleaning, aggregating, analyzing, and finally outputting the data.</p>
<p>When the final results are generated, they are stored in a text file. Results that pass certain conditions and thresholds are logged and shown to the user live.**</p>

<p>Finally, after a certain interval, the program cleans old data from the memory, and this cycle continues until the user decides to stop the program.</p>

<h1>What is included in this repository?</h1>
<p>This project has been under development since July 10, 2022, and is still a work in progress. As a result, the full project and all of its code cannot be made public yet. However, to provide a glance at how the logic of the analysis works and the kinds of concepts being implemented, two analysis programs have been chosen to be posted. <br> It is worth mentioning that the programs made public do not cover all the concepts and methodologies considered in building the project. They are not efficient enough on their own to be implemented in this environment, nor should they solely be relied on for a financial decision.</p>

<div style="margin-top:5px;margin-bottom:5px;width:100%;height:2px;background-color:white;"></div>
<em>* Information hiding is usually done by the exchange to reduce the risk exposure of investors while executing large orders, including iceberg orders. This is more prominent in low-liquidity markets, including Binance's spot market.</em>
<br>
<em>** This project is not built to capture immediate mispricings and trade in a high-frequency nature. Rather, the objective of this project is to capture micro-interactions and gather insights from the HFT market. Therefore, for easy access and readability, the final outputs are stored in a .md file instead of a database.</em>