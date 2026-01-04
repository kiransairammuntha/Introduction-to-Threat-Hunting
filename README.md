<p align="center">
  <img src="https://img.shields.io/badge/Security_Blue_Team-Threat_Hunting-00CED1?style=for-the-badge" alt="Security Blue Team">
</p>

<h1 align="center">🎯 Introduction to Threat Hunting</h1>

<p align="center">
  <img src="https://img.shields.io/badge/Security_Blue_Team-Certified-0078D4?style=flat" alt="SBT">
  <img src="https://img.shields.io/badge/Redline-Endpoint_Analysis-red?style=flat" alt="Redline">
  <img src="https://img.shields.io/badge/IOC_Editor-Indicator_Creation-orange?style=flat" alt="IOC Editor">
  <img src="https://img.shields.io/badge/PowerShell-Scripting-blue?style=flat&logo=powershell" alt="PowerShell">
  <img src="https://img.shields.io/badge/Status-Completed-success.svg" alt="Status">
</p>

<p align="center">
  <i>Proactive threat hunting training covering IOC collection, correlation, and malware detection using Mandiant Redline, IOC Editor, and PowerShell.</i>
</p>

---

## 🎯 Project Aim

> **"Threat hunters don't wait for alerts — they find the attackers hiding in the shadows."**

While SOC analysts respond to alerts, **threat hunters proactively search** for adversaries that evade detection. This certification demonstrates:

🔍 **Proactive Hunting Skills** — Finding threats before they trigger alerts

🦠 **Real Malware Detection** — Hunting for actual malware using industry tools

📋 **IOC Mastery** — Collecting, correlating, and operationalizing Indicators of Compromise

🛠️ **Professional Toolchain** — Mandiant Redline, IOC Editor, PowerShell for endpoint analysis

🎯 **Structured Methodology** — Repeatable threat hunting procedures from intel to report

This is **hands-on threat hunting** — not theory, but actual malware detection using the same tools used by enterprise security teams.

---

## 📑 Table of Contents

- [🔍 Overview](#-overview)
- [✨ Course Modules](#-course-modules)
- [🏗️ Threat Hunting Workflow](#️-threat-hunting-workflow)
- [🛠️ Tools & Technologies](#️-tools--technologies)
- [⚔️ Attacks & Techniques Detected](#️-attacks--techniques-detected)
- [🎓 Skills Demonstrated](#-skills-demonstrated)
- [🏆 Project Achievements](#-project-achievements)
- [📊 Key Metrics & Performance](#-key-metrics--performance)
- [🙏 Acknowledgments](#-acknowledgments)
- [🎬 Project Summary](#-project-summary)
- [📞 Contact & Support](#-contact--support)
- [📊 Project Stats](#-project-stats)

---

## 🔍 Overview

The **Introduction to Threat Hunting** certification from Security Blue Team trains you to proactively hunt for advanced threats using industry-standard tools and methodologies.

| Component | Description |
|-----------|-------------|
| **Provider** | Security Blue Team (SBT) |
| **Duration** | ~5 hours |
| **Level** | Beginner |
| **Focus** | IOC-based threat hunting |
| **Certification ID** | 277761690 |
| **Date Passed** | February 19, 2025 |

> ### 💡 Why Threat Hunting?
> 
> **Threat hunting is proactive detection** — finding attacker activity even when no alert has fired. Unlike reactive SOC alert triage:
> - Hunters **assume breach** and search for evidence
> - Hunters find threats that **bypass automated detection**
> - Hunters reduce **dwell time** from months to hours
> 
> Organizations with mature threat hunting programs detect breaches **67% faster** than those without.

---

## ✨ Course Modules

### Module 1: Foundations — What Threat Hunting Is

| Topic | What You Learn |
|-------|----------------|
| **Proactive vs Reactive** | Hunting vs SOC alert triage differences |
| **IOC-led Hunting** | Evidence/artifacts left behind by attackers |
| **IOA-led Detection** | Behavior/intent-based detection approach |
| **Hunting Lifecycle** | Intel → Hunt → Validate → Report cycle |
| **IOC Context** | IOCs are not signatures — require human analysis |

**Key Distinction:**
| Approach | Focus | Example |
|----------|-------|---------|
| **IOC (Indicator of Compromise)** | Post-compromise artifacts | File hash, IP address, registry key |
| **IOA (Indicator of Attack)** | Attacker behavior/intent | Credential dumping, lateral movement |

---

### Module 2: Generating Indicators

**Purpose:** Extract indicators from malicious files and build structured IOC documents.

| Skill | Implementation |
|-------|----------------|
| **Hash Extraction** | PowerShell Get-FileHash (SHA256/MD5) |
| **File Attributes** | Name, extension, size, path |
| **String Analysis** | Extracting suspicious strings |
| **IOC Creation** | Building OpenIOC XML documents |

**Hands-On Activities:**
- ✅ Extract file hashes using PowerShell
- ✅ Identify malicious file attributes
- ✅ Create IOC files in IOC Editor
- ✅ Build logical IOC structures (AND/OR logic)
- ✅ Add metadata (description, labels, author)

**PowerShell Hash Extraction:**
```powershell
# Generate SHA256 hash of suspicious file
Get-FileHash -Path "C:\suspect\malware.exe" -Algorithm SHA256
```

---

### Module 3: Malware Hunting

**Purpose:** Execute IOC-based hunts on endpoints using Redline.

| Phase | Activity |
|-------|----------|
| **Collector Creation** | Build IOC Search Collector in Redline |
| **Deployment** | Run collector on target system |
| **Data Import** | Import results into Redline |
| **Analysis** | Review IOC reports and matches |
| **Validation** | Confirm true positives vs false positives |

**Redline Hunt Workflow:**
1. Load IOC files into Redline
2. Create IOC Search Collector
3. Deploy collector on target endpoint
4. Import collected data
5. Analyze IOC Report hits
6. Investigate matched artifacts

---

### Module 4: Course Capstone

**Purpose:** End-to-end threat hunting scenario with real malware.

| Deliverable | Description |
|-------------|-------------|
| **IOC Pack** | Complete .ioc files for malware |
| **Collector Output** | Redline collection results |
| **IOC Report** | HTML report with hits |
| **Written Summary** | Findings and recommendations |

**Capstone Challenge:**
- Given malware samples/intel
- Extract all relevant IOCs
- Create structured IOC files
- Execute Redline hunt
- Document findings and next steps

---

## 🏗️ Threat Hunting Workflow

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                        THREAT HUNTING METHODOLOGY                           │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                             │
│   ┌─────────────┐    ┌─────────────┐    ┌─────────────┐    ┌─────────────┐ │
│   │   PHASE 1   │    │   PHASE 2   │    │   PHASE 3   │    │   PHASE 4   │ │
│   │   DEFINE    │───►│   COLLECT   │───►│    BUILD    │───►│   EXECUTE   │ │
│   │  OBJECTIVE  │    │ INDICATORS  │    │  IOC LOGIC  │    │    HUNT     │ │
│   └─────────────┘    └─────────────┘    └─────────────┘    └─────────────┘ │
│         │                  │                  │                  │         │
│         ▼                  ▼                  ▼                  ▼         │
│   ┌─────────────┐    ┌─────────────┐    ┌─────────────┐    ┌─────────────┐ │
│   │ • Threat    │    │ • File hash │    │ • IOC Editor│    │ • Redline   │ │
│   │   intel     │    │ • File name │    │ • OpenIOC   │    │ • IOC Search│ │
│   │ • Malware   │    │ • File size │    │   format    │    │   Collector │ │
│   │   sample    │    │ • Strings   │    │ • AND/OR    │    │ • Deploy    │ │
│   │ • Hunt goal │    │ • Registry  │    │   logic     │    │ • Import    │ │
│   └─────────────┘    └─────────────┘    └─────────────┘    └─────────────┘ │
│                                                                             │
│   ┌─────────────┐    ┌─────────────┐                                       │
│   │   PHASE 5   │    │   PHASE 6   │                                       │
│   │  VALIDATE   │───►│   REPORT    │                                       │
│   │   & TRIAGE  │    │  & RESPOND  │                                       │
│   └─────────────┘    └─────────────┘                                       │
│         │                  │                                               │
│         ▼                  ▼                                               │
│   ┌─────────────┐    ┌─────────────┐                                       │
│   │ • Confirm   │    │ • IOC Report│                                       │
│   │   hits      │    │ • Findings  │                                       │
│   │ • Context   │    │   summary   │                                       │
│   │ • True vs   │    │ • Next steps│                                       │
│   │   false pos │    │ • Contain   │                                       │
│   └─────────────┘    └─────────────┘                                       │
│                                                                             │
└─────────────────────────────────────────────────────────────────────────────┘
```

---

## 🛠️ Tools & Technologies

### Core Toolchain

| Tool | Purpose | What You Learn |
|------|---------|----------------|
| **Mandiant Redline** | Endpoint investigation & IOC hunting | Collector creation, data import, IOC reports |
| **Mandiant IOC Editor** | IOC authoring & management | OpenIOC format, logical structures, metadata |
| **PowerShell** | File triage & hash extraction | Get-FileHash, file attribute collection |

### Redline Capabilities

| Feature | Description |
|---------|-------------|
| **Standard Collector** | Basic endpoint data collection |
| **Comprehensive Collector** | Full forensic data acquisition |
| **IOC Search Collector** | Targeted IOC-based hunting |
| **IOC Reports** | Interactive HTML hit reports |

### IOC Editor Features

| Feature | Description |
|---------|-------------|
| **OpenIOC Format** | Standardized XML indicator format |
| **Logical Operators** | AND/OR logic for complex indicators |
| **Term Library** | File, registry, memory artifact terms |
| **XPath Export** | Filter generation for hunt tools |
| **Metadata** | Author, description, labels |

### Indicator Types

| IOC Type | Example | Detection Use |
|----------|---------|---------------|
| **File Hash** | SHA256, MD5 | Known malware identification |
| **File Name** | evil.exe, payload.dll | Suspicious file detection |
| **File Size** | Exact byte count | Artifact correlation |
| **File Path** | C:\Users\Public\ | Common malware locations |
| **Registry Key** | Run keys, services | Persistence detection |

---

## ⚔️ Attacks & Techniques Detected

### Malware Artifacts Hunted

| Artifact Type | MITRE ATT&CK | Detection Method |
|---------------|--------------|------------------|
| **Scheduled Tasks** | T1053.005 | Registry/file IOCs |
| **Registry Run Keys** | T1547.001 | Registry term IOCs |
| **Startup Folder** | T1547.001 | File path IOCs |
| **Dropped Binaries** | T1105 | File hash IOCs |
| **Renamed Executables** | T1036.003 | File attribute IOCs |

### MITRE ATT&CK Coverage

| Tactic | Techniques Detected |
|--------|---------------------|
| **Persistence** | Registry Run Keys, Scheduled Tasks, Startup Folder |
| **Execution** | Malicious file execution artifacts |
| **Defense Evasion** | Renamed/masqueraded files |
| **Command & Control** | Known malware hashes/indicators |

### IOC vs IOA Detection

| Approach | Strength | This Course Focus |
|----------|----------|-------------------|
| **IOC Hunting** | Known-bad artifact discovery | ✅ Primary focus |
| **IOA Detection** | Behavior/intent identification | Conceptual introduction |

---

## 🎓 Skills Demonstrated

### Technical Skills
- 🔍 **Threat Hunting** — Proactive threat detection methodology
- 🦠 **Malware Analysis** — Extracting indicators from malicious files
- 📋 **IOC Creation** — Building OpenIOC-format indicator files
- 🛠️ **Redline Proficiency** — IOC Search Collector deployment and analysis
- 💻 **PowerShell** — File hashing and triage scripting
- 📊 **Report Generation** — IOC reports and findings documentation

### Security Knowledge
- 🎯 **IOC vs IOA** — Understanding indicator types and applications
- 🔗 **MITRE ATT&CK** — Mapping artifacts to attack techniques
- 🏹 **Hunt Methodology** — Intel → Hunt → Validate → Report lifecycle
- 🚫 **False Positive Handling** — Validating and triaging hunt results
- 📈 **Threat Intelligence** — Operationalizing intel into hunts

### Professional Competencies
- 📝 **Documentation** — Hunt findings and recommendations
- 🔄 **Repeatable Procedures** — Standardized hunting workflows
- 🎓 **Tool Mastery** — Industry-standard Mandiant toolchain
- 🧪 **Hands-On Experience** — Real malware hunting scenarios
- 🗣️ **Communication** — Reporting findings to stakeholders

---

## 🏆 Project Achievements

### What This Project Demonstrates
- ✅ Completed Security Blue Team threat hunting certification
- ✅ Extracted IOCs from real malware samples
- ✅ Created structured OpenIOC indicator files
- ✅ Executed endpoint hunts using Mandiant Redline
- ✅ Generated IOC reports documenting malware presence
- ✅ Applied proactive threat hunting methodology
- ✅ Completed capstone challenge with real-world scenario

### Business Value
- 🔍 **Proactive Defense** — Find threats before they cause damage
- ⏱️ **Reduced Dwell Time** — Detect breaches faster
- 🛡️ **Defense in Depth** — Complement automated detection
- 📈 **Mature Security Posture** — Threat hunting capability
- ✅ **Industry Recognition** — Security Blue Team certification

---

## 📊 Key Metrics & Performance

### Training Coverage

| Metric | Value |
|--------|-------|
| **Course Duration** | ~5 hours |
| **Modules Completed** | 4 (Foundations, Indicators, Hunting, Capstone) |
| **Tools Mastered** | Redline, IOC Editor, PowerShell |
| **IOC Types** | File hash, name, size, path, registry |
| **Hunt Methodology** | 6-phase structured workflow |
| **Capstone** | End-to-end malware hunt |

### Threat Hunting Capabilities

| Capability | Proficiency |
|------------|-------------|
| 📋 IOC Extraction | ✅ Job-Ready |
| 🛠️ IOC Editor Usage | ✅ Job-Ready |
| 🔍 Redline Hunting | ✅ Job-Ready |
| 📊 Report Generation | ✅ Job-Ready |
| 🦠 Malware Detection | ✅ Job-Ready |
| 🔄 Hunt Methodology | ✅ Job-Ready |

---

## 🙏 Acknowledgments

**Training Provider:**
- [Security Blue Team](https://www.securityblue.team/) — Certification and training

**Tool Developers:**
- [Mandiant/FireEye](https://www.mandiant.com/) — Redline and IOC Editor
- [Microsoft](https://microsoft.com/) — PowerShell

**Frameworks & Standards:**
- [OpenIOC](https://github.com/mandiant/OpenIOC_1.1) — Indicator format standard
- [MITRE ATT&CK](https://attack.mitre.org/) — Threat technique framework

**Security Community:**
- Threat hunting best practices
- Blue team defender methodologies
- Malware analysis techniques

---

## 🎬 Project Summary

This Introduction to Threat Hunting certification represents **hands-on proactive threat detection training** that combines:

✅ **Threat Hunting Methodology** (Intel → Hunt → Validate → Report)
✅ **IOC Extraction** (File hashes, attributes, registry keys)
✅ **IOC Creation** (OpenIOC format with IOC Editor)
✅ **Endpoint Hunting** (Mandiant Redline IOC Search Collector)
✅ **Real Malware Detection** (Capstone with actual malware)
✅ **Professional Reporting** (IOC reports and documentation)

**Demonstrates:**
- Proactive threat hunting skills
- Industry-standard tool proficiency
- Malware analysis fundamentals
- IOC creation and management
- Structured hunting methodology

**Delivers:**
- Threat hunter capabilities
- Hands-on malware detection experience
- Industry-recognized certification
- Practical blue team skills
- Career advancement foundation

**Perfect For:**
- Threat Hunter roles
- SOC Analyst advancement
- Incident Response positions
- Blue Team careers
- Security Operations roles

---

## 📞 Contact & Support

- **Project Repository**: https://github.com/kiransairammuntha/Introduction-to-Threat-Hunting
- **Issues**: https://github.com/kiransairammuntha/Introduction-to-Threat-Hunting/issues
- **Discussions**: https://github.com/kiransairammuntha/Introduction-to-Threat-Hunting/discussions

---

## 📊 Project Stats

![GitHub stars](https://img.shields.io/github/stars/kiransairammuntha/Introduction-to-Threat-Hunting?style=social)
![GitHub forks](https://img.shields.io/github/forks/kiransairammuntha/Introduction-to-Threat-Hunting?style=social)
![GitHub issues](https://img.shields.io/github/issues/kiransairammuntha/Introduction-to-Threat-Hunting)
![GitHub pull requests](https://img.shields.io/github/issues-pr/kiransairammuntha/Introduction-to-Threat-Hunting)

---

<div align="center">

**Built with ❤️ for Threat Hunters**

**Hunt. Detect. Validate. Report.**

**Proactive Defense • Real Malware • Industry Tools**

[⬆ Back to Top](#-introduction-to-threat-hunting)

</div>
