# Web Application Security — Penetration Testing PoC

> ⚠️ **Disclaimer:** All testing was performed exclusively on intentionally vulnerable applications and controlled lab environments (PortSwigger Web Security Academy, Acunetix testphp.vulnweb.com). No real systems were harmed. Do not replicate against any system without explicit written permission.

## Overview

A four-part Proof of Concept (PoC) series demonstrating real-world web application attack techniques. Submitted as the Capstone Project for the **Certified Ethical Hacker (CSEH)** programme at Boston Institute of Analytics (Aug 2025).

Each topic covers the full offensive lifecycle — reconnaissance, exploitation, evidence collection, and remediation recommendations.

## Topics Covered

| # | Attack Type | Target Platform | Technique |
|---|---|---|---|
| 1 | Session Hijacking | Adafruit (live e-commerce) | Cookie replay attack |
| 2 | Session Fixation | Acunetix testphp.vulnweb.com | Pre-auth session token reuse |
| 3 | Stored XSS + Cookie Theft | PortSwigger Web Security Academy | Script injection via Burp Collaborator |
| 4 | CSRF | PortSwigger Web Security Academy | Forged state-changing HTML form |

## Topic Summaries

### Topic 1 — Session Hijacking via Cookie Replay
Demonstrated that possession of a valid session cookie is sufficient to fully impersonate an authenticated user on a live e-commerce platform. Analysed absence of IP binding, user-agent binding, and step-up re-authentication controls.

### Topic 2 — Session Fixation
Demonstrated failure to regenerate session ID post-authentication on a vulnerable test application, allowing a pre-planted session token to be reused after victim login to gain unauthorised access.

### Topic 3 — Stored XSS & Session Cookie Theft
Injected a malicious JavaScript payload into a blog comment field on a PortSwigger lab. Exfiltrated HttpOnly-unprotected session cookies via Burp Collaborator server, then replayed the stolen session to fully impersonate the victim.

### Topic 4 — Cross-Site Request Forgery (CSRF)
Crafted a forged HTML form exploiting absent CSRF token validation to execute unauthorised account actions on behalf of an authenticated victim — without stealing credentials or session cookies.

## Tools Used

- Burp Suite (Proxy, Repeater, Collaborator)
- Browser Developer Tools
- PortSwigger Web Security Academy Labs
- Acunetix Vulnerable Web Application

## Key Concepts Demonstrated

- OWASP Top 10 — A07 (Identification & Authentication Failures), A03 (Injection), A01 (Broken Access Control)
- Session management vulnerabilities
- Client-side attack techniques
- Cookie security flags (HttpOnly, Secure, SameSite)
- CSRF token validation
- Offensive documentation to professional pentest report standard

## Repository Structure
```
web-app-security-poc/
│
├── Topic-1-Session-Hijacking/
│   ├── Session_Hijacking_PoC.docx
│   └── Screenshots/
│
├── Topic-2-Session-Fixation/
│   ├── Session_Fixation_PoC.docx
│   └── Screenshots/
│
├── Topic-3-XSS-Cookie-Theft/
│   ├── XSS_PoC.docx
│   ├── Scripts/
│   └── Screenshots/
│
├── Topic-4-CSRF/
│   ├── CSRF_PoC.docx
│   ├── Scripts/
│   └── Screenshots/
│
└── README.md
```

## Author

**Omkar Sawant** — Cybersecurity Analyst & Ethical Hacker
[LinkedIn](https://www.linkedin.com/in/omkarsawant94) · [GitHub](https://github.com/omkarsawant94)
