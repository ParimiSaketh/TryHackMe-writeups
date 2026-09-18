# Nmap Basics — Pre Security Path

## Objective
Understand how network scanning works and how `nmap` is used to discover live hosts, open ports, and running services on a network.

## Key Concepts
- **Host discovery** — identifying which IP addresses on a network are active before scanning them further.
- **Port scanning** — probing TCP/UDP ports to determine whether they are open, closed, or filtered.
- **Service/version detection** — fingerprinting what software is listening on an open port (e.g. Apache 2.4, OpenSSH 8.2) to help identify potential vulnerabilities later.
- **Scan types** — the difference between a full TCP connect scan (`-sT`) and a stealthier SYN scan (`-sS`), and why the latter is often preferred in real engagements.

## Approach
1. Started with a basic host discovery sweep to confirm the target was reachable.
2. Ran a default `nmap` scan against the target to get a quick picture of open ports.
3. Followed up with service/version detection flags to identify what was running behind each open port.
4. Cross-referenced identified service versions against known CVEs to understand the *why* behind a pentest scan, not just the *how*.

## What I Learned
Nmap output is only useful once you understand what each flag is actually doing under the hood — e.g. why a SYN scan is faster and stealthier than a full connect scan, and why version detection matters for building an attack surface picture. This room reinforced that reconnaissance is about building context, not just running a tool.

---
*Room: Pre Security path — TryHackMe*
