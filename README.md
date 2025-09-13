# Fake iPhone Scam — Investigation

**Case summary:** This repository documents an investigation into a fraudulent "free iPhone" giveaway funnel. The funnel impersonates brands and relies on multi-hop redirects, affiliate offer gating, and tracking fields to harvest user data and monetize traffic.

---

## Indicators & Verdict (short)
- **Verdict:** Tracking / information-harvesting scam funnel (not a legitimate brand promotion).
- **Primary bait domain observed:** `freeapple-gift.web.app`
- **Affiliate / redirect domains observed:** `fly.metozemoon.com`, `nl.prijzen-winnaar.com`, and related hosts.
- **Key risks:** personal data harvesting (names, phone numbers), potential premium-number or UPI/QR payment prompts, brand impersonation.

---

## Evidence overview
All forensic evidence (screenshots, network captures, HTML snapshots, and IOCs) were preserved in an evidence set for reporting and legal escalation. Evidence includes:
- Screenshots of landing pages and redirect chains
- Network capture (PCAP) showing DNS resolution and redirect timing
- Saved HTML snapshots and extracted IOCs (domains, IPs, phone numbers)
- WHOIS and nslookup digests used to identify hosting and name servers

> Note: raw evidence has been preserved offline and is available on request to takedown contacts; it is not published publicly in this repository to avoid leaking sensitive data.

---

## Investigation highlights
- The funnel required visitors to complete third-party offers as a “human verification” step to claim the prize.
- HTML analysis revealed large numbers of hidden tracking inputs and affiliate parameters (`variant`, `subaccount`, `offer_id`, etc.).
- DNS/WHOIS checks showed the domain(s) using AWS name servers and multi-cloud infrastructure (AWS + Google/Firebase) across the redirect chain.
- OSINT checks (community reports, domain reputation scans) corroborated suspicious activity for several domains in the chain.

---

## How this repo is organized (suggested)
- `README.md` — overview and verdict (this file)
- `IOC.md` — short machine-readable list of observed indicators (domains, IPs)
- `Methodology.md` — detailed steps and OPSEC guidance
- `REPORT_TEMPLATE.md` — copy-ready takedown/report email templates
- `TAKEDOWN.md` — tracker for report submissions and responses
- `Evidence/` — (private) preserved artifacts for legal/takedown use
- `Analysis/` — detailed domain reports and infra mapping

---

## Summary statement
This investigation confirms the operation is a scam funnel whose goal is to harvest user information and extract affiliate revenue. Use the preserved evidence for reporting and coordinate takedown across hosting providers and brand owners.

**Investigator:** Leroy Anand — Cyber Security Practitioner
