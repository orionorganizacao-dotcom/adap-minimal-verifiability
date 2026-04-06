# A-DAP — Minimal Verifiability Protocol

A-DAP (Algorithmic Decision Auditability Protocol) defines a minimal architecture for **external verifiability of algorithmic decisions**.

It does not aim to explain decisions.

It ensures that decisions can be:
- reconstructed
- independently verified
- contested outside the system that produced them

---

## Core Principle

A decision is only auditably valid if it can be verified outside the system that generated it.

---

## The Problem

Modern AI systems can:

- generate structured outputs
- produce convincing justifications
- simulate technical authority

Without providing:

- external traceability
- independent verification
- reconstructable decision paths

This creates a structural condition:

**the system decides, records, explains, and validates itself.**

---

## What A-DAP Provides

A minimal structure to ensure:

- tamper-evident decision logs
- external timestamping
- independent verification
- separation between execution and validation

---

## Minimal Event Structure

```json
{
  "event_id": "uuid",
  "timestamp_external": "RFC3339",
  "input_hash": "sha256",
  "output_hash": "sha256",
  "model_id": "string",
  "model_version": "string",
  "parameters": {},
  "policy_id": "string",
  "chain_hash": "sha256",
  "signature": "ed25519"
}
