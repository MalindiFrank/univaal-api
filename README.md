# UniVaal API (Backend)

UniVaal is a production e-commerce platform serving university students in the Vaal region of South Africa.  
This repository contains the backend API for the UniVaal MVP, built to production standards and designed to scale cleanly over time.

---

## What This Service Does (MVP Scope)

- Exposes the public product catalog (including product images and category)
- Supports cart and checkout flow
- Handles payment confirmation
- Creates orders and manages basic order status flow
- Provides API-level admin capabilities for product and image management
- Publishes a formal OpenAPI specification as the source of truth for integration

Out of scope for the current MVP:
- Inventory management and fulfillment domain
- Delivery tracking domain
- Operations/admin domain beyond MVP-level product/image management

---

## Architectural Approach

- **Design approach:** Domain-Driven Design (DDD)
- **API strategy:** API-first development
- **Specification:** OpenAPI is treated as the contract and integration reference
- **Goal:** predictable behavior, clean boundaries, and maintainable evolution

---

## Tech Stack

- **Language:** Java
- **Database:** PostgreSQL
- **API Style:** REST (OpenAPI-driven)

---

## Repository Structure (DDD-Oriented)

This codebase is structured to keep domain boundaries explicit and avoid mixing concerns:

- `domain/` — core business models and rules
- `application/` — use-cases and orchestration
- `infrastructure/` — persistence, integrations, external systems

Note: folder naming may vary, but the intent remains the same: domains stay clean and independent.

---

## API Contract

The OpenAPI specification in this repo is the integration contract for UniVaal.  
Frontend and other consumers should align to the spec and treat changes as versioned, reviewed contract updates.

---

## Status

This backend is an actively developed production MVP.  
Changes are expected, but the system is being built with long-term stability and maintainability in mind.
