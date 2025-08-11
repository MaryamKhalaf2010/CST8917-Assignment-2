# Serverless Service Alternatives Report  
**Course:** CST8917 – Serverless Applications  
**Assignment 2 – Serverless Service Alternatives**  
**Author:** Maryam Khalaf  
**Date:** August 15, 2025  

---

##  Objective
This report compares core serverless services in Microsoft Azure with their Amazon Web Services (AWS) and Google Cloud Platform (GCP) equivalents.  
The comparison covers:  
- **Overview**  
- **Core Features (triggers, bindings, eventing)**  
- **Integration Options**  
- **Monitoring & Observability**  
- **Pricing Model**  
- **Strengths & Weaknesses**  

---

## 1) Azure Functions

### Overview
| Cloud Provider | Service Name | Overview |
|---|---|---|
| **Azure** | Azure Functions | Event-driven compute with triggers/bindings to multiple services, supports multiple runtimes. |
| **AWS** | AWS Lambda | Event-driven compute supporting many AWS services/events. |
| **GCP** | Cloud Functions | Lightweight, event-driven compute for GCP/cloud/hybrid events. |

### Core Features
- **Triggers:** HTTP, queue, topic, blob, timer, Cosmos DB, Event Hub, Event Grid (Azure); API Gateway, S3, DynamoDB Streams, SNS/SQS, CloudWatch Events (AWS); HTTP, Pub/Sub, Cloud Storage, Firestore (GCP).
- **Bindings:** Azure supports input/output bindings; AWS & GCP rely on SDKs and integrations.

### Integration Options
- Azure Functions integrates with Azure DevOps, GitHub Actions, Logic Apps; AWS Lambda integrates with CodePipeline, SAM, Step Functions; GCP Cloud Functions integrates with Cloud Build, Workflows.

### Monitoring & Observability
- Azure Monitor + App Insights; AWS CloudWatch; GCP Cloud Monitoring & Logging.

### Pricing Model
- Pay-per-execution, memory, execution time for all three; free quotas available.

### Strengths & Weaknesses
- **Azure:** Rich binding model; tight integration with Azure services; region availability narrower than AWS.
- **AWS:** Largest ecosystem of triggers; very mature; lacks direct binding model.
- **GCP:** Simple and fast deploy; fewer trigger types than AWS/Azure.

---

## 2) Durable Functions

### Overview
| Cloud Provider | Service Name | Overview |
|---|---|---|
| **Azure** | Durable Functions | Extension of Azure Functions for stateful orchestrations. |
| **AWS** | AWS Step Functions | Visual workflows to coordinate AWS Lambda/services. |
| **GCP** | Workflows | Orchestrates and connects services via YAML/JSON definitions. |

### Core Features
- **Patterns:** Function chaining, fan-out/fan-in, async HTTP APIs, monitoring, human interaction.
- AWS Step Functions offers Standard & Express workflows; GCP Workflows supports synchronous & async executions.

### Integration Options
- All integrate with native serverless compute (Functions/Lambda) and other services.

### Monitoring & Observability
- Azure Monitor; AWS CloudWatch (workflow execution history); GCP Cloud Logging & Cloud Trace.

### Pricing Model
- Per-action/state transition; free tier available.

### Strengths & Weaknesses
- **Azure:** Easy for existing Functions devs; fewer visual tools than AWS Step Functions.
- **AWS:** Powerful visual designer; tight AWS service integrations.
- **GCP:** Simple YAML; fewer built-in integrations.

---

## 3) Azure Logic Apps

### Overview
| Cloud Provider | Service Name | Overview |
|---|---|---|
| **Azure** | Azure Logic Apps | Low-code workflow integration and automation service. |
| **AWS** | AWS Step Functions + EventBridge + AppFlow | Combines orchestration, events, and SaaS integration. |
| **GCP** | Workflows + AppSheet + Eventarc | Orchestration, SaaS automation, and event routing. |

### Core Features
- 300+ connectors in Logic Apps; AWS has fewer native SaaS connectors; GCP has limited direct connectors.

### Integration Options
- CI/CD via ARM/Bicep/Terraform; AWS via SAM/CDK; GCP via Deployment Manager/Terraform.

### Monitoring & Observability
- Azure Monitor, run history; AWS CloudWatch; GCP Cloud Logging.

### Pricing Model
- Per-action or connector execution.

### Strengths & Weaknesses
- **Azure:** Rich connector library; visual designer.
- **AWS:** More coding; fewer drag-drop tools.
- **GCP:** Minimal native connectors.

---

## 4) Azure Service Bus (Queues & Topics)

### Overview
| Cloud Provider | Service Name | Overview |
|---|---|---|
| **Azure** | Azure Service Bus | Enterprise-grade message broker with queues/topics (pub/sub). |
| **AWS** | Amazon SQS + SNS | Managed queue + pub/sub topic messaging. |
| **GCP** | Pub/Sub | Global pub/sub messaging. |

### Core Features
- Service Bus offers FIFO, DLQ, scheduled delivery; AWS SQS offers FIFO/DLQ; SNS handles pub/sub; GCP Pub/Sub offers global topics/subscriptions.

### Integration Options
- All integrate with serverless compute (Functions/Lambda/Cloud Functions).

### Monitoring & Observability
- Azure Monitor; AWS CloudWatch; GCP Monitoring.

### Pricing Model
- Pay-per-operation/message.

### Strengths & Weaknesses
- **Azure:** Strong hybrid integration; complex setup.
- **AWS:** Clear separation (SQS vs SNS); regional service.
- **GCP:** Global scale; fewer advanced broker features.

---

## 5) Azure Event Grid

### Overview
| Cloud Provider | Service Name | Overview |
|---|---|---|
| **Azure** | Event Grid | Event routing with filtering and delivery guarantees. |
| **AWS** | Amazon EventBridge | Event bus for routing AWS and SaaS events. |
| **GCP** | Eventarc | Event routing from GCP services and custom sources. |

### Core Features
- Filtering by attributes; retries; dead-letter destinations.

### Integration Options
- All integrate with serverless compute and messaging.

### Monitoring & Observability
- Metrics, logs in respective monitoring tools.

### Pricing Model
- Per-million events.

### Strengths & Weaknesses
- **Azure:** Broad source support; simpler than EventBridge rules.
- **AWS:** Rich schema registry; SaaS partner events.
- **GCP:** Tight GCP integration; fewer sources.

---

## 6) Azure Event Hubs

### Overview
| Cloud Provider | Service Name | Overview |
|---|---|---|
| **Azure** | Event Hubs | Big data streaming ingestion service. |
| **AWS** | Amazon Kinesis Data Streams | Scalable, real-time data streaming. |
| **GCP** | Pub/Sub | Real-time messaging and streaming. |

### Core Features
- Event Hubs supports Kafka protocol; Kinesis integrates tightly with AWS analytics; GCP Pub/Sub integrates with Dataflow.

### Integration Options
- Stream processing via Azure Stream Analytics; AWS Kinesis Data Analytics; GCP Dataflow.

### Monitoring & Observability
- Native monitoring; AWS CloudWatch; GCP Monitoring.

### Pricing Model
- Capacity units or throughput pricing.

### Strengths & Weaknesses
- **Azure:** Kafka endpoint; integration with Stream Analytics.
- **AWS:** Strong with analytics services.
- **GCP:** Global messaging; simpler operations.

---
