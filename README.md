#CRM-Analytics-CLTV-Prediction
![image](https://user-images.githubusercontent.com/124357663/224994928-a8ae4b0c-c7ff-495a-89a4-66d8e404f625.png)

Customer lifetime value (Customer Lifetime Value, CLTV) is considered the monetary value that a customer will bring to a company during its relationship and communication with that company. If a company identifies the benefits that its customers can provide in the future, it can streamline its customer relationships and take a more value-added approach. A company that has calculated unit costs for acquiring new customers can compare customer lifetime value calculations with marketing activities aimed at existing customer bases and efforts to find new customers.

# How is customer lifetime value calculated?
 * CLTV = (Customer Value / Churn Rate) * Profit Margin
 * Customer Value = Average Order Value * Purchase Frequency
 * Average Order Value = Total Price / Total Transaction
 * Purchase Frequency = Total Transaction / Total Number of Customers
 * Churn Rate = 1 — Repeat Rate (elde tutma oranı)
 * Repeat Rate = Birden fazla alışveriş yapan müşteri sayısı / tüm müşteriler
 * Profit Margin = Total Price * 0.10
 As a result, when groups are created by dividing from certain points according to the CLTV values to be calculated for each customer, customers will be segmented.
 
# CLTV Prediction
 CLTV prediction is to capture the buying behavior of the whole audience in a data set and to make it possible to predict this when individual characteristics come.
 
 **CLTV = (BG/NBD Model) * (Gamma Gamma Submodel)**
 
 ### BG/NBD (Beta Geometric / Negative Binomial Distribution) ile Expected Number of Transaction
 
 The BG/NBD Model probabilistically models two processes for the Expected Number of Transactio
 
 * **Transaction Process (buy)**
 
      * As long as it is alive, the number of transactions to be performed by a customer in a given time period is distributed with the transaction rate parameter.
      * As long as a customer is alive, they will continue to make random purchases around their transaction rate.
      * Transaction rates vary for each client and are gamma distributed (r,a) for the entire audience. The reception habit of the whole audience is different and               everyone's transaction rate is different. We can make inferences and make probabilistic estimations over a variable and population whose distribution is known.
      
  * **Dropout Process (till you die)**
  
      * Each customer has a dropout rate with probability p.
      * A customer drops with a certain probability after making a purchase.
      * Dropout rates vary for each client and beta is distributed for the entire audience (a,b)
      
 Gamma Gamma Submodel (Conditional Expected Average Profit) allows us to express the average amount of snow as probabilistic.
 
 About the dataset
 The dataset named Online Retail II includes the sales of a UK-based online store between 2010 and 2011. We are evaluating over the sales in the years 2010–2011.
 
 ### Variables
 **Invoice:** Invoice number. The unique number of each transaction, namely the invoice. Aborted operation if it starts with C.

 **StockCode:** Product code. Unique number for each product.

 **Description:** Product name

 **Quantity:** Number of products. It expresses how many of the products on the invoices have been sold.

 **InvoiceDate:** Invoice date and time.

 **UnitPrice:** Product price (in GBP)

 **CustomerID:** Unique customer number

 **Country:** The country where the customer lives.


 
 
      
