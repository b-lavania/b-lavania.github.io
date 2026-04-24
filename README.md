# b-lavania.github.io
## AI Systems & Marketplace Product Lead: Logistics & Finance

---

# SUMMARY

## Differentiation

* Combines AI systems with real-world marketplace operations
* Focus on applied AI, not theoretical modeling
* Strong unit economics and operational outcomes

## Core Capability

Designing and deploying AI systems that directly impact revenue, cost, and scalability in marketplace environments.

---

# CASE STUDY PORTFOLIO
This portfolio provides structured evidence of product ownership, system design, and measurable outcomes across AI-driven marketplace systems.

---

# CASE STUDY 1: AI-DRIVEN COST ESTIMATION SYSTEM (MOVING MARKETPLACE)

## 1. Problem

Manual quoting for moving and last-mile delivery jobs was:

* Slow (hours to days)
* Inconsistent across operators
* Not scalable with demand growth

This created:

* Conversion drop-offs
* Operational bottlenecks
* Pricing inaccuracies impacting margins

---

## 2. Objective

Build an automated system that:

* Generates accurate job estimates from minimal user input
* Reduces time-to-quote to near real-time
* Maintains cost accuracy within acceptable variance

---

## 3. System Design

### Inputs

* User-uploaded images (rooms, items)
* Distance between pickup and drop-off

### Processing Pipeline

1. Image interpretation via LLM-assisted CV reasoning
2. Feature extraction:

   * Item types
   * Volume proxies
   * Weight heuristics
3. Optimization layer:

   * Inventory → estimated cubic volume
   * Volume + distance → cost model
   * Operations research algorithms to:

     * estimate job duration
     * determine optimal number of movers
     * perform 3D bin packing for truck loading efficiency

### Model Strategy

* Gemini Flash:

  * Fast inference
  * Used for standard jobs

* GPT-4.1:

  * Higher reasoning capability
  * Used for edge cases and ambiguity

### Model Routing Logic

* Default: low-cost, low-latency model
* Escalation conditions:

  * low confidence outputs
  * ambiguous image interpretation
  * high-value jobs

---

## 4. Evaluation Framework

Built internal testbench with:

### Metrics

* Accuracy: deviation from actual job cost
* Latency: response time per request
* Cost: per-inference cost

### Method

* Benchmarked against historical job dataset
* Compared model outputs vs human-generated quotes
* Iterated on prompt pipelines to improve consistency

---

## 5. Production Constraints

* Latency requirements for real-time UX
* Cost ceilings per quote to maintain margins
* Model output variability (non-deterministic responses)

### Mitigations

* Prompt standardization
* Structured output formatting
* Fallback logic for inconsistent responses

---

## 6. Outcomes

* Reduced quoting time from ~1 hour (mean) to ~3 minutes
* Achieved high estimation reliability: ~85% of jobs completed within algorithmically predicted time range
* Enabled near real-time pricing, unlocking automated booking flow

---

## 7. Business Impact

* Increased conversion by eliminating delayed quoting bottlenecks
* Reduced operational dependency on manual estimations
* Improved customer trust via consistent and predictable pricing

---

* Supported marketplace growth without linear ops scaling
* Increased conversion via faster response times
* Reduced operational overhead

---

# CASE STUDY 2: MARKETPLACE OPERATIONS & UNIT ECONOMICS

## 1. Marketplace Model

A managed marketplace with controlled supply onboarding.

### Key Design Choice

Prioritized:

* reliability
* fulfillment consistency

over open marketplace liquidity

---

## 2. Core Metrics

* CAC: ~$10
* LTV: $1,000+
* Retention: 12+ months
* Fill rate: ~99%

---

## 3. Why Metrics Are Strong

* Controlled supply acquisition
* Geographic focus
* Pricing discipline
* Operational standardization

---

## 4. Supply Strategy

* Curated onboarding of movers/providers
* Quality control over supply side
* Reduced variability in service delivery

---

## 5. Demand Strategy

* Targeted acquisition channels
* Optimized conversion funnel via fast quoting

---

## 6. Pricing System

* Based on:

  * estimated volume
    n  - distance
* Standardized pricing models reduce negotiation overhead

---

## 7. Outcomes

* High fulfillment reliability (99% fill rate)
* Strong retention driven by consistent service
* Favorable LTV/CAC dynamics

---

# CASE STUDY 3: SMS-BASED OPERATIONS AGENT

## 1. Problem

Customer communication required manual effort:

* booking confirmations
* status updates
* inquiry handling

---

## 2. Solution

Built SMS-based conversational agent to:

* respond to customer inquiries
* handle booking-related communication
* reduce manual coordination

---

## 3. System Design

### Inputs

* Customer SMS messages

### Processing

* LLM-based intent recognition
* Prompt pipelines for response generation

### Outputs

* Structured, context-aware responses

---

## 4. Constraints

* Need for fast response times
* High accuracy to avoid customer confusion
* Cost control per interaction

---

## 5. Outcomes

* Deflected ~50% of support tickets via automated SMS handling
* Reduced manual ops workload significantly in booking and coordination
* Improved response time and consistency of customer communication
* Enabled scalable communication layer without linear headcount growth

---

# CASE STUDY 4: MULTI-MODEL EVALUATION FRAMEWORK

## 1. Problem

Different AI models had varying performance across:

* cost
* latency
* reasoning ability

No standardized way to select models.

---

## 2. Solution

Built internal benchmarking system.

---

## 3. Models Tested

* GPT-4.1
* GPT-4o
* Gemini Flash variants

---

## 4. Evaluation Dimensions

* Accuracy (task completion)
* Latency (response time)
* Cost per request

---

## 5. Application

* Informed model selection decisions
* Enabled routing logic in production systems

---

## 6. Outcome

* Balanced cost vs performance tradeoffs
* Improved system efficiency across use cases

---

# CASE STUDY 5: BVXPRESS SaaS EXPANSION

## 1. Context

Single-product SaaS within M&A advisory firm.

---

## 2. Objective

Expand into multi-product SaaS business unit.

---

## 3. Actions

* Identified adjacent product opportunities
* Launched 5 products (0→1)
* Built integrated product ecosystem

---

## 4. Outcomes

* 1 → 3 core products
* ARPU: $450 → $600
* Retention: +14%
* Conversion: +7%

---


# END
