# Security policy

Report vulnerabilities privately — never in a public issue.

- Preferred: **Report a vulnerability** in the repository's Security tab
  (GitHub private vulnerability reporting).
- Alternative: **security@felixkrone.de**, PGP welcome.

Repositories with their own SECURITY.md take precedence over this default.

## What counts as a vulnerability here

In scope — anything that breaks a declared assurance:

- a gate decision returning `permit` where `hold` or `deny` is declared;
- bypassing the egress lock or the overlay boundary: raw data or unredacted
  personal data leaving the process;
- bypassing or forging signature and receipt verification (DSSE, evidence
  chain);
- role or authority bypass on the A2A channel;
- bypassing the commit gate or the supply-chain gate;
- code execution on import, or reading env, disk or network on import.

Out of scope:

- the substantive correctness of a grounded norm — that is a bug, not a
  vulnerability;
- non-deterministic model output with no assurance broken;
- resource exhaustion in a locally invoked CLI;
- missing hardening in files marked as examples.

## Sending a report

Include the affected repository and version, and a reproduction.

**Use synthetic data in proofs of concept.** Do not send real personal data,
third-party credentials, or confidential documents. A report must not become a
data breach of its own.

## Timelines

Acknowledgement within 7 days · initial assessment within 14 days · coordinated
disclosure after a fix, and at the latest 90 days after confirmation. Advisories
are published as GHSA. You are credited unless you prefer otherwise.

## No bounty

This is a one-person project with no bug bounty programme. Reports are welcome
and credited; they are not paid.

## Safe harbour

Good-faith research within this policy — against your own local installation
only, no access to other people's data, no service disruption — will not be
pursued legally by me. I cannot waive the rights of third parties.
