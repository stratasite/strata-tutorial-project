# Strata Tutorial Project

A complete, pre-built semantic layer for the [TPC-DS](https://www.tpc.org/tpcds/) retail benchmark dataset. Use this to get a working Strata project deployed in minutes.

## What's included

**Three retail data channels, fully modelled:**

- **Store** — in-store sales and returns, store dimensions
- **Catalog** — catalog orders, returns, call center, catalog pages
- **Inventory** — snapshot inventory levels by item, warehouse, and date

**Common dimensions shared across channels:**

- Customer (with PII tagging), Customer Address, Customer Demographics
- Date Dimension, Time Dimension, Item
- Household Demographics, Income Band, Ship Mode, Warehouse, Reason
- Role-playing dimensions: Returning Customer, Billed Customer, Catalog Ship Date

**Security policies:**

- PII masking on customer email via group-tag access control
- Row-level filtering on profit measures by item category

## Setup

The easiest way to set this up is via your Strata instance:

1. Open your Strata instance and click **Try Tutorial** on the home screen
2. Follow the 3-step guide shown — it generates the `strata tutorial` command pre-filled with your API key and project URL
3. Run the command, then `strata deploy`

```bash
strata tutorial -s <your-strata-url> -a <your-api-key>
cd tutorial
strata deploy
```

## Data

The tutorial uses a TPC-DS DuckDB database bundled with the Strata Docker image at `/data/tpcds.duckdb`. No separate data download or setup is needed.

## Learn more

See [AGENTS.md](AGENTS.md) for a full reference on Strata semantic model concepts, patterns, and CLI commands.
