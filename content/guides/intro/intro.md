---
title: Platform Overview
category: 6272f14d2c9adf004c1bbab9
---

# A Synctera Platform Overview for FinTechs

You’re a developer about to integrate the Synctera platform with your application. Before you start, what is the Synctera platform anyway? What does it offer, and how do you work with it?

## The Synctera Platform in a Nutshell

The Synctera platform is a comprehensive set of cloud-based financial services that brings three types of businesses together:

- **FinTechs** that provide unique financial services to their customers
- **Sponsor banks** that provide the necessary legal framework and financial resources to FinTechs to carry out FinTech business
- **Service vendors** that team up with Synctera to provide fundamental financial services to FinTechs and sponsor banks.

<img src="/images/graphPlatformOverview.svg" alt="The basic architecture of the Synctera platform." />

Synctera provides a unified platform that manages interactions between FinTechs and sponsor banks. It consolidates a variety of essential services such as accounts and ledger, card issuance and management, money movement, and risk management under central control through a family of APIs and the Synctera Dashboard.

### FinTechs and Sponsor Banks

The first step in a FinTech’s relationship with Synctera is onboarding to Synctera. During the onboarding process, Synctera helps determine the banking resources the FinTech requires, find a sponsor bank that can provide those resources, and works to establish a business relationship between both parties.

Once a FinTech has connected with a sponsor bank, the Synctera platform provides services that help the FinTech and sponsor bank communicate essential information to each other as they carry out business together. The FinTech can, for example, reconcile the transactions its customers carry out with the customers’ accounts held by the sponsor bank so that the FinTech and the bank’s records agree. Or the FinTech can communicate actions it takes to ensure compliance with banking laws so the sponsor bank knows that their mutual business doesn’t risk breaking those laws.

### Synctera Services

In addition to the connection between a sponsor bank and a Fintech, the Synctera platform services are implemented and provided by Synctera and our vendor partners. Synctera’s native services include setting up customers and accounts, reconciling FinTech transactions with a sponsor bank, reporting compliance activities, and so on.

Synctera depends on vendor partners to provide more specialized services that include creating debit cards, performing know-your-customer (KYC) checks on potential customers before signup, performing debit card transactions, and more. These vendor services are all available through the Synctera platform without requiring external setup, contract negotiation, or connections.

### Synctera Products

To use Synctera services, a FinTech subscribes to one or more Synctera products via the sponsor bank. Each product provides access to services that address a particular business case.

FinTechs can pick and choose products to fit their requirements. A FinTech that carries out its own KYC may, for example, opt not to use Synctera KYC products, but may decide to use Synctera ledger and card products to issue and manage debit cards.

Synctera offers products that provide, among other things:

- Basic financial services such as ledger and customer views
- Card services such as debit card issuance and processing
- Money movement services such as ACH transactions and mobile Remote Deposit Capture (mRDC)
- Risk services such as KYC, Document Verification, and Transaction Fraud monitoring

## Platform Interfaces

The Synctera Platform provides two main interfaces to a FinTech:

- The [Synctera APIs](/reference) for direct application access to the platform
- The Synctera dashboard for human access to the platform

Use the Synctera APIs to integrate Synctera services with your applications, then use the Synctera dashboard for executives, administrators, operators, and your customer care staff to work with those services. The dashboard lets you oversee and gain insights into your business.

### Synctera APIs

The Synctera APIs are RESTful APIs. They include a set of basic service APIs:

- The [**Customers API**](/reference#customers), which creates and manages records for many types of customers that include information about customer employment and risk ratings.
- The [**Accounts API**](/reference#accounts), which creates and manages customer accounts and relationships between customers and accounts.
- The [**Reconciliations API**](/reference#reconciliations), which handles account reconciliation between a FinTech and its sponsor bank.

A set of risk management APIs:

- The [**KYC Verification API**](/reference#kycverification), which can create and manage documentation for a customer and run verification checks through a vendor service to ensure that a customer is valid.
- The [**Disclosures API**](/reference#disclosures), which handles legally required disclosures to customers.
- The [**Watchlist API**](/reference#watchlist), which subscribes customers to security watchlists and handles watchlist alerts.

A set of money movement APIs:

- The [**Transactions API**](/reference#transactions), which creates, manages, and lists Automated Clearing House (ACH) transfers between internal and external accounts.
- The **mRDC Deposits API**, which handles remote deposit capture (RDC) transactions, including working with the captured images for deposits.

A set of card management APIs:

- The [**Cards API**](/reference#cards), which issues, activates, and manages cards for customers.
- The [**Card Transaction Simulations API**](/reference#cardtransactionsimulations), only available in the sandbox, which simulates various card transactions so you can generate transaction events to test your application features such as customer alerts and balance updates (if your application provides the account ledger).

<!--
And a utility API:

- The **Webhooks API**, which sets up and manages event monitoring for different Synctera services.
-->

Access to these APIs in production depends on the Synctera products to which you’re subscribed.

### The Synctera Dashboard

The Synctera dashboard is a browser-based user interface that humans in both a FinTech and its sponsor bank can use to work with integrated Synctera features. The dashboard has three views:

- The **platform view** provides displays and controls that allow operators such as customer service staff to handle actions like updating customer information, viewing customer risk assessments, requesting card reissuance, and so on.
- The **administrator view** provides displays and controls that FinTech and sponsor bank administrators can use to set up and manage operators and to manage Synctera service operations. Developers can also use the admin page to manage their API integration and API keys, review error logs, check API performance, manage webhooks, and so on.

## Development and Deployment

Synctera provides two environments for successful integration:

- The **Synctera sandbox** provides a place to test integration without real world consequences. It offers full access to all Synctera APIs where requests are fulfilled without incurring expenses for underlying vendor services or communications with outside entities such as the sponsor bank. It connects to underlying vendor sandboxes to test services involving their services.
- The **production environment** where a successfully tested integration moves to conduct business with the real world with real financial and legal consequences.

We also provide an SDK, full API documentation, and developer support through our Synctera Community Slack account that you can join at [https://launchpass.com/synctera-community](https://launchpass.com/synctera-community).

## Getting Started

It’s easy to give our platform a try. [Sign up for a Synctera account](https://app.synctera.com) and learn how to play in our sandbox.
