# Mango Markets (mango-markets)

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

Mango Markets is a decentralized derivatives exchange and money market built on Solana, operated by the Blockworks Foundation. Mango v4 introduces unified margin accounts that combine spot trading, perpetual futures, and borrow/lend in a single risk engine, settled by the on-chain Mango v4 program. Beyond the on-chain program and the TypeScript client, the project exposes low-latency public market-data feeds through the mango-feeds geyser services - the Fills Feed (service-mango-fills, fills.mngo.cloud) and the Orderbook Feed (service-mango-orderbook, orderbook.mngo.cloud) - which stream fill events and L2/L3 orderbook state for Mango V4 Perp markets and Openbook spot markets over WebSocket.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/mango-markets/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/mango-markets/refs/heads/main/apis.yml)

## Tags

- Cryptocurrency
- DeFi
- Decentralized Exchange
- Perpetual Futures
- Spot
- Margin
- Orderbook
- Fills
- Market Data
- WebSocket
- Solana
- Mango v4

## Timestamps

- **Created:** 2026-05-30
- **Modified:** 2026-05-30

## APIs

### Mango v4 Fills Feed

Low-latency WebSocket feed (service-mango-fills) that parses Mango V4 Perp and Openbook event queues and emits individual fill events as they are processed by the validator. Supports getMarkets discovery, subscribe / unsubscribe by marketIds or by Mango account, and an optional headUpdates mode that emits event-queue head pointer updates. Fill events that occurred on a fork are revoked via a status='revoke' message.

- **Human URL:** [https://github.com/blockworks-foundation/mango-feeds/tree/lou/l3-feed/service-mango-fills](https://github.com/blockworks-foundation/mango-feeds/tree/lou/l3-feed/service-mango-fills)
- **Base URL:** `wss://fills.mngo.cloud`

#### Tags

- WebSocket
- Fills
- Market Data
- Perpetuals
- Spot
- Solana

#### Properties

- [Documentation](https://github.com/blockworks-foundation/mango-feeds/blob/lou/l3-feed/service-mango-fills/README.md)
- [AsyncAPI](asyncapi/mango-markets-feeds-asyncapi.yml) — [AsyncAPI Specification](https://www.asyncapi.com/docs/reference/specification/latest)
- [Source Code](https://github.com/blockworks-foundation/mango-feeds/tree/lou/l3-feed/service-mango-fills)
- [SDK](https://github.com/blockworks-foundation/mango-feeds/tree/main/ts/client)
- [Public A P I](https://api.mngo.cloud/fills/v1/)

### Mango v4 Orderbook Feed

Low-latency WebSocket feed (service-mango-orderbook) that parses Mango V4 Perp and Openbook spot bookside accounts and emits L2 (price / quantity) and L3 (per-order) checkpoints and per-side delta updates. Clients subscribe with subscriptionType=level for L2 or subscriptionType=book for L3; the server returns an initial checkpoint followed by streaming per-side updates with slot and writeVersion for ordering.

- **Human URL:** [https://github.com/blockworks-foundation/mango-feeds/tree/lou/l3-feed/service-mango-orderbook](https://github.com/blockworks-foundation/mango-feeds/tree/lou/l3-feed/service-mango-orderbook)
- **Base URL:** `wss://orderbook.mngo.cloud`

#### Tags

- WebSocket
- Orderbook
- L2
- L3
- Market Data
- Perpetuals
- Spot
- Solana

#### Properties

- [Documentation](https://github.com/blockworks-foundation/mango-feeds/blob/lou/l3-feed/service-mango-orderbook/README.md)
- [AsyncAPI](asyncapi/mango-markets-feeds-asyncapi.yml) — [AsyncAPI Specification](https://www.asyncapi.com/docs/reference/specification/latest)
- [Source Code](https://github.com/blockworks-foundation/mango-feeds/tree/lou/l3-feed/service-mango-orderbook)
- [SDK](https://github.com/blockworks-foundation/mango-feeds/tree/main/ts/client)
- [Public A P I](https://api.mngo.cloud/orderbook/v1/)

## Common Properties

- [Website](https://mango.markets)
- [Documentation](https://docs.mango.markets)
- [GitHub Organization](https://github.com/blockworks-foundation)
- [Source Code](https://github.com/blockworks-foundation/mango-feeds)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
