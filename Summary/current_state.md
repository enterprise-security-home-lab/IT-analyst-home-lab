# Current Lab State

## Active Phase
Phase 22 — Suricata IDS deployed on pfSense OPT2/em3 with full Wazuh integration.
ET Open ruleset active with six categories. Live ET SCAN alerts validated end-to-end.

## Network — VMnet19 (DMZ)
Status: OPERATIONAL
Subnet: 10.10.30.0/24, Host-only
Dell host adapter: 10.10.30.2
pfSense OPT2/em3: 10.10.30.1
All endpoints reachable. Issue 51 resolved May 4, 2026.

## VM Status
- SRV-FW01 (pfSense): 10.10.10.1 — operational
- SRV-DC01 (Windows Server 2022): 10.10.10.133 — operational
- SRV-SIEM01 (Wazuh 4.7.5): 10.10.10.135 — operational
- SRV-DB01 (Ubuntu/MySQL): 10.10.10.128 — operational
- CLI-WIN11-01 (Windows 11): 10.10.20.134 — operational
- ATT-KALI01 (Kali): 10.10.30.130 — operational, primary attack source
- DMZ-VULN01 (Metasploitable 2): 10.10.30.101 — operational

## Primary Attack Source
ATT-KALI01 at 10.10.30.130. MacBook Kali deprecated — Cox gateway enforces
wireless client isolation with no UI toggle.

## Remaining Phase 22 Tasks
- Add custom Suricata rule for vsftpd port 6200 backdoor traffic
- Validate rule 100022 fires end-to-end
- Write IR-2026-004
- Update all documentation to v22
- Push to GitHub (on hold — not ready to push yet)