# Web3-Wallet-API-Audit-Automation
Using python and API to audit transaction records on Web3 wallets

I’ve been diving into quant trading, particularly in digital currency. After speaking with industry professionals — especially in investment operations — I noticed a key challenge:

Manual reconciliation is tedious and error-prone. Especially for small funds, traders manually log their transactions, often across multiple funds, assets, custodians, wallets, and accounts. This makes auditing slow, complex, and COSTLY.

I wanted to make this project to automate with the reconciliation process. What i envision for the end product is that it will automatically retrieve trading data, compare to internal records in the system (e.g. manual entries), and flag discreptancies. Ultimately, this will make the the eventual auditing process a lot smoother.


### How this minimum viable product (MVP) works:
- API Data Integration – Use Python + BscScan API to pull blockchain transaction data.
- Error Detection – Compare API data with manual entries (csv files) using Pandas.
- Automated Reporting – Flag discrepancies and generate alerts for reconciliation.



### Next Steps & Improvements:
- Support multiple addresses and APIs.
- Enable unit conversions for multi-coin support.
- Expand error checks beyond manual entry mismatches to include timestamps, sender/receiver addresses, and transaction hashes.
- Implement secure API key storage (e.g., environment variables).
- Refine manual entry formats for consistency.
Long-Term – Integrate with blockchain-based fund tracking, and ML for anomaly detection and reporting insights.


I think this can help: crypto traders track transactions accurately, fund accountants streamline reporting, auditors speed up verification, and financial institutions manage digital assets with greater transparency and compliance. 



# Here's my simple tool, as of Feb 9, 2025. 
Assuming we have this wallet, that manages a multichain porfolio. It's pretty big $2B.

And say that this is our internal records of our transactions, for traders A-J, there's an error in reported transaction value for traderH

I got the transaction history using a Python script. That spaces out the AP requests so that we are not kicked off the server, and will print errors if the extraction is unsuccessful. 

Using a Python API script, we successfully fetched 241 transactions, and we save it into csv file:

Python code to save API data into csv 

Now, we load the manual entry transaction data. 

And then we use pandas merge & valuematch to check for discrepancies. 

the merged results
And we successfully discovered the discrepancy. We can update it we choose. 

we found a discrepancy! and if we choose, we can update it. 

link to LinkedIn Article: https://www.linkedin.com/pulse/project-automating-crypto-wallet-audit-python-apis-siru-lin-nrrmc/?trackingId=4qWXB0UyjeHREm1zQwukiw%3D%3D
