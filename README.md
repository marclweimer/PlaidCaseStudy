# Plaid - A Case Study on Open Banking
## Overview and Origin
Much can be said about the growth and excitement of the burgeoning FinTech space.  Many of these companies are innovative, unencumbered by the old infrastructure or business models of existing financial institutions.  Data takes the center stage at these companies as they use it provide new insights or streamline old processes.  To access this data, FinTech companies typically need to tap into existing banks.  

This need to connect old and new platforms means there must be a willingness and ability for FinTech and incumbent financial institution platforms to interact.  Without a seamless interface between the two, new companies would not be able to capture market share and incumbent companies risk migration of customers to banks that are more open. In the early days of FinTech, no basic infrastructure for startups and banks to easily integrate existed.

Enter Plaid.  Founders Zach Perret and William Hockey knew how difficult it was for new FinTech companies to integrate their innovative ideas into a spider web of bank systems. Zach and William their strategy off the difficulty they faced in prior consumer finance application development.  Their focus for Plaid is standardizing API connectivity, allowing other FinTech's to more easily harness the power of existing Financial infrastructure.

Since Plaid's founding in 2012, it has raised $300mm of capital from venture capital titans and entrenched global financial institutions alike.  More importantly, Plaid has established working relationships with FinTech's *and* banks alike -- claiming name brand participants from Venmo to Bank of America.

## Business Activities:

Consumer banks have for a long time been the center of consumer financial life.  Banks competed with other banks to provide a full suite of services for their consumer.  This meant that the checking account was a consumer's home base or *financial hub*.  Paychecks are deposited, payments are paid via check, ACH or card all from the same institution.  Maybe a consumer would shop around for an auto loan or mortgage, but the checking account at their main bank would be drafted each month for payment.

Today, the checking account continues to be the financial hub of most consumers.  The difference, however, is that an increasing array of non-bank technology companies are targeting these consumers in new ways; for example, they are providing alternative means to send money to friends - e.g. Venmo - or creative peer-to-peer lending schemes - e.g. Lending Club.

However, FinTech like this looking to move money, get access to financial history or a portfolio all must at some point interact with this financial hub. As the consumer signs up with a FinTech provider, that provider must then ask the consumer to integrate with their financial hub - the checking account.  The FinTech provider may be looking to validate a consumer's identity, evaluate and score lending suitability, or simply verify payment detail for the movement of funds back and forth between their application and the consumer's financial hub.  Thus, as non-bank businesses market new financial products to consumers, they need to provide a frictionless integration process, connecting their app to a consumer bank account.  If not, a consumer may not make it through the onboarding process due to lack of convenience.

While a FinTech company would like to have easy access to bank data, banks have traditionally taken the approach that unfettered access to their consumer data is risky.  They argue, most of the time for legitimate reasons, that cybersecurity and consumer privacy expectations require them to monitor and restrict third-party access to consumer bank data.

Plaid's creative positioning sits squarely in this area of natural tension - between a bank's need to protect data access and a FinTech's desire to create a seamless consumer onboarding experience.  Plaid first focused on creating standard APIs for FinTech development, while working with the banking industry to alleviate concerns of unapproved access to data.  The result is a company that facilitates the movement of data in a controlled and secure fashion between two companies with a mutual consumer.

Most consumers are completely unaware they are interacting with Plaid.  The technology seamlessly fits into the flow of popular apps such as Robinhood and Coinbase, which are examples of platforms Plaid claims in their customer base.  You can think of Plaid as a process integrator, like the new highway of the consumer banking world that had previously been dominated by proprietary messaging networks like SWIFT.  
Plaid puts the types of data it aggregates into buckets of products, which it then sells to FinTech providers as data flows onto which they can build products.  These "products" are summarized from Plaid's website below:
* Transactions - The /transactions/get endpoint allows developers to receive user-authorized transaction data for credit and depository-type Accounts. Transaction data is standardized across financial institutions, and in many cases, transactions are linked to a clean name, entity type, location, and category. Similarly, account data is standardized and returned with a clean name, number, balance, and other meta information where available.
* Auth - Plaid offers 4 authentication paths for a user to successfully verify their Auth numbers, where a user enters their credentials and can either be authenticated immediately or using a live "penny test" transaction and monitoring.
* Balance - returns the real-time balance for each of an Item's accounts. It can be used for existing Items that were added via any of Plaid’s other products.
* Identity - allows you to retrieve various account holder information on file with the financial institution, including names, emails, phone numbers, and addresses.
* Investments - allows developers to retrieve user-authorized Holding, Security, and Investment transactions data for a wide array of investment account and security types. Both Investments endpoints are only compatible with Items having Accounts of type investment.
* Assets - allow you to retrieve point-in-time snapshots of an Item or set of Items, including account balances, historical transactions, and account holder identity information, which we call Asset Reports.
* Liabilities - returns various details about an Item with loan accounts. Today, the only supported Account subtype is a student loan (student). The types of information returned by Liabilities can include:
    * Balances: how much is owed and over what pay period
    * Payment timing: last payment date and next payment due date
    * Current loan terms: interest rate, maturity, limits
    * Account details: original loan amount, guarantor, and more
* Income - allows you to retrieve information pertaining to an item’s income. In addition to the annual income, detailed information will be provided for each contributing income stream (or job). Details on each of these fields can be found below.

The technology behind Plaid's system is simple:
1. APIs - leveraged when connecting seamless interfaces in FinTech apps and process flows.  Also, where possible, they may use APIs to connect right through the front door to a bank.
2. Data Scraping - this is using a machine program to crawl through, collect and understand/categorize data that is on a web portal meant for human consumption.  This process at Plaid is fundamental to collect data from a financial institution when a secure API channel is not possible.  Some industry estimates put the amount of total traffic on bank websites due to data scraping for website like Mint.com as high as 40-70%.  This technology can use multiple tools, such as:
    * Screen scraping - a bank's website may be more easily understood or accessible only in visual format, and the program will use a picture and OCR, *optical character recognition*, technology to lift the words off the picture.
    * Web scraping / crawling - the use of an algorithm going through the HMTL of the website to collect and correctly categorize data.
    * Natural Language Recognition - Plaid claims to have the ability to accurately access thousands of bank websites.  This would be extremely hard to do by having a someone code to the individual setup of each website.  Plaid would use natural language recognition as a way for its program to automatically associate tables of data correctly.
3. Database tools (MySQL, Mango DB)
4. Java tools (React, TypeScript)- as a company that both integrates into online platforms of its clients and collects data from bank websites, Plaid uses these tools to manage their platform.
5. Python with various data analysis and visualization tools - Plaid is launching new avenues for revenue, moving away from being a simple data aggregator to a data analyzer.

Plaid does the heavy lifting for both the banks and the Plaid FinTech customers: they make sure as many banks as possible are accessible on their "network", creating a simple and single point of entry for the consumer.  The result is a successful company. For 2017, Forbes estimated Plaid booked $40mm of revenue.  

## Results and Landscape

Plaid is not the only company providing data aggregation services to FinTech, and, interestingly, it was not the first.  A major competitor is Yodlee, which predated Plaid *over a decade*.  In addition, a more established financial technology company - Intuit, which owns Mint.com and Quicken Loans - provided and consumed these services for years before discontinuing the service in 2016.  There are a handful of other players in this space, and the list gets wider when you look internationally.

Plaid does not release financials or comment publicly on financial returns; however, the company does have some metrics it references to measure success.  For example, user growth reached new heights in 2018, with 1 in 4 US consumers interacting with Plaid's technology in the last year.  Plaid has also done the work to successfully integrate into 10,000 banks in the USA (and now Canada) - key for a company that want to act as the central plumbing for FinTech companies.

For comparison, Yodlee likes to claim it works with over 1,100 companies and has 23 million users.  Plaid, by its own account, dwarfs those numbers.  One interesting statistic does stick out for Yodlee; they claim that over 60% of their data is aggregated through established, structured data feeds.  This means they have established and working data feeds with financial institutions instead of having to rely on screen/data scraping techniques to retrieve data.  This is a data point that I, frankly, could not find for Plaid's platform.

Plaid may rely very heavily on screen scraping, which is a risk to its business.  In 2018, Plaid and Capital One had a very public fight after Capital One decided to improve data security measures and limit certain data aggregators ability to function for users on the Capital One network.  Plaid launched a public relations campaign to try to shame Capital One into opening its infrastructure up again; however, other major data aggregators did *not* have a problem accessing Capital One client data.  This tells us that Plaid is doing something different, likely screen scraping after impersonating a user login via robotics automation, that is less secure.

Even as events like the Capital One spat become more common, its apparent that companies like Plaid have completely changed the environment for consumer banking.  It has forced major banks to consider and implement their own API strategy, at the risk of being disintermediated by FinTech providers accessing their data and providing more value-added services.  Add the fact that regulation in multiple countries is forcing banks to open themselves up to FinTech integration, and the market quickly seems to shift to a more open environment for FinTech providers.  Additionally, consumers are increasingly comfortable with sharing data to third parties.

![](https://assets.sourcemedia.com/dims4/default/b0a840f/2147483647/resize/680x%3E/quality/90/?url=http%3A%2F%2Fsource-media-brightspot.s3.amazonaws.com%2Fcb%2Fd8%2F9ab9a6de4c948784c380950dc95d%2Fab-data-1.png)

This does not mean that banks are on their way out.  Instead, Plaid itself has a white paper with studies showing that over 80% of consumers preferred their bank to help them securely manage third party app access. 

## Recommendations

There are two areas that Plaid should consider exploring.  Namely, as finance goes global, the company needs to expand its capabilities to more countries.  Access to capital, investments and even simple bank account management is now global.

Additionally, I think there is a large untapped market in the corporate sector.  While there are sophisticated mechanisms in place to securely pass data between a corporation and its banking establishment, the process on integration and servicing is extremely clunky and rife for improvement.  The rise of SaaS financial technology, like Treasury Workstations and even entire ERPs built in the cloud, increases the likelihood that data aggregation can be a successful venture and delighter for companies *and* banks alike.

Both opportunities for expansion may prove costly, with regulatory and client expectations differing greatly from their core competency.  However, as the world gets smaller and technology continues to enable more convenient options for data transfer, Plaid is in a good position to meet the challenges.

## References


* Accenture. (2019, July). THE FUTURE OF FINTECH AND BANKING: DIGITALLY DISRUPTED OR REIMAGINED? Retrieved from Accenture: https://www.accenture.com/us-en/insight-future-fintech-banking
* DiCamillo, N. (2018, July 17). In data dispute with Capital One, Plaid stands alone. Retrieved from American Banker: https://www.americanbanker.com/news/in-data-dispute-with-capital-one-plaid-stands-alone
* Konrad, A. (2018, December 11). Fintech Startup Plaid Is Now Valued At $2.65 Billion After $250 Million Raise. Retrieved from Forbes: https://www.forbes.com/sites/alexkonrad/2018/12/11/mary-meekers-first-post-kleiner-deal-fintech-startup-plaid-now-valued-at-265-billion/#2545290677d6
* Laura Brodsky, C. I. (2018, August). Open banking’s next wave: Perspectives from three fintech CEOs. Retrieved from McKinsey: https://www.mckinsey.com/industries/financial-services/our-insights/open-bankings-next-wave-perspectives-from-three-fintech-ceos
* Plaid LLC. (2019, August). Plaid. Retrieved from Plaid: https://plaid.com/
* StackShare, Inc. (2019, August). Plaid Stack. Retrieved from Stackshare: https://stackshare.io/plaid/plaid
