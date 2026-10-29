# Awesome-Buy-Now-Pay-Later-BNPL

# Awesome-Buy-Now-Pay-Later-BNPL
**Top Buy Now Pay Later BNPL (Opensource) 🌟 Star if you like it! 🌟**

**Curated List of SaaS Products & Open-Source GitHub Projects**
*Focused on Installment Payments, Merchant Integration, Credit Decisioning & Consumer Checkout Financing*
**Last updated: October 2026**

This repository tracks notable **SaaS platforms** and **open-source projects** for **Buy Now, Pay Later (BNPL)**. These tools enable merchants to offer installment financing at checkout and enable consumers to split purchases into scheduled payments—from fully managed BNPL networks with underwriting, fraud detection, and merchant settlement to self-hosted lending engines and payment orchestration layers that give organizations control over installment logic and credit workflows.

**Examples** include Klarna, Afterpay, Affirm, Zip, Sezzle, PayPal Pay in 4, Shop Pay Installments, Splitit, Sunbit, and Zilch (the category leaders in commercial space).

**Open-source emphasis**: This section is expanded with every relevant project for self-hosting, installment lending, and open payment infrastructure. **Critical note**: True open-source BNPL—a consumer-facing installment network with underwriting, regulatory compliance, and merchant settlement—does not exist. Open-source projects provide **lending infrastructure** (loan management, installment calculation) or **payment orchestration** (routing BNPL as a payment method), not a turnkey BNPL product.

Contributions welcome! Open a PR to add/update entries. Keep descriptions factual and link to official sites.

## Table of Contents
- [SaaS/Hosted Platforms](#saas-hosted-platforms)
- [Open-Source GitHub Projects](#open-source-github-projects)
- [How to Contribute](#how-to-contribute)
- [Disclaimer](#disclaimer)

## SaaS/Hosted Platforms

- **[Klarna](https://www.klarna.com/)**
  **Global BNPL network** with Pay in 4, Pay in 30 days, and financing options. **Pricing**: Merchant fees per transaction; consumer late fees vary by market. **Free tier**: None for merchants. **Best for**: merchants wanting broad global reach and a mature BNPL brand at checkout.

- **[Afterpay](https://www.afterpay.com/)** (Block)
  **BNPL platform** with Pay in 4 installments, popular in retail and fashion. **Pricing**: Merchant fees per transaction. **Free tier**: None. **Best for**: retailers targeting younger demographics with a well-recognized installment brand.

- **[Affirm](https://www.affirm.com/)**
  **BNPL and installment lending** platform with longer-term financing options and transparent terms. **Pricing**: Merchant fees; consumer interest on longer plans varies. **Free tier**: None. **Best for**: merchants wanting flexible financing options beyond short-term splits.

- **[Zip (Quadpay)](https://zip.co/)**
  **BNPL platform** with Pay in 4 and installment options across multiple markets. **Pricing**: Merchant fees. **Free tier**: None. **Best for**: merchants wanting a widely recognized BNPL option with global coverage.

- **[Sezzle](https://sezzle.com/)**
  **BNPL platform** focused on Pay in 4 with a consumer app and merchant network. **Pricing**: Merchant fees. **Free tier**: None. **Best for**: merchants wanting a BNPL option with strong consumer engagement features.

- **[PayPal Pay in 4](https://www.paypal.com/)**
  **PayPal's BNPL offering** allowing eligible customers to split purchases into four payments. **Pricing**: Merchant fees; eligibility determined by PayPal. **Free tier**: None for merchants. **Best for**: merchants already on PayPal wanting a native BNPL option without additional integration.

- **[Shop Pay Installments](https://shop.app/)**
  **Shopify's BNPL** powered by Affirm, available to eligible Shopify merchants. **Pricing**: Merchant fees; eligibility requirements apply. **Free tier**: None. **Best for**: Shopify merchants wanting an integrated installment option without a separate BNPL integration.

- **[Splitit](https://www.splitit.com/)**
  **Installment payment platform** using existing consumer credit cards, without new credit applications. **Pricing**: Merchant fees. **Free tier**: None. **Best for**: merchants wanting installment options without consumer credit checks or new accounts.

- **[Sunbit](https://sunbit.com/)**
  **BNPL platform** focused on in-person and point-of-sale financing for services and retail. **Pricing**: Merchant fees. **Free tier**: None. **Best for**: service providers and retailers wanting in-person installment financing.

- **[Zilch](https://www.zilch.com/)**
  **BNPL and rewards platform** with a focus on responsible lending and consumer rewards. **Pricing**: Merchant fees. **Free tier**: None. **Best for**: merchants in the UK and Europe wanting a BNPL option with consumer rewards integration.

## Open-Source GitHub Projects

- **[Hyperswitch](https://github.com/juspay/hyperswitch)**
  **Open-source payment orchestration platform** (Apache 2.0 for core) — **the most significant open-source infrastructure relevant to BNPL**, though it is not a BNPL product itself. **Features**: Unified SDK supporting **cards, wallets, BNPL, bank transfers**, and more across 100+ payment processors; intelligent routing and retry logic; Control Center for managing payment workflows; supports authorization, capture, void, refund, and chargeback handling . **Tech stack**: Rust (backend), TypeScript/React (SDK/web). **Deploy**: Self-hosted (Docker Compose, AWS CDK, Helm) or Hyperswitch Cloud. **Trade-off**: **Orchestration layer, not a BNPL lender**—it routes transactions to BNPL providers (Klarna, Affirm, etc.) but does not provide underwriting, installment plans, or consumer credit. **Best for**: merchants wanting to offer BNPL alongside other payment methods through a single integration, with control over routing and retries.

- **[Frappe Lending](https://github.com/mhakooma/lending)**
  **Open-source loan management system** (license per repo) — **the most complete open-source lending engine** applicable to installment financing. **Features**: Loan product configuration with customizable terms, interest rates, and repayment options; full lifecycle from application to disbursement and repayment; collateral tracking; automated accounting entries; billing and interest calculations; risk and compliance reporting; co-lending support . **Tech stack**: Python (Frappe Framework), ERPNext. **Deploy**: Self-hosted (Frappe Bench + ERPNext). **Trade-off**: **General loan management, not a BNPL checkout product**—no merchant integration, no checkout SDK, no real-time credit decisioning. It manages loans after they are originated. **Best for**: lenders and fintechs wanting a proven open-source engine to manage installment loans and repayment schedules.

- **[RPB Lending](https://github.com/info-rbp/rpb-lending)**
  **Frappe-based loan origination and servicing application** (license per repo) — **a production-hardening loan management system** with active development. **Features**: Loan products, pricing, and repayment schedules; loan leads and applications; disbursement, repayment, and interest accrual; collateral management; delinquency and classification processing; accounting-linked operations through ERPNext. The project is undergoing hardening for validation, permissions, and regression coverage . **Tech stack**: Python (Frappe/ERPNext). **Deploy**: Self-hosted (Frappe Bench + ERPNext). **Trade-off**: **Loan servicing infrastructure**, not a BNPL checkout solution—same limitations as Frappe Lending. **Best for**: institutions wanting a loan management system with active maintenance and a modernization roadmap.

- **[bnpl_system](https://github.com/p4prathamesh/bnpl_system)**
  **Educational BNPL system implementation** (license per repo) — **a simple Flask-based reference for BNPL mechanics**. **Features**: User registration with credit limits; purchase recording with full payment or EMI repayment types; repayment plan tracking; late payment penalties; reporting endpoints for outstanding balances and repayment history . **Tech stack**: Python (Flask), MySQL. **Deploy**: Self-hosted (Flask dev server). **Trade-off**: **Educational/demo project**—no production hardening, no merchant integration, no payment processing, no real credit decisioning. **Best for**: developers learning BNPL data models and basic installment logic.

- **[InstallmentPay](https://github.com/JamshedJ/InstallmentPay)**
  **Installment payment service example** (Go, license per repo) — **a narrow implementation of installment calculation for a specific merchant scenario**. **Features**: Product-category-based installment duration rules (smartphone 3–9 months, computer 3–12, TV 3–18); percentage markup per additional installment period; SMS notification with purchase details; `/calculate` endpoint for total payment calculation . **Tech stack**: Go (Gin, Zerolog). **Deploy**: Self-hosted (`go run cmd/main.go`). **Trade-off**: **Narrow scope**—single merchant use case, no credit assessment, no payment processing, no recurring billing. **Best for**: developers wanting a reference for installment pricing logic with category-based rules.

- **[T_Cred](https://github.com/Tameem2004/T_Cred)**
  **BNPL service concept with Web3 integration** (license per repo) — **an early-stage project exploring blockchain-based BNPL**. **Features**: Purchase splitting into installments; smart contract integration (Web3) for payment logic. **Tech stack**: Web3, JavaScript. **Deploy**: Self-hosted. **Trade-off**: **Extremely early-stage** (last commit March 2025), minimal documentation, no production validation, no traditional payment rails. **Best for**: developers exploring Web3/blockchain approaches to BNPL—not for production use.

- **[django-react-iou-bnpl](https://github.com/mojtaba-arvin/django-react-iou-bnpl)**
  **Full-stack BNPL system with I.O.U-based installment model** (license per repo) — **a Django/React implementation with merchant-assigned plans**. **Features**: Private/Assigned Plan model where merchants assign installment plans to customers; separate admin panels for customers and merchants; account-type-restricted access; micro-frontend architecture (TypeScript). **Tech stack**: Python (Django), React.js, TypeScript. **Deploy**: Self-hosted. **Trade-off**: **Early-stage with 0 stars**—no community validation, no payment processing, no credit underwriting. **Best for**: developers wanting a full-stack reference for merchant-assigned installment plan workflows.

### Additional Strong Open-Source Options

- **MONEI for Saleor** — Payment app supporting card installments via MONEI Flex for Spanish customers (license per repo). **Note**: **Regional installment feature** within a payment gateway integration—not a BNPL platform. Split card payments into monthly installments for eligible customers . **Best for**: Saleor merchants in Spain wanting installment options through MONEI.
- **POSNext** — Open-source POS with customer credit and partial payment support (license per repo). **Note**: **Retail POS with credit sales**, not BNPL—supports paying with customer credit and partial payments but no installment plans or credit decisioning . **Best for**: retailers wanting POS with customer credit tracking.

**Frameworks for building custom systems**: Combine **Hyperswitch** as the payment orchestration layer for routing transactions to BNPL providers with **Frappe Lending** or **RPB Lending** as the loan management backend for installment plans, and **bnpl_system** or **InstallmentPay** as references for installment calculation logic—creating a BNPL infrastructure stack. **None of these provide a turnkey BNPL product**—merchant onboarding, credit underwriting, regulatory compliance, and consumer checkout UI must be built or sourced separately.

## How to Contribute

1. Fork the repo.
2. Add/edit entries in `README.md` (follow existing format).
3. Include: name, link, 1–2 sentence description, license (for open-source), and whether it's SaaS or open-source.
4. Submit PR with a short explanation.

Star the repo if you find it useful!

## Disclaimer

- This is a **community-curated** list — not exhaustive and not an endorsement.
- BNPL platforms handling consumer credit and payment data must comply with financial regulations (consumer lending laws, truth-in-lending disclosures, KYC/AML, PCI DSS) and data protection regulations (GDPR, CCPA, etc.).
- **The "BNPL network" vs. "lending infrastructure" vs. "payment orchestration" distinction is absolute.** **Klarna, Afterpay, Affirm, Zip, Sezzle, PayPal Pay in 4, Shop Pay Installments, Splitit, Sunbit, and Zilch** are **BNPL networks**—they provide consumer credit, merchant settlement, and checkout integration. **Frappe Lending and RPB Lending** are **lending infrastructure**—they manage loans after origination but do not provide BNPL checkout or consumer credit. **Hyperswitch** is **payment orchestration**—it routes to BNPL providers but is not a lender. **No open-source project replicates the full BNPL network model.**
- **Open-source BNPL is essentially nonexistent as a consumer product.** The projects listed are either educational demos (`bnpl_system`, `InstallmentPay`, `django-react-iou-bnpl`), early-stage concepts (`T_Cred`), or loan management infrastructure (`Frappe Lending`, `RPB Lending`). **None provide a production-ready BNPL checkout with underwriting, merchant onboarding, and consumer credit.** Organizations wanting to offer BNPL to consumers will need a commercial provider or significant custom development with lending partners.
- **Hyperswitch is the most valuable open-source project for BNPL-adjacent infrastructure.** It enables merchants to offer BNPL alongside other payment methods through a unified integration, with routing and retry logic that can improve success rates . **The trade-off**: it does not underwrite, originate, or service installment loans—it delegates to BNPL providers.
- **Frappe Lending and RPB Lending are the strongest open-source lending engines** for managing installment loans after origination. RPB Lending is actively being hardened for production with validation, permissions, and regression coverage . **The trade-off**: both are Frappe/ERPNext-dependent and designed for loan servicing, not BNPL checkout.
- **Educational BNPL projects are useful for learning, not production.** `bnpl_system`, `InstallmentPay`, and `django-react-iou-bnpl` demonstrate data models and calculation logic but lack security, compliance, and integration capabilities . **Do not deploy these with real consumer credit data.**
- **Pricing opacity is universal across commercial BNPL vendors.** Klarna, Afterpay, Affirm, Zip, Sezzle, PayPal, Shop Pay Installments, Splitit, Sunbit, and Zilch all have merchant fee structures that vary by volume, merchant category, and negotiation. **Validate with direct vendor conversations against your average order value and target demographics.**
- Self-hosted open-source solutions require proper server setup, security hardening, and compliance work. **Consumer credit data and payment information are highly sensitive**—ensure your deployment meets all applicable regulatory and security requirements before handling real transactions.

---

**Made for developers, fintech teams, and merchants building transparent installment payment solutions.**
Let's make Buy Now Pay Later more open, data-driven, and consumer-friendly.
