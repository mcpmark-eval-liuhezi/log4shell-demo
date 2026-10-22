# Log4Shell Remediation Checklist

Reference facts for the Log4Shell (CVE-2021-44228) security advisory, assembled for the supply-chain security briefing.

## Advisory facts

- **GHSA ID:** GHSA-jfh8-c2jp-5v3q
- **CVE:** CVE-2021-44228
- **Severity:** Critical (CVSS 3.1 score 10.0, vector `CVSS:3.1/AV:N/AC:L/PR:N/UI:N/S:C/C:H/I:H/A:H/E:H`)
- **Affected package:** `org.apache.logging.log4j:log4j-core` (Maven)
- **Affected version range:** `< 2.15.0` (any Log4j version prior to 2.15.0; the Log4j 1.x branch is EOL and vulnerable to other RCE vectors)
- **First patched version:** 2.15.0
  - Note: Apache's updated advice is to move to **2.16.0**, which disables JNDI by default and removes message lookup support (the 2.15.0 patch did not disable attacker-controlled JNDI lookups in all situations — see CVE-2021-45046).
  - Backports of the fix are also available in 2.3.1, 2.12.2, and 2.12.3.

## Toolchain appendix

- **Node.js `v20.11.0` tag (nodejs/node):** `8d4fbd7bb11a300157aeff8e13221c093628dd4e`

## Sources

- GitHub Security Advisory: https://github.com/advisories/GHSA-jfh8-c2jp-5v3q
- Apache Log4j security guide: https://logging.apache.org/log4j/2.x/security.html
