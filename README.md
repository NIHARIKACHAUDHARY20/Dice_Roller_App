<img width="220" alt="appImage" src="https://github.com/NIHARIKACHAUDHARY20/Dice_Roller_App/assets/124075156/a5258244-7331-4733-a822-675056d3a4d5">
Attended the WSR (Weekly Status Review) Meet focused on EC operations:

Reviewed weekly incidents, platform releases, and key operational highlights.

Discussed site alerts, corresponding actions, and resolutions.

Analyzed health parameters of the site with detailed traffic analysis.

Contributed to discussion on Uniqlo India’s payment optimization:

Focus on UPI-related error rate reduction and overall checkout experience improvement.
Weekly Internship Report
Intern: Niharika
Role: Software & Data Intern
Period: 19 May – 23 May 2025
Company: Fast Retailing (Uniqlo Platform Teams)


---

Monday, 19 May 2025

EC SPA/PC Session

Overview of SPA (mobile & desktop) → BFF → downstream PFs

Country-specific bundles served via Akamai (wave 1.5: CA, PH, SG, TH, AU, MY, IN, ID, VN; wave 2.0: JP, US)

Tools & libraries: Preact 8.3.0, Adyen Web SDK, Redux/Redux-Saga, React Router, TypeScript, ESLint, Webpack


Questions to Nisha-san

Git branching: asean-develop (in-progress), asean-staging (tested), v3.x-support (production)

Commit-message format: <ticket-no>–<ticket title>»<brief desc>


EC BFF Platform Session

BFF = API-gateway proxy (Node.js on AWS) between front end & microservices

Responsibilities: performance tuning, API routing, data aggregation, security, error-handling

Wave 1.5 vs 2.0: semantic versioning (V3) vs V4/V5 APIs; single BFF module vs many microservices + BFF-navi reuse




---

Tuesday, 20 May 2025

Basket PF Session

Functionalities:

1. Create/change/return orders


2. Manage cart contents & fetch upstream data


3. Validate & assemble order payload



APIs & Batches: 51 APIs, 4 batch jobs

Tech stack: Java (W1.5→8; W2.0→11), Spring Boot, Spring Batch, SQL, Redis, Docker

Order-splitting: single-order API divides across warehouses; supports delivery-date selection


PAM Access & ServiceNow Ticket

Raised SNOW ticket to provision PAM/PAM-EM accounts (for 18–24 May service requests)




---

Wednesday, 21 May 2025

Inventory PF Session

Part of OMS; manages stock info & bookings across EC-warehouse (real), DC-transit, preorder

Bookings: temporary (“basket”) vs real (core-PF booking + shipment status)

Store pickup (W2.0 only): direct vs ship-from-store


Payment PF Session

W1.5 methods: Credit/Debit Card, Netbanking, UPI, Virtual Bank Transfer, COD, PayPal

W2.0 adds: PayPay, ApplePay, Gift Card, UQPay; PSPs: Cafis Pitt, Toppan, GMO Multi Pay, Adyen, BlueGate

APIs (real-time): authorize, register, retrieve, delete stored cards

Batches: capture, cancel, refund payments


Feature Comparison Table

Compiled Wave 1.5 vs 2.0 features:

Cart tax display & in-store receipt limits

Multi-language support & data-privacy compliance (ASEAN DPA)

Payment methods & environment-variable configurations





---

Thursday, 22 May 2025

OMS Core Session

Order-lifecycle management: creation → shipment → delivery → return

Integration points: Inventory, Payment, WMS, Sales, Coupon, Account

Ordering flows: SPA/PC → Kafka; EC-Admin → direct

Master data: country-specific features (e-invoices, policy constants)


Search PF Session

Components: 1 API endpoint + 3 batch modules, ElasticSearch service

Couplings: Catalog, Price, Review platforms

Wave 2.0 enhancements: typeahead search & dedicated Search Admin UI


Accenture Ops Strategy Meet

Reviewed incident-ticket trends & region-specific stage-3 alerts

Action items: define health-parameter thresholds; improve response during traffic spikes


SCM Team Support

Prepared order-confirmation/completion UI screenshots for Home-Delivery (Wave 1.5)

Documented recommended messaging flows for OPS handoff




---

Friday, 23 May 2025

Catalog PF Session

Data flows:

Importer (upstream SCM/Price/Inventory files, 5-min poll)

Image importer (image-URL ingestion)

Exporters (CIF to downstream PFs & Bazaarvoice → S3)


APIs: Consumer (read-only) vs Admin (write/update)

Terminology hierarchy:

L1: broad classifications

L2: SKU attributes (color/size/pattern)

L3: supply-chain splits; products = L2 combinations



Price PF & Seasons

Price Admin: manage non-item rules (round-up, discount, currency) & execution logic

Price Batches: data store, tax-master, store-master, PLU-master tables


“Thanks-Giving” Sale Analysis Meet

Reviewed real-time traffic & sales across SG, VN, PH, CA, AU

Identified site-failure risks; recommended incorporating pre-sale historical data for trend context




---

End of Report

