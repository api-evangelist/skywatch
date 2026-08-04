# SkyWatch (skywatch)

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

SkyWatch Space Applications is an Earth observation company whose **EarthCache** platform gives developers a single, provider-agnostic API to discover, price, order, and deliver commercial satellite imagery and geospatial data - from providers including Pleiades, SPOT, PlanetScope, SkySat, Sentinel-1, Sentinel-2, TripleSat, and Kompsat. The EarthCache API (base `https://api.skywatch.co/earthcache`, `x-api-key` auth) exposes Archive Search over historical imagery, Pipelines that monitor an area of interest and deliver imagery on a schedule, interval results with analytics and metadata download URLs, cost estimation, reusable output configurations, saved locations, and callback-based subscriptions. Imagery is billed per square kilometre with resolution-based purchase minimums.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/skywatch/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/skywatch/refs/heads/main/apis.yml)

## Tags

- Satellite Imagery
- Earth Observation
- Geospatial
- Remote Sensing
- EarthCache
- Imagery

## Timestamps

- **Created:** 2026-07-04
- **Modified:** 2026-07-04

## APIs

### SkyWatch EarthCache Archive Search API

Create an asynchronous archive search over historical satellite imagery for an area of interest and date window, filtering by resolution, coverage, and interval, then poll for matching search results (scene metadata, previews, and per-scene pricing) across SkyWatch's provider catalog.

- **Human URL:** [https://api-docs.earthcache.com/](https://api-docs.earthcache.com/)
- **Base URL:** `https://api.skywatch.co/earthcache`

#### Tags

- Archive
- Search
- Imagery

#### Properties

- [Documentation](https://api-docs.earthcache.com/)
- [API Reference](https://api-docs.earthcache.com/)
- [OpenAPI](openapi/skywatch-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/skywatch.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/skywatch.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Plans](plans/skywatch-plans-pricing.yml)

### SkyWatch EarthCache Pipelines API

Create, list, get, update, and delete pipelines - standing orders that monitor an area of interest between a start and end date, apply budget, cloud-cover, resolution, source, and interval constraints, and deliver matching imagery on a recurring schedule to a configured output.

- **Human URL:** [https://api-docs.earthcache.com/](https://api-docs.earthcache.com/)
- **Base URL:** `https://api.skywatch.co/earthcache`

#### Tags

- Pipelines
- Ordering
- Monitoring

#### Properties

- [Documentation](https://api-docs.earthcache.com/)
- [OpenAPI](openapi/skywatch-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/skywatch.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/skywatch.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### SkyWatch EarthCache Interval Results & Delivery API

Retrieve the results produced by pipeline intervals - either scoped to a single pipeline or across all pipelines - including per-interval status, cost, probability of collection, band metadata, and the analytics and metadata download URLs used to deliver each image.

- **Human URL:** [https://api-docs.earthcache.com/](https://api-docs.earthcache.com/)
- **Base URL:** `https://api.skywatch.co/earthcache`

#### Tags

- Interval Results
- Delivery
- Downloads

#### Properties

- [Documentation](https://api-docs.earthcache.com/)
- [OpenAPI](openapi/skywatch-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/skywatch.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/skywatch.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### SkyWatch EarthCache Cost Estimation API

Estimate cost before ordering - calculate the price of a location and intervals (honoring purchase minimums and pre-purchase discounts), calculate a full pipeline's cost together with probability of collection for tasking intervals, and look up per-resolution price information for the caller's plan.

- **Human URL:** [https://api-docs.earthcache.com/](https://api-docs.earthcache.com/)
- **Base URL:** `https://api.skywatch.co/earthcache`

#### Tags

- Pricing
- Cost
- Estimation

#### Properties

- [Pricing](https://skywatch.com/earthcache/pricing/)
- [Documentation](https://api-docs.earthcache.com/)
- [OpenAPI](openapi/skywatch-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/skywatch.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/skywatch.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### SkyWatch EarthCache Outputs & Bands API

List and retrieve output configurations - the reusable, named definitions (format such as GeoTIFF, band selection, and mosaic behavior) that a pipeline references to control how delivered imagery is rendered and packaged.

- **Human URL:** [https://api-docs.earthcache.com/](https://api-docs.earthcache.com/)
- **Base URL:** `https://api.skywatch.co/earthcache`

#### Tags

- Outputs
- Bands
- Formats

#### Properties

- [Documentation](https://api-docs.earthcache.com/)
- [OpenAPI](openapi/skywatch-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/skywatch.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/skywatch.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### SkyWatch EarthCache Locations API

Create, list, fetch, update, and delete saved locations - the Locations API abstracts spatial data supplied as KML or GeoJSON into a reusable server-side area-of-interest instance that Search and Pipelines can reference by id.

- **Human URL:** [https://api-docs.earthcache.com/](https://api-docs.earthcache.com/)
- **Base URL:** `https://api.skywatch.co/earthcache`

#### Tags

- Locations
- AOI
- GeoJSON

#### Properties

- [Documentation](https://api-docs.earthcache.com/)
- [OpenAPI](openapi/skywatch-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/skywatch.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/skywatch.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### SkyWatch EarthCache Subscriptions & Callbacks API

Register a callback URI to receive EarthCache platform events (HTTP webhooks) - create, list, update, and delete subscriptions, send sample payloads to a subscription, and list the callback invocations made over the last three months.

- **Human URL:** [https://api-docs.earthcache.com/](https://api-docs.earthcache.com/)
- **Base URL:** `https://api.skywatch.co/earthcache`

#### Tags

- Subscriptions
- Callbacks
- Webhooks

#### Properties

- [Documentation](https://api-docs.earthcache.com/)
- [OpenAPI](openapi/skywatch-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/skywatch.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/skywatch.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

## Common Properties

- [LinkedIn](https://www.linkedin.com/company/skywatch-apps)
- [Website](https://skywatch.com/)
- [Documentation](https://api-docs.earthcache.com/)
- [Plans](plans/skywatch-plans-pricing.yml)
- [Rate Limits](rate-limits/skywatch-rate-limits.yml)
- [Fin Ops](finops/skywatch-finops.yml)
- [Blog](https://skywatch.com/blog/)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
