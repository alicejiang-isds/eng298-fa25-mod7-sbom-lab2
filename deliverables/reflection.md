# Module 7: Assignment: Maintaining Secure Systems with SBOMs and Patching----Reflection File


## Part 2: Generate Baseline SBOM and Vulnerability Report
### Syft

**There are 1,829 packages reported.**
There are 2,825 executables reported.
There are 17,016 locations of file metadata reported.
There are 17,014 files digest reported

### Grype
Based on the scan there are 379 vulnerabilies
Based on the severity levels, there are...
- 9 critical
- 36 high
- 1689 medium
- 187 low
- 24 negligible


## CVE-2024-56433

A Linux package called shadow-utils or also known as shadow has a default behaviour where it can conflict the UIDs of users defined on locally administered networks, which have a chance to result in account takeover or gaining access to same-host resources and/or NFS home directory. How the attacker can get access to NFS home directory or same-host resources is through using newuidmap, which basically means unauthorized access to data and network resources.

===

## Part 3: Identify and Apply System Updates

### 3 packages listed from doing the code `sudo apt list --upgradable`
libpython3.10-minimal/jammy-security 3.10.12-1~22.04.12 amd64 [upgradable from: 3.10.12-1~22.04.11]

libpython3.10-stdlib/jammy-security 3.10.12-1~22.04.12 amd64 [upgradable from: 3.10.12-1~22.04.11]

python3.10-minimal/jammy-security 3.10.12-1~22.04.12 amd64 [upgradable from: 3.10.12-1~22.04.11]

---

## Part 5: Reflection
1. How does maintaining updated packages illustrate complete mediation?

Maintaining updated packages illustrate complete mediation by doing security checks on the packages to make sure every time the package is used, the verification on the package are continous and monitored. This helps re-evaluate the security dependencies of the packages anad the security status of the packages overall, as well as making sure policies are still implemented.

2. Why is generating a new SBOM after patching essential to assurance?

Generating a new SBOM after patching is essential to assurance because it gives you the up-to-date information about the vulernabilities, where it tells you the vulernabilities that were detected got updated after patch. It is also related to incident response where it shows logs of detected vulernabilities, the components that were affected, and the operation team can find the root cause of the incident based on the information provided.

3. What risks persist when organizations delay system updates?

Risks that can persist when organizations delay system updates is that it will increase security risks such as cyberattacks and data breaches, so it doesn't just affect developers of the system, but it also affects people who use the system. This also introduces to system downtime where operations are having performance issues, and/or can introduce to system being compromised to the point attackers gain access to the systems, and whatever intentions those bad threat actors have in mind, they can use it for ransom or spreading malware on the network.

4. How does this exercise embody the secure design lifecycle principle?

This exercise embody the secure design lifecycle principle by expressing transparency on what components of the package had detected vulnerabilities and being one of the methods for risk management that is proactive in monitoring and identification. It also serves as a resource for incident response for operation teams, as well as being used for continously doing security checks on the package(s).