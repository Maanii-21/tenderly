# Tenderly: AI-Powered Real Estate Tender Intelligence Platform

An end-to-end AI-driven platform designed to automate, streamline, and optimize the tendering process for real estate developers, EPC contractors, facility managers, and infrastructure consultants. By leveraging **Natural Language Processing (NLP)**, **Machine Learning (ML)**, **GIS Spatial Analysis**, and **Predictive Analytics**, Tenderly transforms raw procurement notices into actionable win strategies.

---

## Frontend Layout & Interface Design

Tenderly features a modern, responsive, microservices-backed presentation layer built for high readability, operational speed, and intuitive decision-making.

```
+----------------------------------------------------------------------------------------------------------+
|   TENDERLY PLATFORM                                                 [Global Search]  [3] [Profile] |
+-------------------------------+--------------------------------------------------------------------------+
|  NAVIGATION                   |  DASHBOARD OVERVIEW                                                   |
|                               +------------------------+-----------------------+-------------------------+
|   Dashboard               |  Active Tenders        |  Matched Tenders      |  Avg Win Probability    |
|   Smart Discovery         |  1,420                 |  128 (Eligible)       |  78.4%                  |
|   Matched Tenders         +------------------------+-----------------------+-------------------------+
|   Win Probability         |                                                                          |
|   Bid Assistant           |  GIS SPATIAL ANALYSIS & TENDER HEATMAP                                |
|   Analytics & ROI         |  +--------------------------------------------------------------------+  |
|   Business Profile        |  |  [Satellite Overlay: ON]  [Density Threshold: High]                |  |
|                               |  |                                                                    |  |
|                               |  |         High Density Zone (NCR Region)                           |  |
|                               |  |         Tender ID: #TND-8942 (Govt Commercial Hub)               |  |
|                               |  |         Tender ID: #TND-3301 (Residential Infrastructure)        |  |
|                               |  |                                                                    |  |
|                               |  +--------------------------------------------------------------------+  |
|                               |                                                                          |
|                               |   TOP RECOMMENDED TENDERS FOR YOU                                     |
|                               |  +--------------------------------------------------------------------+  |
|                               |  | Tender Title / Issuing Auth    | Value     | Deadline  | Win Prob | Action|  |
|                               |  +--------------------------------+-----------+-----------+----------+-------+  |
|                               |  | Commercial Complex Phase-II    | $12.5M    | 2026-08-15|   89%    | [View]|  |
|                               |  | State Housing Board            |           |           |          |       |  |
|                               |  +--------------------------------+-----------+-----------+----------+-------+  |
|                               |  | Smart City Road Expansion      | $45.0M    | 2026-08-20|   74%    | [View]|  |
|                               |  | National Infra Corp            |           |           |          |       |  |
|                               |  +--------------------------------+-----------+-----------+----------+-------+  |
+-------------------------------+--------------------------------------------------------------------------+
```

### Key UI Modules & Features
| Module | Key Feature | Core Benefit |
| :--- | :--- | :--- |
| **Smart Discovery** | Aggregated tender feed with real-time updates and GIS spatial mapping. | Eliminates missed opportunities across portals. |
| **Profile Matching** | AI-driven eligibility check and automated scoring. | Surfaces only qualified, actionable tender opportunities. |
| **Win Probability Engine** | ML-based award probability percentage derived from historical data. | Helps prioritize high-ROI, high-value bid submissions. |
| **Bid Assistant** | Interactive checklist, automated document gap analysis, & clause extractor. | Drastically reduces compliance disqualification risks. |
| **Analytics Dashboard** | Win-rate trends, category insights, dynamic cost projections, & ROI tracking. | Enables data-driven procurement strategies. |

---

## System Workflow

here is the basic workflow of the system

```
       [ 🌐 External Data Sources ]
  (eProcurement, GeM, World Bank, CPPP)
                    │
                    ▼
       ┌─────────────────────────┐
       │   1. DATA LAYER         │ 
       └────────────┬────────────┘
                    │
                    ▼
       ┌─────────────────────────┐
       │ 2. BUSINESS PROFILE     │ 
       └────────────┬────────────┘
                    │
                    ▼
       ┌─────────────────────────┐
       │ 3. AI / ML INFERENCE    │ 
       └────────────┬────────────┘
                    │
                    ▼
       ┌─────────────────────────┐
       │ 4. API GATEWAY          │ ─
       └────────────┬────────────┘
                    │
                    ▼
       ┌─────────────────────────┐
       │ 5. PRESENTATION LAYER   │ 
       └─────────────────────────┘
```

1. **Ingestion & Normalization:** Automated web scrapers and API connectors aggregate tender notices daily across national and international portals. Unstructured documents are extracted into structured schemas.
2. **Business Profiling:** The user onboarding module captures company parameters (turnover, RERA registration, past contract values, ISO certifications, operational geography, and equipment lists).
3. **AI Eligibility & Relevance Matching:** NLP algorithms evaluate tender criteria against business profiles to assign an instant **Relevance & Eligibility Score**.
4. **Predictive Analytics & Pricing:** Machine Learning models evaluate historical bidding data, local construction density (via satellite GIS data), and economic indicators (material price indices, inflation) to generate **Win Probability %** and optimized pricing suggestions.
5. **Bid Preparation & Gap Analysis:** The Bid Assistant highlights missing documentation, analyzes qualification gaps, and assists in proposal assembly.

---

## Data Collection & Sources

Tenderly continuously aggregates procurement data to provide real-time coverage and market insights.

### 1. Primary Tender Data Sources
* **Government eProcurement Portals:** Central Public Procurement Portal (CPPP), State & Local Municipal Portals.
* **National Procurement Marketplaces:** Government e-Marketplace (GeM), RERA National Portals, Tender Tiger.
* **International Financial Agencies:** World Bank, Asian Development Bank (ADB), Asian Infrastructure Investment Bank (AIIB).

### 2. Standardized Tender Data Schema

| Field Name | Description | Data Type |
| :--- | :--- | :--- |
| `Tender ID` | Unique identifier for the tender | String (UUID) |
| `Title` | Official title of the tender | Text |
| `Issuing Authority` | Name of the publishing organization / department | Text |
| `Category` | Industry domain (e.g., Construction, Property Management, Infra) | Enum |
| `Estimated Value` | Approximate contract value (INR / USD) | Numeric |
| `Submission Deadline` | Last date and time for bid submission | DateTime |
| `Eligibility Criteria` | Technical, financial, and regulatory qualifications required | Text |
| `Geographic Scope` | State, city, or regional boundaries of execution | Text |
| `Document URL` | Direct link to the official tender document / RFP | URL |

### 3. Contextual & Spatial Data Layers
* **GIS Spatial & Satellite Context:** Satellite construction density heatmaps for regional demand evaluation.
* **Economic & Financial Indicators:** Commodity/material price indices, inflation rates, and GDP metrics for dynamic cost forecasting.

-

## Links
* **CPPP India:** [eprocure.gov.in](https://eprocure.gov.in)
* **Government e-Marketplace:** [gem.gov.in](https://gem.gov.in)
* **RERA Portal:** [rera.gov.in](https://rera.gov.in)
* **ADB Tenders:** [adb.org/projects/tenders](https://www.adb.org/projects/tenders)






