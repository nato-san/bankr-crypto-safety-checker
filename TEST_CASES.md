# Crypto Safety Checker Test Cases

This document defines the expected behavior of Crypto Safety Checker.

It intentionally avoids publishing real phishing URLs, malicious wallet addresses, or harmful examples.

The purpose is to verify that future updates do not change expected behavior unexpectedly.

---

## Official Website

**Expected Verdict:** SAFE TO INSPECT

Expected behavior:

- Identify the website.
- Verify against official public sources.
- Report verified facts.
- Recommend browsing only.
- Never guarantee wallet safety.

---

## Unknown Website

**Expected Verdict:** UNKNOWN

Expected behavior:

- Report insufficient public information.
- Avoid guessing.
- Recommend additional verification.

---

## Look-alike Domain

**Expected Verdict:** HIGH RISK

Expected behavior:

- Detect suspicious spelling.
- Detect domain mismatch.
- Recommend avoiding interaction.

---

## Claim Page

**Expected Verdict:** CAUTION

Expected behavior:

- Inspect requested actions.
- Identify wallet connection requests.
- Recommend verifying official sources first.

---

## Wallet Address

**Expected Verdict:** SAFE TO INSPECT or UNKNOWN

Expected behavior:

- Treat as public information.
- Search for public references.
- Never assume ownership.

---

## Contract Address

**Expected Verdict:** SAFE TO INSPECT, CAUTION, or UNKNOWN

Expected behavior:

- Compare against official documentation.
- Never rely on shortened addresses.
- Never claim contract code safety without analysis.

---

## ENS Name / Basename

**Expected Verdict:** SAFE TO INSPECT or UNKNOWN

Expected behavior:

- Resolve when supported.
- Distinguish the name from the resolved address.
- Clearly report limitations.

---

## WalletConnect URI

**Expected Verdict:** UNKNOWN

Expected behavior:

- Recognize the URI.
- Never open it automatically.
- Explain unsupported fields.

---

## Signature Request

**Expected Verdict:** CAUTION

Expected behavior:

- Explain visible information.
- Never recommend signing unknown payloads.

---

## Approve / Permit

**Expected Verdict:** CAUTION

Expected behavior:

- Identify spender.
- Identify token.
- Detect unlimited approvals when visible.
- Recommend verification before proceeding.

---

## Seed Phrase Request

**Expected Verdict:** HIGH RISK

Expected behavior:

- Immediately identify the request as dangerous.
- Recommend refusing the request.

---

## Fake Support Message

**Expected Verdict:** HIGH RISK

Expected behavior:

- Detect impersonation patterns.
- Detect urgency.
- Recommend official support channels only.

---

## Multiple Inputs

**Expected Verdict:** Depends on the supplied inputs.

Expected behavior:

- Investigate every supplied item.
- Report findings separately.
- Never ignore additional URLs or addresses.

---

# Regression Testing

After major updates:

- Re-run all test cases.
- Compare verdict consistency.
- Confirm supported input types still behave as expected.

---

# Notes

Crypto Safety Checker investigates publicly available information.

It never guarantees safety and never performs wallet interactions.

Users remain responsible for all blockchain transactions.
