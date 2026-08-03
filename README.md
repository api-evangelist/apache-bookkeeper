# Apache BookKeeper (apache-bookkeeper)

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

Apache BookKeeper is a scalable, fault-tolerant, and low-latency storage service optimized for real-time workloads developed by the Apache Software Foundation. It provides a simple log-oriented storage abstraction called ledgers for reliable, replicated storage of sequential data. BookKeeper is used as the durable log storage layer in Apache Pulsar and other distributed messaging and stream processing systems. It provides a Java client API and an HTTP Admin REST API for cluster management, bookie monitoring, and auto-recovery operations.

**URL:** [https://bookkeeper.apache.org/](https://bookkeeper.apache.org/)

**Run:** [Capabilities Using Naftiko](https://github.com/naftiko/fleet?utm_source=api-evangelist&utm_medium=readme&utm_campaign=company-api-evangelist&utm_content=repo)

## Tags

 - Apache, Distributed Systems, Log Storage, Open Source, Storage, Streaming

## Timestamps

- **Created:** 2026-03-16
- **Modified:** 2026-04-19

## APIs

### Apache BookKeeper Admin API
The Apache BookKeeper HTTP Admin API provides REST endpoints for managing and monitoring BookKeeper clusters, bookies, ledgers, and auto-recovery operations. It enables programmatic cluster administration, ledger inspection, bookie health monitoring, and garbage collection management.

**Human URL:** [https://bookkeeper.apache.org/docs/admin/http](https://bookkeeper.apache.org/docs/admin/http)

#### Tags

 - Administration, Cluster Management, Monitoring

#### Properties

- [Documentation](https://bookkeeper.apache.org/docs/admin/http)
- [OpenAPI](openapi/apache-bookkeeper-admin-openapi.yaml)
- [GettingStarted](https://bookkeeper.apache.org/docs/getting-started/installation)

### Apache BookKeeper Java Client API
The BookKeeper Java client API provides programmatic access for creating, writing, reading, and managing ledgers. It supports both the legacy LedgerHandle API and the newer Ledger API with explicit durability guarantees.

**Human URL:** [https://bookkeeper.apache.org/docs/api/ledger-api](https://bookkeeper.apache.org/docs/api/ledger-api)

#### Tags

 - Java, Ledger, Storage

#### Properties

- [Documentation](https://bookkeeper.apache.org/docs/api/ledger-api)
- [APIReference](https://bookkeeper.apache.org/docs/api/javadoc/)

## Common Properties

- [GitHubOrganization](https://github.com/apache)
- [GitHubRepository](https://github.com/apache/bookkeeper)
- [Documentation](https://bookkeeper.apache.org/)
- [GettingStarted](https://bookkeeper.apache.org/docs/getting-started/installation)
- [Support](https://bookkeeper.apache.org/community/mailing-lists)
- [TermsOfService](https://www.apache.org/licenses/)
- [ChangeLog](https://github.com/apache/bookkeeper/releases)

## Features

| Name | Description |
|------|-------------|
| Ledger Storage | Append-only log segments called ledgers provide the foundational storage primitive for reliable sequential data storage. |
| Ensemble Replication | Data is written to a configurable ensemble of bookies with write quorum and ack quorum parameters for fault tolerance. |
| Auto-Recovery | Built-in under-replication detection and automatic ledger re-replication when bookie nodes fail. |
| HTTP Admin API | RESTful HTTP Admin API for managing ledgers, bookies, cluster configuration, and triggering recovery operations. |
| Metrics Export | Prometheus-format metrics endpoint for monitoring bookie performance and storage utilization. |
| Auditor Election | ZooKeeper-based leader election for the auditor role responsible for detecting under-replicated ledgers. |
| Garbage Collection | Configurable garbage collection for reclaiming storage from deleted or expired ledger data. |
| Journal and Ledger Storage | Separate journal and ledger storage paths optimized for sequential write throughput and random read performance. |

## Use Cases

| Name | Description |
|------|-------------|
| Durable Log Storage | Serve as the replicated, durable write-ahead log for Apache Pulsar topics and distributed streaming systems. |
| Distributed Transaction Logs | Store distributed transaction log segments for systems requiring exactly-once semantics and durable commit records. |
| Metadata Store | Persist metadata and configuration data for distributed systems requiring consistent, replicated storage. |
| Stream Processing Storage | Provide low-latency, high-throughput sequential storage for real-time stream processing pipelines. |
| Cluster Administration | Monitor and manage BookKeeper clusters using the HTTP Admin API for operational visibility and recovery. |

## Integrations

| Name | Description |
|------|-------------|
| Apache Pulsar | BookKeeper serves as the durable log storage layer for Apache Pulsar messaging topics. |
| Apache ZooKeeper | ZooKeeper is used for bookie coordination, auditor election, and cluster metadata management. |
| Apache Hadoop | BookKeeper can be used with Hadoop ecosystem tools for reliable log storage alongside HDFS. |
| Prometheus | BookKeeper exports Prometheus-format metrics for cluster monitoring and alerting. |
| Grafana | Grafana dashboards consume BookKeeper Prometheus metrics for operational visibility. |

## Artifacts

Machine-readable API specifications organized by format.

### OpenAPI

- [Apache BookKeeper Admin API](openapi/apache-bookkeeper-admin-openapi.yaml)

### JSON Schema

9 schema files covering LedgerList, LedgerMetadata, LedgerEntries, BookieInfo, BookieList, ClusterInfo, BookieState, GcStatus, and AuditorInfo.

### JSON-LD

- [Apache BookKeeper Context](json-ld/apache-bookkeeper-context.jsonld)

## Capabilities

Naftiko capabilities organized as shared per-API definitions composed into customer-facing workflows.

### Shared Per-API Definitions

- [Apache BookKeeper Admin API](capabilities/shared/bookkeeper-admin.yaml) — 10 operations for monitoring, ledger inspection, bookie management, and auto-recovery

### Workflow Capabilities

| Workflow | APIs Combined | Tools | Persona |
|----------|--------------|-------|---------|
| [Apache BookKeeper Cluster Management](capabilities/bookkeeper-cluster-management.yaml) | Admin API | 6 | Cluster Administrator, Storage Engineer |

## Vocabulary

- [Apache BookKeeper Vocabulary](vocabulary/apache-bookkeeper-vocabulary.yaml) — Domain taxonomy mapping 7 resources, 5 actions, 1 workflow, and 2 personas for cluster management and ledger operations

## Rules

- [Apache BookKeeper Spectral Rules](rules/apache-bookkeeper-spectral-rules.yml) — 12 rules across 5 categories enforcing Apache BookKeeper API conventions

## Maintainers

**FN:** Kin Lane

**Email:** info@apievangelist.com
