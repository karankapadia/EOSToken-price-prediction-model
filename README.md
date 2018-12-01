# EOSToken-price-prediction-model

## Data Description:-
Our data files contain two primary groups: EOS token network edge files, and EOS token price files. The Ethereum project is a blockchain platform, and our data comes from there.
Although Ethereum started in 2015, most tokens have been created since 2016. As such, tokens have different starting dates, and their data starts from that initial date.

Token edge files have this row structure: fromNodeID\ttoNodeID\tunixTime\ttokenAmount\r\n

This row implies that fromNodeID sold tokenAmount of the token to toNodeID at time unixTime. fromNodeID and toNodeID are people who invest in the token in real life; 
each investor can also use multiple addresses. Two addresses can sell/buy tokens multiple times with multiple amounts. For this reason, the network is considered a weighted, 
directed multi(edge) graph. 

There are two things; first, EOS token has a limited supply (i.e., token count, which can be found on coinmarketcap.com as circulating amount). Then EOS have 10^18 sub-units.
This is similar to dollar in the US. There are around 18 trillion dollars in the economy, and each dollar is divided into 100 cents (subunits). Similarly, there is a token supply, 
and then there is a subunit for each token. This idea comes from Bitcoin where subunits are called Satoshis, 1 Bitcoin =10^8 satoshis. Coin market cap gives the total supply, but not sub-units, 
which differ from token to token. Some tokens have 10^18 sub-units. That means there can be numbers as big as totalAmount∗10^18.

Etherscan.io gives these sub-units as decimals, For EOS: It has 18 decimals, which means each EOS token has 10^18 subunits. https://etherscan.io/token/0x86fa049857e0209aa7d9e616f7eb3b3b78ecfdb0

Price files have no extensions, but they are text based. If you open them with a text editor (use notepad++ or similar), you will see this row structure: Date\tOpen\tHigh\tLow\tClose\tVolume\tMarketCap\r

The price data is taken from https://coinmarketcap.com/. Open and close are the prices of the specific token at the given date. Volume and MarketCap give total bought/sold tokens and market valuation at the date.

## How to run code:-
There are two files uploaded on the repository i.e .html file and .rmd file.
First of all, to run an .rmd file, we need to have RStudio in the system. If not, you can download RStudio from https://www.rstudio.com/products/rstudio/download/.
After downloading RStudio, open the .rmd file using RStudio. It is an R markdown file, so after you can easily knit the .rmd file to html file.

