# CompTIA-Security-X-Trainer
CompTIA SecurityX CAS-005 Exam Trainer: A self-contained, browser-based exam trainer for the CompTIA SecurityX certification, CompTIA Advanced Security Practitioner (formerly CASP+), exam code CAS-005. Built as a single HTML file with 180 questions mapped to the official CompTIA exam objectives, three study modes, and persistent progress tracking.

 CompTIA SecurityX CAS-005 Exam Trainer

A self-contained, browser-based exam trainer for the **CompTIA SecurityX** certification, *CompTIA Advanced Security Practitioner (formerly CASP+), exam code CAS-005*.

Built as a single HTML file with **180 questions** mapped to the official CompTIA exam objectives, three study modes, persistent progress tracking, and a dark security-themed interface.

---

## Features

- **268 questions** across all 4 official exam domains, weighted to match the real exam
- **Three modes:**
  - **Study** — answer-by-answer with explanations revealed immediately
  - **Practice** — pick a domain and question count, scored at the end
  - **Exam Sim** — 90 questions, 165-minute timer, quick-jump grid, flag-for-review
- **Persistent progress tracking** — scores, per-domain accuracy, and session history saved to `localStorage`
- **Weak-area mode** — prioritizes questions you've previously missed or haven't seen yet
- **Randomized answer positions** — Fisher-Yates shuffle on every question draw ensures correct answers spread evenly across A/B/C/D (no positional guessing)
- **Detailed explanations** for every question
- **Dark theme** — designed for long study sessions
- **No installation, no dependencies** — opens in any modern browser

---

## Question Distribution

| Domain | Weight | Questions |
|---|---|---|
| Governance, Risk, and Compliance | 20% | 55 |
| Security Architecture | 27% | 73 |
| Security Engineering | 31% | 83 |
| Security Operations | 22% | 57 |
| **Total** | **100%** | **268** |

### Topics Covered

- **Governance, Risk, and Compliance** — NIST RMF (SP 800-37), ISO 27001/27002, NIST CSF 2.0, risk quantification (ALE/SLE/ARO), GDPR/HIPAA/SOX/PCI-DSS/FedRAMP, third-party/supply-chain risk, AI risk management (NIST AI RMF), data classification, BCP/DR, SOC 2, tabletop exercises

- **Security Architecture** — Zero Trust Architecture (NIST 800-207), SASE/SSE, CASB, ZTNA, micro-segmentation, IaaS/PaaS/SaaS shared responsibility, IaC security, Kubernetes & container architecture, IdP/SAML/OIDC/OAuth, secrets management, post-quantum cryptography, TLS 1.3, certificate pinning, SBOM/SLSA, LLM/AI security, service mesh, API gateways, immutable infrastructure

- **Security Engineering** — AES modes (GCM/CCM/CBC/ECB), Argon2/bcrypt/scrypt, AD attacks (Kerberoasting, Golden Ticket, Pass-the-Hash), Credential Guard, TLS interception, DNSSEC/DoH/DoT, SPF/DKIM/DMARC, application allowlisting (WDAC/AppLocker), container hardening (seccomp/AppArmor), OWASP Top 10 mitigations, cloud IAM hardening, WPA3-Enterprise/802.1X, NGFW App-ID, TPM/Secure Boot, anti-fileless defenses

- **Security Operations** — NIST SP 800-61 lifecycle, SOAR playbooks, MITRE ATT&CK, threat hunting, IOA vs IOC, Sysmon event analysis, LOLBin detection, deception technology, MTTD/MTTR, EPSS + KEV vulnerability prioritization, purple teaming, YARA, cloud detection (CloudTrail/GuardDuty), MDR/XDR, detection-as-code

---

## Usage

### Quick Start

1. Download `securityx-exam-trainer.html`
2. Double-click to open in your browser
3. Start training

No build step, no server, no dependencies.

### Recommended Study Path

1. **Week 1:** Run **Study Mode** through GRC and Architecture to build conceptual foundation
2. **Week 2:** Study Mode through Engineering and Operations — these carry the most exam weight (53% combined)
3. **Week 3:** Switch to **Practice Mode** with 25–50 questions per session, focusing on weaker domains
4. **Week 4:** Take 1–2 full **Exam Sim** runs (90 questions, 165 min) to build pacing and stamina
5. **Final review:** Use the **weak-areas** toggle to drill missed questions until consistent

The dashboard flags `EXAM_READY` once your overall accuracy hits 75%. Note: SecurityX is pass/fail with no published scaled score, so this is a conservative readiness target — aim higher in practice.

---

## Technical Notes

- **Single HTML file** — all CSS, JavaScript, and questions embedded
- **Storage** — uses `localStorage` for persistence; data stays on your device
- **Privacy** — no analytics, no network calls, no telemetry
- **Browser support** — any modern browser (Chrome, Firefox, Edge, Safari)
- **Mobile** — responsive layout works on phones and tablets

### Resetting Progress

Click **ANALYTICS → RESET ALL PROGRESS** to clear all saved scores and session history.

---

## Disclaimer

This trainer is an **independent study aid** and is not affiliated with, endorsed by, or sponsored by CompTIA. CompTIA®, SecurityX®, and CASP+® are trademarks of the Computing Technology Industry Association.

Questions are written to align with the publicly published CAS-005 exam objectives and are intended to reinforce understanding of the exam topics. They are **not real exam questions** and passing this trainer does not guarantee passing the certification exam.

The real SecurityX exam includes **performance-based questions (PBQs)** that this trainer does not simulate. Supplement with hands-on labs (CompTIA CertMaster Labs, cloud sandboxes, home VM lab) to build the practical skills PBQs require.

---

## License

MIT

---

## Contributing

Spot a question that needs correction or want to add more? Open an issue or pull request. Each question entry follows a simple structure:

```js
{
  id: 181,
  domain: "ENG",    // GRC | ARC | ENG | OPS
  q: "Question text...",
  choices: ["Option A", "Option B", "Option C", "Option D"],
  a: 1,             // index of correct answer (0-3) — will be shuffled at runtime
  exp: "Explanation of why this is correct."
}
```

---

**Good luck on your exam.**
