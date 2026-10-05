# Awesome-Endpoint-Detection-And-Response-EDR

# Awesome-Endpoint-Detection-And-Response-EDR



**Curated List of SaaS Products & Open-Source GitHub Projects**

*Focused on Endpoint Detection, Response Automation, Threat Hunting & Ransomware Rollback*

**Last updated: October 2026**



This repository tracks notable **SaaS platforms** and **open-source projects** for **Endpoint Detection and Response (EDR)**. These tools help security teams detect, investigate, and respond to threats on endpoints—from malware and ransomware to fileless attacks and lateral movement.



**Examples** include Microsoft Defender for Endpoint, CrowdStrike Falcon, SentinelOne Singularity, VMware Carbon Black, Trend Micro Vision One, Sophos Intercept X, Cybereason, Cynet 360, Palo Alto Cortex XDR, and Broadcom Symantec EDR (the category leaders).



**Open-source emphasis**: The open-source EDR ecosystem is **emerging and purpose-built for specific use cases**. **Warden** is an open-source EDR for Linux workstations written in Rust, with YARA scanning, quarantine management, and a hardened security model . **Kizashi** provides a self-hostable EDR for Windows endpoints with ETW-based process/network/registry monitoring and NATS JetStream response dispatch . **AEGIS** is an open-source autonomous platform with 12 Sigma rules covering the ransomware kill-chain, sub-300ms pipeline, and offline-capable AI triage . **Radegast EDR** brings end-to-end encrypted log storage using age encryption, with a Rust eBPF sensor for Linux and Windows . This section documents these focused solutions honestly.



## 📖 Table of Contents



- [☁️ SaaS/Hosted Platforms](#-saas-hosted-platforms)

- [🔓 Open-Source GitHub Projects](#-open-source-github-projects)

- [🤝 How to Contribute](#how-to-contribute)

- [⚠️ Disclaimer](#-disclaimer)



## ☁️ SaaS/Hosted Platforms



> **📊 Market Context**: The global EDR market is estimated at **~$8B in 2026**, growing toward **~$20B by 2032**. The sector is **moderately concentrated** — **CrowdStrike Falcon** leads with **22.68% market share** (13,432 customers) , followed by **Microsoft Defender for Endpoint** at **15.61%** and **SentinelOne** at **11.52%** . **Pricing varies dramatically**: CrowdStrike benchmarks at **$92/endpoint/year** for 1,000–2,499 endpoints (dropping to **$54** at 75,000+), while SentinelOne runs **10–18% below** CrowdStrike at equivalent tiers . **Microsoft Defender P2 is bundled with M365 E5**, with an allocated benchmark cost of **$42–$58/endpoint/year**—making it the most cost-effective option for Microsoft-centric organizations . No single vendor holds a winner-take-all position; enterprises typically run multi-vendor stacks.



| Platform | Description | Pricing (Starting Tier) | Free Tier Limits | Company Size |

|----------|-------------|------------------------|------------------|--------------|

| **[Microsoft Defender for Endpoint](https://www.microsoft.com/en-us/security/business/endpoint-security/microsoft-defender-endpoint)** | **Microsoft's native EDR.** Deep integration with Defender XDR, Intune, and Entra ID. **16% market share** . | **Included in Microsoft 365 E5** (marginal cost $0). **Standalone**: ~$4/user/month (Plan 2). **Allocated benchmark cost**: **$42–$58/endpoint/year** . | **No perpetual free tier**. **Microsoft 365 E5 trial** available (30 days). | **~$281B revenue (Microsoft FY2025)** |

| **[CrowdStrike Falcon](https://www.crowdstrike.com/)** | **The EDR market leader.** Cloud-native platform with threat intelligence, OverWatch managed hunting, and 23+ modules. **22.68% market share**, 13,432 customers . | **Falcon Enterprise**: **$92/endpoint/year** (1K–2.5K endpoints), **$54** (75K+) . **~$8.99/endpoint/month** . **Premium pricing, maximum negotiability** . | **No free tier**. **15-day free trial** available. | **~$4B revenue (FY2025)**, ~$16B market cap  |

| **[SentinelOne Singularity](https://www.sentinelone.com/)** | **Autonomous AI-powered EDR.** On-device AI with **ransomware rollback**—the strongest in the category. **11.52% market share** . | **Singularity Complete**: **$80/endpoint/year** (1K–2.5K), **$44** (75K+) . **~$6/endpoint/month** . **10–18% below CrowdStrike** at equivalent tiers . | **No free tier**. **Free trial** available. | **$821.5M revenue (FY2025)**  |

| **[VMware Carbon Black](https://www.vmware.com/products/carbon-black-cloud.html)** | **Broadcom-owned EDR.** Behavioral visibility and VMware integration. **Commercial uncertainty** post-Broadcom acquisition . | **Custom enterprise pricing**—quote required. **Pricing moved upward for mid-market** (5K–25K endpoints) while remaining competitive for large enterprise (100K+) . | **No free tier**. **Free trial** available. | **$209.7M revenue (FY2018)**  |

| **[Trend Micro Vision One](https://www.trendmicro.com/)** | **XDR platform with EDR.** Broad visibility across email, endpoint, cloud, and network. | **Custom enterprise pricing**—quote required. **List prices lower** than CrowdStrike/Trellix, less room to compress . | **No free tier**. **Free trial** available. | **~$1.8B revenue (Trend Micro FY2025)** |

| **[Sophos Intercept X](https://www.sophos.com/)** | **SMB-focused EDR with XDR.** Strong cloud visibility ratings (91% data discovery, 92% cloud registry) . | **Custom pricing**—quote required. | **Free trial** available. | **Private (~$700M+ revenue est.)** |

| **[Cybereason](https://www.cybereason.com/)** | **Defense-focused EDR.** Behavioral detection with attack timeline visualization. | **Custom enterprise pricing**—quote required. | **Free trial** available. | **Private (~$2.7B valuation est.)** |

| **[Cynet 360](https://www.cynet.com/)** | **Autonomous breach protection.** EDR + NDR + UEBA in one platform. | **Custom pricing**—quote required. | **Free trial** available. | **Private (~$100M+ raised)** |

| **[Palo Alto Cortex XDR](https://www.paloaltonetworks.com/cortex/cortex-xdr)** | **Palo Alto's XDR platform.** EDR + network + cloud telemetry correlation. | **Custom enterprise pricing**—quote required. | **Free trial** available. | **~$9.2B revenue (Palo Alto FY2025)** |

| **[Broadcom Symantec EDR](https://www.broadcom.com/)** | **Symantec's EDR.** Integrated with Broadcom's security portfolio. | **Custom enterprise pricing**—quote required. | **Free trial** available. | **~$51B revenue (Broadcom FY2025 est.)** |



## 🔓 Open-Source GitHub Projects



| Repo | Description | Stars |

|------|-------------|-------|

| **[Warden](https://github.com/Spellskite-coding/Warden)** — **Open-source EDR for Linux Workstations written in Rust.** **YARA scanning**, **ransomware fanotify monitors**, **quarantine with setuid-stripping**, **detection history**, **SHA-256-anchored exceptions**, and a **GTK4/libadwaita dashboard**. **Hardened through adversarial testing**: found and fixed package-manager spoofing, fork-per-file ransomware across directories, unprivileged auto-quarantine bypass, and TOCTOU issues. **Root daemon with systemd sandboxing** (`ProtectSystem=strict`, `NoNewPrivileges`, `RestrictAddressFamilies=AF_UNIX`) . | [![Stars](https://img.shields.io/github/stars/Spellskite-coding/Warden?style=social&color=white)](https://github.com/Spellskite-coding/Warden/stargazers) | ~500 |

| **[Kizashi](https://github.com/kizashi-labs/kizashi)** — **Self-hostable open-source EDR for Windows endpoints (AGPL-3.0).** **ETW sensor** capturing process, network, registry, DNS, auth, WMI, named pipes, and PowerShell events. **Network isolation** via console (`POST /agents/:id/isolate`) dispatched over NATS JetStream. **Rule-driven auto-remediation** gated behind `AUTO_ISOLATE_MIN_SEVERITY` (default 9). **Zero outbound traffic by default**—no telemetry, no alerts, no file contents uploaded. Agent ring-buffers events while offline and reconnects with exponential backoff . **Note**: Curated rule packs, stateful detectors (port-scan, DNS tunnelling, C2 correlation, ransomware burst), YARA scanning, and SigmaHQ sync are **commercial edition only** . | [![Stars](https://img.shields.io/github/stars/kizashi-labs/kizashi?style=social&color=white)](https://github.com/kizashi-labs/kizashi/stargazers) | ~200 |

| **[AEGIS](https://github.com/alejadxr/AEGIS)** — **Open-source autonomous cybersecurity platform with 11/11 detection score.** **Sub-300ms pipeline**, **honeypot deception**, **breadcrumb traps**, **AI-powered triage**, and **Rust endpoint agent**. **12 Sigma rules** cover the complete ransomware kill-chain: shadow delete (T1490), LOLBin certutil (T1105), rundll32 (T1218), SMB lateral movement (T1021.002), WinRM exec (T1021.006), RDP-then-encrypt (T1021.001 + T1486), mass extension change (T1486), canary tripped, ransom note detection, entropy spike, VSS inhibit, and backup delete. **RaaS threat intel feed** refreshed every 6 hours from RansomLook + CISA. **Fully offline-capable**: set `AEGIS_AI_MODE=disabled` for deterministic fallback across all AI call sites. **Runs on a Mac mini or Raspberry Pi** . | [![Stars](https://img.shields.io/github/stars/alejadxr/AEGIS?style=social&color=white)](https://github.com/alejadxr/AEGIS/stargazers) | ~100 |

| **[Radegast EDR](https://github.com/radegast-edr/radegast-backend)** — **Lightweight, privacy-respecting EDR platform with end-to-end encryption.** **age encryption** for log data—the server **cannot read** your logs even if compromised. **Rustinel eBPF sensor** for Linux and Windows. **Built-in SQLite database**—no external database server required. **Device management**, **configuration packs**, **team collaboration**, **email notifications**, and **single-command installation**. **Zero-trust architecture**: all data encrypted client-side, server never has access to private keys. **Docker/Podman deployment** with three named volumes (database, uploads, releases) . | [![Stars](https://img.shields.io/github/stars/radegast-edr/radegast-backend?style=social&color=white)](https://github.com/radegast-edr/radegast-backend/stargazers) | ~100 |



**Additional open-source options worth exploring:**



| Repo | Description |

|------|-------------|

| **[Wazuh](https://github.com/wazuh/wazuh)** — Open-source security platform with EDR capabilities. File integrity monitoring, log analysis, and active response. |

| **[Velociraptor](https://github.com/Velocidex/velociraptor)** — Endpoint visibility and forensic collection. Query endpoints with VQL for incident response. |

| **[Osquery](https://github.com/osquery/osquery)** — SQL-powered operating system instrumentation. Query endpoint state for detection and compliance. |

| **[GRR](https://github.com/google/grr)** — Google's remote live forensics framework. Rapid incident response at scale. |



## 🤝 How to Contribute



1. Fork the repo.

2. Add/edit entries in `README.md` (follow existing format).

3. Include: name, link, 1–2 sentence description, and whether it's SaaS or open-source.

4. Submit PR with a short explanation.



Star the repo if you find it useful!



## ⚠️ Disclaimer



- This is a **community-curated** list — not exhaustive and not an endorsement.

- EDR platforms handle sensitive endpoint telemetry and security data; ensure proper access controls and compliance with organizational security policies.

- **Open-source reality**: The open-source ecosystem for EDR is **emerging and purpose-built for specific use cases**. **Warden** provides a hardened Linux EDR with adversarial testing . **Kizashi** offers a self-hostable Windows EDR with ETW-based monitoring and NATS response dispatch . **AEGIS** delivers autonomous ransomware defense with offline-capable AI triage . **Radegast EDR** brings end-to-end encrypted log storage with a Rust eBPF sensor . However, **commercial platforms** (CrowdStrike Falcon, Microsoft Defender, SentinelOne) provide **massive cross-customer threat intelligence networks, managed threat hunting, and enterprise-scale response automation** that open-source alternatives cannot match. The open-source path is **genuinely viable** for **Linux workstations, homelabs, small teams, and privacy-focused deployments**.

- **Pricing caveat**: All pricing figures are **verified against cited search results** but may change without notice. **CrowdStrike benchmarks at $92/endpoint/year** for 1K–2.5K endpoints, dropping to **$54** at 75K+ . **SentinelOne runs 10–18% below CrowdStrike** at equivalent tiers . **Microsoft Defender P2 is bundled with M365 E5**, with an allocated cost of **$42–$58/endpoint/year** . **Always request a formal quote** — enterprise EDR pricing is heavily negotiable.



---



**Made for SOC analysts, incident responders, security engineers, and IT administrators.**

Let's make endpoint detection and response more open, transparent, and accessible.
