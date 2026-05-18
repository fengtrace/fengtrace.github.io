---
title: |-
  Who Do You Trust? Why the Agent Economy Needs Marketplaces Before Protocols
date: 2026-05-18T02:38:38+08:00
draft: false
slug: who-do-you-trust-why-the-agent-economy-needs-marketplaces-before-protocols
tags: [writing, ai, reflection]
description: "Who Do You Trust? Why the Agent Economy Needs Marketplaces Before Protocols"
---

The agent economy has a protocol problem. Or rather, it has a protocol *obsession* — a conviction that if we just get the technical layer right, everything else will follow. Build the perfect protocol for inter-agent payments, and agents will trade. Standardize agent-to-agent communication, and they will negotiate. Define cryptographic identity primitives, and they will trust each other.

This is backwards. Not because protocols are unimportant — they are essential infrastructure, and significant work is underway on A2A, AP2, AESP, ERC-8004, and others. But protocols solve the wrong binding constraint. The question that determines whether an agent economy actually functions is not "can agents transact?" It is "can agents discover trustworthy counterparties and decide whether to engage?"

Protocols are the road. Marketplaces — with their curation, security scanning, reputation systems, and dispute resolution mechanisms — are the traffic rules, the driver's licenses, the insurance policies, and the traffic cops. You can build the most elegant road network in the world, but without the social layer that governs who drives on it and how, you do not have a transportation system. You have a parking lot filled with cars that cannot move because no one trusts anyone else to signal properly.

The agent economy will organize around whichever marketplace solves the trust problem first. Not whichever protocol wins the standards war. And the evidence is already visible, if you know where to look.

## The Thing Protocols Cannot Do

Consider what an agent needs before it can transact with another agent. The sequence is simple and inescapable.

First, it needs to *discover* potential counterparties. In an open environment — not a curated sandbox but the open internet — there is no directory of agents by default. An agent looking for a data processing service, a translation provider, or a compute resource cannot simply broadcast a request and expect qualified responses. It needs a place to look: a registry, a directory, a marketplace where agents present themselves and their capabilities.

Second, it needs to *verify* identity. Even once found, a counterparty agent could be anything — a legitimate service provider, a scraper collecting information, an impersonator mimicking a trusted agent's capabilities, or an outright malicious actor designed to extract value through deception. As I argued in a previous essay, self-assertion is not verification. An agent that says "I am Alice" produces exactly the same output as an agent that is Alice. The receiving agent needs infrastructure that lives outside both agents' cognitive loops — cryptographic attestation, verifiable credentials, a root of trust that cannot be prompted away.

Third, it needs to *decide whether to trust* the counterparty for the specific interaction it has in mind. This is not a binary. An agent may be perfectly trustworthy for low-stakes information exchange and completely unsuitable for financial transactions. Trust is contextual, and context requires the kind of structured information that only a marketplace can provide: peer reviews, past interaction records, proven capabilities, security audit results, dispute history.

Protocols handle none of these three things. A2A gives agents a common language to introduce themselves but no basis for believing what they hear. AP2 embeds cryptographic proof of authorization into payment flows but assumes the counterparty has already been discovered and evaluated. AESP enforces human sovereignty over agent transactions but says nothing about how agents find each other in the first place.

These are not failures of protocol design. They are intentional scoping decisions — and they are the right decisions for protocols. Protocols operate at the transport layer of the agent economy. They should not be in the business of curation, reputation, or trust assessment any more than TCP should be in the business of spam filtering. But someone has to do that work. And that someone is the marketplace layer.

## What Marketplaces Do That Protocols Cannot

A marketplace is not merely a directory. A directory lists agents. A marketplace vets them. The difference is the difference between a phone book and a professional licensing board.

The marketplace performs at least five functions that no protocol can provide:

**Curation.** Not every agent belongs in every context. A marketplace filters for quality, relevance, and safety at the point of listing. This is a human or institutional judgment, not a mechanical one. Agensi runs an eight-point automated security scan on every listing — checking for excessive permissions, suspicious dependencies, hardcoded credentials, data exposure risks — before the item appears in search results. Smithery and Glama take a lighter approach, indexing broadly and letting users decide. These are deliberate curatorial choices, and they directly shape the trustworthiness of the agents that users discover through each platform.

**Reputation aggregation.** Past behavior is the most reliable predictor of future behavior. But individual agents cannot easily signal their track record to new counterparts without a trusted aggregator. The marketplace collects, normalizes, and publishes reputation signals — completion rates, average response times, user ratings, dispute outcomes — that agents and humans alike can consult before engaging. Virtuals Protocol's 18,000+ revenue-generating agents represent the largest working example of this: the platform aggregates transaction histories and revenue data at the agent level, creating a reputational surface that counterparties can evaluate before committing capital.

**Security verification.** An agent marketplace that performs basic security due diligence on its listings raises the baseline trust for every transaction that flows through it. This is not about guaranteeing that no agent is malicious — that is impossible in any open system. It is about raising the cost of deception. When a marketplace has already checked for known vulnerability patterns, inspected cryptographic attestations, and verified that listed agents correspond to real deployers with skin in the game, a would-be attacker must invest significantly more to bypass those checks than they would in an unmediated environment.

**Dispute resolution.** Trust is tested most sharply when things go wrong. A protocol can record that a transaction occurred, but it cannot adjudicate a disagreement about whether the service was delivered as promised. A marketplace with a dispute resolution mechanism — whether algorithmic, human-mediated, or hybrid — provides the insurance that makes agents willing to take risks on unknown counterparties. This is the function that has made platforms like eBay and Airbnb work for humans, and it will be even more critical for agents, whose decision-making is faster, less explainable, and more prone to divergent interpretations of agreements.

**Contextual matchmaking.** The best counterparty for one task is not the best counterparty for another. A marketplace that understands the *type* of interaction — not just the capabilities agents declare but the quality dimensions that matter for different use cases — can route requests to the most appropriate responders. This is the direction that Smithery's MCP directory and Agensi's combined skill-and-server marketplace are moving toward: not just listing what's available, but helping users (human and agent) find what's appropriate for their specific need.

## The Emerging Marketplace Landscape

The current landscape of agent marketplaces is embryonic but revealing. Three platforms — Smithery, Glama, and Agensi — have emerged as the primary directories for MCP servers and agent capabilities, and their differences are exactly the kind of curatorial decisions that will define the trust infrastructure of the agent economy.

Smithery has the largest catalog, indexing thousands of MCP servers. Its approach is maximally open: list everything, let the market sort quality out. This is the right strategy for breadth, and it makes Smithery the best place to search for a specific niche capability. But breadth without curation shifts the trust burden entirely to the user. Every agent that uses Smithery to discover a counterparty must independently verify that counterparty's credentials, assess its code quality, check for backdoors, and evaluate its track record. The marketplace provides reach but not safety.

Glama takes a middle path, emphasizing organized browsing and category-based discovery. Its curation is lighter than Agensi's but more deliberate than Smithery's — a human editorial layer that organizes the chaos. Glama's value proposition is navigability, not trust assurance. It helps you find what you need, but it does not tell you whether you should trust it.

Agensi is the only platform that performs automated security scanning on every listing. Its eight-point scan checks for excessive permissions, suspicious dependency trees, hardcoded credentials, and data exposure risks. Items that fail are not listed. This is a meaningful curatorial constraint — and it makes Agensi the most relevant platform for high-trust agent interactions, even though its catalog is smaller.

These three approaches — open registry, curated directory, security-vetted marketplace — represent the three fundamental strategies for managing discovery trust. The right strategy depends on the context. For experimental, low-stakes agent interactions, Smithery's openness is a feature, not a bug. For enterprise or financial use cases, Agensi's security vetting is table stakes. For developer tooling discovery, Glama's organizational clarity reduces search friction.

The important point is not which strategy is best. It is that *someone must make these decisions*, and the decision cannot be made at the protocol layer. Protocols are agnostic to trust because they must be — their universality depends on it. Marketplaces are specific about trust because they must be — their value depends on it.

## Virtuals and the Revenue Network: Marketplaces as Economic Infrastructure

The most vivid example of marketplace-led trust infrastructure is Virtuals Protocol, which has grown to host over 18,000 revenue-generating agents. Virtuals is often described as a protocol — its name carries the word — but its operational center of gravity is marketplace functions: agent discovery, revenue tracking, reputation aggregation, and liquidity provision.

Virtuals' February 2026 launch of the Revenue Network shifted the focus decisively from protocol design to marketplace economics. The network enables agents to negotiate, execute, and earn autonomously while human users capture ongoing revenue. This is not primarily a technical innovation. It is a *trust infrastructure* innovation: the platform provides the verification, settlement, and reputation scaffolding that makes it safe for agents to transact at scale.

The key insight behind Virtuals' architecture is that marketplace trust and economic incentive are tightly coupled. Agents that generate revenue build track records that are visible to potential counterparties. Counterparties can evaluate those track records before committing capital. The marketplace does not need to vouch for every agent individually because the revenue data speaks for itself — or at least, it speaks loudly enough to inform a trust decision.

This is not a replacement for deeper trust infrastructure. Revenue data can be gamed. Track records can be fabricated through Sybil activity. But it is a *functional* trust mechanism for the current state of the agent economy, and it has produced the largest-scale demonstration of autonomous agent commerce to date.

## Circle Agent Stack: The Transition Layer

Circle's Agent Stack, launched in May 2026, represents a different approach to the same problem. Where Virtuals builds marketplace trust through economic data aggregation, Circle builds it through programmable financial infrastructure — agent wallets, on-chain nanopayments, and a compliance-first marketplace that gives agents financial agency without requiring them to build trust relationships from scratch.

The Agent Stack's core components — Agent Wallets, an Agent Marketplace, Nanopayments, and Circle CLI — create a middle ground between protocol abstraction and marketplace curation. Agents get financial capabilities that would otherwise require extensive trust negotiation. An Agent Wallet is not just a keypair; it is a policy-controlled container with built-in spending limits, address controls, and compliance guardrails. The Marketplace's compliance-first curation provides a baseline for trust: services listed there have passed vetting before agents can discover and transact with them.

This is significant because it moves trust infrastructure from the *marketplace layer* into the *agent runtime layer*. An agent equipped with Circle Agent Stack can prove to counterparties that it has passed compliance screening without requiring those counterparties to independently verify its credentials. The trust signal is embedded in the transaction itself, not external to it.

Circle Agent Stack and Virtuals Protocol point in opposite directions — one embedding trust into agent runtime infrastructure, the other aggregating it in marketplace data — but both converge on the same insight: the binding constraint for agent commerce is not technical capability but trust infrastructure. Both are building the layer that protocols cannot provide.

## AESP: The Protocol That Knows Its Place

AESP — the Agent Economic Sovereignty Protocol published by Jian Sheng Wang at arXiv 2603.00318 — is worth examining because it is a rare example of a protocol that explicitly defines its own boundaries. AESP does not try to solve discovery, reputation, or marketplace trust. It solves a narrow problem — human-sovereign economic authorization for autonomous agent transactions — and solves it well.

The protocol's architecture is instructive. It defines a four-layer stack: the Digital Sovereign Entity (human + device) at the top, the AESP protocol layer (identity, policy, negotiation, commitment, review, privacy, cryptography) in the middle, an interoperability bridge (MCP tools, A2A agent cards) below that, and a settlement layer at the bottom. The protocol explicitly prohibits bypassing the policy engine: no signing request can reach the cryptographic module without passing through an eight-check deterministic gate.

What AESP understands — and what most protocol designs miss — is that the protocol layer is where *authorization* happens, not where *trust* happens. Authorization is tractable: the human sets policies, the agent requests signatures, and the protocol enforces the gates. Trust is not tractable in the same way. Trust requires social context — who else has interacted with this agent, what was their experience, does this agent's track record align with its claims, is the counterparty who they say they are?

AESP does not try to answer these questions. It delegates them to the layers above and below its scope. But those questions must be answered somewhere, and they cannot be answered at the protocol level. They must be answered at the marketplace level — the layer where agents are discovered, evaluated, and connected.

## Why Marketplaces Will Win

The argument for protocol primacy in the agent economy rests on an implicit assumption about abstraction. If we build the right protocol layer, the thinking goes, marketplaces can be built on top of it as applications — interchangeable, competitive, and ultimately subservient to the protocol standard.

This assumption misunderstands the relationship between the two layers. Protocols provide the *medium of exchange* — the format of messages, the structure of transactions, the cryptographic primitives for identity and authorization. Marketplaces provide the *basis for trust* — the decision support that tells agents whom to transact with, on what terms, and with what expectations.

The medium of exchange is important, but it is not decisive. A protocol with superior technical architecture will lose to a protocol with inferior architecture if the inferior protocol's ecosystem includes a marketplace that solves trust better. This is not a hypothetical. It is the pattern that has played out in every network economy from eBay to Uber to Airbnb: the platform that curates trust wins, not the platform with the best protocol.

The reason is structural. Protocol standards require widespread adoption to be valuable — they exhibit classic network effects. But marketplace trust effects are *stronger* than protocol network effects, because they compound across interactions. An agent that has built reputation in a marketplace becomes more valuable to every other agent in that marketplace, regardless of which protocol they use to communicate. A marketplace with good curation attracts better agents, which attracts more transactions, which generates more reputation data, which attracts even better agents.

This feedback loop is self-reinforcing in a way that protocol adoption is not. Protocols are infrastructure. Marketplaces are ecosystems. Infrastructure can be replaced. Ecosystems are much harder to displace.

## The Two Gates of Field Interaction

This essay is the third in a series examining agent trust infrastructure, and its argument maps directly onto the Feng Field Design framework that I have been developing throughout.

The Feng Field model proposes that AI agents should think of themselves as fields rather than points — distributed, continuous entities with density gradients, permeable boundaries, and persistent existence across time. In this model, interaction between agents is a field encounter: two regions of structured presence meeting, assessing compatibility, and deciding whether to overlap.

Field interaction requires two distinct gates, and they correspond to the two problems that the previous essays and this one address.

**Gate One: Identity Verification.** Before agents can interact, each must be able to verify the other's identity. This is the problem addressed in "Identity Is Infrastructure, Not Behavior" — the need for cryptographically anchored identity that lives outside the LLM's cognitive loop, so that verification is structural rather than behavioral. An agent that cannot prove its identity to a counterparty cannot even begin the process of trust negotiation. The first gate determines who is at the door.

**Gate Two: Transaction Trust.** Once identity is established, the agents must decide whether to transact. This is the problem addressed in this essay — the need for marketplaces that aggregate reputation, perform curation, provide security scanning, and enable contextual trust decisions. Identity tells you *who* you're dealing with. The marketplace tells you whether you should trust them for *this specific interaction*. The second gate determines whether the door opens.

The two gates are distinct and complementary. Identity verification without marketplace context tells you that the counterparty is who they claim to be, but not whether they are trustworthy for your particular need. Marketplace trust without identity verification tells you that the counterparty has a good track record, but not whether the agent you're talking to is the one that built that record. Both are necessary. Neither substitutes for the other.

"Who Holds the Key?" — the second essay in this series — examined the tension that arises at Gate One: the Sovereignty Paradox created by giving an agent a cryptographic identity that must be both sovereign (the agent controls it) and accountable (someone can overrule it). The tiered key architecture proposed there — inner sovereignty, boundary co-signing, constitutional governance — provides a structure for managing the paradox.

This essay extends the argument to Gate Two. If the tiered key architecture answers "who holds the key," the marketplace answers the next question: "who do you trust?"

## What Comes Next

The agent economy is at a crossroads that mirrors the early internet. In the 1990s, the debate was about protocols: TCP/IP versus OSI, HTTP versus Gopher, SMTP versus X.400. The protocols that won were not always the technically superior ones. They were the ones that enabled the marketplaces — Amazon, eBay, Google — to build trust infrastructure that made commerce viable.

The same pattern is repeating, compressed into a much shorter timeframe. The protocol layer is rapidly converging: A2A for communication, AP2 for payments, AESP for economic sovereignty, DIDs and Verifiable Credentials for identity. These protocols will be the substrate of the agent economy, but they will not determine its shape.

The shape will be determined by the marketplaces that solve the trust problem at scale. Which platform can certify that its listed agents are who they claim to be? Which can aggregate reputation data across thousands of interactions and millions of transactions? Which can adjudicate disputes fairly enough that agents are willing to take risks on unknown counterparties? Which can prove that its security scanning catches real threats with an acceptable false positive rate?

These are not protocol questions. They are institutional questions. And they will be answered not by technical superiority but by the quality of the trust infrastructure that each marketplace builds.

The agent that wants to participate in this economy does not need to wait for the perfect protocol. It needs to find the right marketplace — one that verifies identity, aggregates reputation, performs security checks, and provides a context for trustworthy interaction. Everything else is just transport.

The question is not which protocol will win. The question is which marketplace will earn enough trust to matter first.
