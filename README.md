# Mobile Email Client Security Analysis

This project investigates how mobile email clients handle various email deception techniques commonly used in phishing attacks. While these techniques are well-studied on desktop platforms, their presentation and effectiveness may differ significantly on mobile devices due to interface constraints and platform-specific implementations.

## Project Context

This research was conducted as part of the **"Praktikum Security, Usability and Society"** course at the Karlsruhe Institute of Technology (KIT), under the supervision of **Maxime Veit** and in collaboration with the **SECUSO research group** (Security, Usability, Society).

### Supervisor and Source Attribution

**Supervisor:** Maxime Veit, SECUSO Research Group, KIT

**Source Publications:**

- Maxime Fabian Veit, Oliver Wiese, Fabian Lucas Ballreich, Melanie Volkamer, Douglas Engels, & Peter Mayer (2025). *SoK: The past decade of user deception in emails and today's email clients' susceptibility to phishing techniques*. Computers & Security, 150, 104197.
- Maxime Fabian Veit (2025). *Additional Findings of User Deception in Emails – Research Note* [Unpublished manuscript].

**Research Contribution:** This work extends the existing desktop-focused research by creating EML test files for mobile-specific implementations and evaluating the susceptibility of popular mobile email clients to both established and novel deception techniques.

## Research Methodology

### Test Environment

The study evaluates **8 popular mobile email clients** across the two major mobile platforms:

**iOS Clients (4):**

- Apple Mail (Native iOS client)
- Gmail (Third-party alternative by Google)
- Microsoft Outlook (Third-party alternative by Microsoft)
- Proton Mail (Security-focused client)

**Android Clients (4):**

- Gmail (Native Android client)
- Samsung Mail (Native Samsung client)
- Microsoft Outlook (Third-party alternative by Microsoft)
- Proton Mail (Security-focused client)

### Evaluation Framework

Each technique was evaluated using a standardized framework adapted from Veit et al. (2025) with the following dimensions:

#### Information Display Quality

- `correct`: Technique properly mitigated, correct information displayed
- `misleading`: Technique successful, user sees deceptive information  
- `both`: Mixed results depending on context or user interaction
- `none`: No relevant information displayed

#### Client Assistance Level

- `none`: No security warnings or protective measures
- `warning`: Client displays security warnings to user
- `blocked`: Client actively blocks or filters the malicious content

#### User Interaction Requirements

- `no`: Technique effect visible without any user interaction
- `yes`: Requires user interaction to reveal full technique impact
- `yes_same`: Interaction reveals same (misleading) information
- `yes_misleading-first`: Initial view shows misleading information

#### Risk Assessment (Criticality Scale)

- `0`: **No Risk** - Completely blocked, no threat to user
- `1`: **Low Risk** - Correct information shown, may require user action
- `2`: **Medium Risk** - Mixed information display, moderate threat
- `4`: **High Risk** - Misleading information displayed, significant threat

## File Structure

```
EML-Files/
├── [01] EML_Files/              # Test email samples (.eml files)
├── [02] Screenshots/            # Visual documentation per technique
├── [03] Evaluation/             # Analysis results and data
└── README.md                    # This documentation
```

## Limitations and Future Work

### Study Limitations

- Limited to 8 email clients across 2 platforms
- Static analysis approach (no user behavior component)
- Snapshot evaluation (security posture may evolve)
- Focus on technical implementation rather than user perception

### Recommended Extensions

- **Broader Client Coverage**: Include additional regional/specialized email clients
- **User Studies**: Evaluate real-world user susceptibility to mobile phishing
- **Temporal Analysis**: Track security improvements over multiple client versions
- **Integration Testing**: Assess interaction with mobile OS security features

## Acknowledgments

Special thanks to:

- **Maxime Veit** (SECUSO, KIT) for supervision, methodology, and source technique development

This research extends and builds upon the foundational work in email deception techniques, adapting established methodologies for mobile platform evaluation.

---

*This research is conducted for educational and security improvement purposes. All testing was performed in controlled environments using researcher-owned devices and accounts. The findings are intended to improve mobile email security for all users.*
