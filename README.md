![](assets/AstusGitBanner.png)

#### ⚠ WARNING: THESE DOCS ARE UNFINISHED AS OF APR 2026 ⚠

# Astrus Communication Projects - Docs
In this repository you will find all of the publically available documentation for Project Astrus  
this information is intended to help developers and end users understand how to use and develop  
for the Astrus platform. This repository may be relocated to [@luailyprod/astrus-docs](https://github.com/luailyprod/astrus-docs) in the future.

### **WHITEPAPER LOCATED AT `/WHITEPAPER/Astrus-Whitepaper-YYYY_MM.pdf`**

## Basic Astrus Components
### 1. **Nodes** [N/S] (Matrix Equivalent: Homeservers)
   - Documentation: `/nodes/regular-mode/...` | `/nodes/isolated/...`
   - These are the instances which host user data, chat groups, and hold mailboxes. They  
     are built to power the required functions of the ecosystem, so that it can continue to  
     work correctly. Nodes can be used in isolated mode natively.
   - Astrus provides a basic python-based server, named **Astrus-Satellite**.  
     The Astrus-Satellite project contains a basic API which is the standard for federated  
     communication. It requires WS and HTTP support, as well as an x86_64 or ARM64 computer  
     to run. It cannot be run natively on Mobile devices (phones) without heavy modification.
     - Reccomended Specs:
       ```
       CPU: any x86_64 CPU or ARM64 v8 made in the last 12 years with a base speed of 1.90 GHz+
       RAM: 2GB minimum.
       SSD: 10GB of free space minimum. SSDs are reccomended for short term storage.
       HDD: 10GB of free space minimum. HDDs are reccomended for long term storage.
       Flash/SD: 5GB of free space minimum. Flash/SD card storage is NOT reccomended.
       OS/Linux: Debian-systems reccomended. See Python.
       OS/MacOS: Big Sur or newer reccomended. See Python.
       OS/Windows: Windows 10 20h2+ or 11 21h2+ not in S mode. Windows compatibility is untested.
       Python: Python 3.11 to 3.13. 3.14 compatibility is iffy.
       Network: 45mbps WiFi or Ethernet reccomended. 5mbps minimum.
       Net-addressing: static IPv4 or IPv6 reccomended OR domain + proxy.
       Intranet-support: in Isolation mode ONLY.
       ``` 
### 2. **Proxies** [N/P]
   - Documentation: `/nodes/proxy-mode/...`
   - Proxy servers usually run identical serverware to Nodes, however they do not host chat  
     groups or hold user data, they cannot be used with Isolated nodes without extended setup.  
   - Astrus reccomends those who want to host Nodes to use **Astrus-Satellite**.  
     Astrus-Satellite contains the API and presets for proxy support. Mailboxes still run on  
     this configuration and discovery still runs when Isolated mode is off.  
     - Reccomended Specs:
       ```
       CPU: any x86_64 CPU or ARM64 v8 made in the last 12 years with a base speed of 1.60 GHz+
       RAM: 1GB minimum.
       SSD: 5GB of free space reccomended for Mailbox. 2gb required. SSDs are reccomended.
       HDD: 5GB of free space reccomended for Mailbox. 2GB required. HDDs will work.
       Flash/SD: 2GB of free space minimum. SD will work fine here.
       OS/Linux: Debian-systems reccomended. See Python.
       OS/MacOS: Big Sur or newer reccomended. See Python.
       OS/Windows: Windows 10 20h2+ or 11 21h2+ not in S mode. Windows compatibility is untested.
       Python: Python 3.11 to 3.13. 3.14 compatibility is iffy.
       Network: 60mbps WiFi or Ethernet reccomended. 5mbps minimum.
       Net-addressing: static IPv4 or IPv6 reccomended OR domain + proxy.
       Intranet-support: in Isolation mode ONLY with additional setup.
       ```
### 3. **Clients** [C/x]
   - Documentation: `/clients/<type>/...` TYPES: `WEB [C/W]`, `TUI [C/T]`, `DESKTOP [C/D]`, `MOBILE [C/A] & [C/i]`, `UNCONVENTIONAL [C/U]`
   - Clients are the way end-users will interact with the ecosystem, these can come in many forms  
     including, but not limited to, Desktop Clients, Web-Based Clients, Mobile Phone Apps, etc.    
   - Clients are only intended for human users. For building Bots or systems that work with the API   
     see APIs below.  
   - Astrus provides a simple Python-based **tui** desktop client named **Astrus-STARship**.   
     This runs on any system that has a terminal UI and has Python 3.11 - 3.13 installed.  
   - Astrus also provides a basic **web**-based client named **Astrus-SPACEship**.  
     CHROMIUM: any system with at least 2GB of RAM and a chromium-based brower version 121 or higher.  
     FIREFOX: any system with at least 1.5GB of RAM and a firefox-based browser version 122 or higher.  
   - ASTRUS AT THE MOMENT DOES NOT PROVIDE ANY DESKTOP OR MOBILE CLIENTS.  
     WE PREFER COMMUNITY DEVELOPED MOBILE & DESKTOP APPS.  
### 4. **API Routers** [A/x]
   - Documentation: `/API/ROUTERS/...` 
   - API documentation: `/API/<type>/...` TYPES: `ROUTERS [A/R]`, `WEBHOOKS [A/W]`, `APPLICATIONS [A/A]`, `DISCOVERY [A/D]`
   - API routers are similar to proxies but only meant for application interactions or webhooks,
     providing a stable way to connect to Clients & Nodes to serve or get data. By default these should
     require authentication using API Keys.
   - Astrus provides a full API blueprint and partially maintained Python & JavaScript API libraries  
     under the names **astrus-JS** and **astrus-PY** for developers to use as reference.

## Pre-release Software

| **Build**            |   N   |   C   |   A   | **Update Frequency** | **Enrollment Process** |
|----------------------|-------|-------|-------|----------------------|------------------------|
| SOURCE PROOF         |   ✕   |   ✕   |   ✕   |          ✕           |     Develop Astrus     |
| SDK Packages         |  ALL  |   ✕   |   ✕   |     see SDK Repo     |No Enrollment Possible*¹|
| Nightly Channel      |  ALL  |`T & W`|   ✕   |        Weekly*²      |     Download Nightly   |
| Public Beta Channel  |  ALL  |`T & W`|`R,W,A`| Monthly or Quarterly |      Download Beta     |
| Release Candidate    |  ALL  |`T & W`|`R,W,A`|7 Days Before Release*³| Download Preview Build |
| Stable Release       |  ALL  |`T & W`|`R,W,A`|      Release Day     |     Download Stable    |

<sub>*¹:*SDK is INVITE-ONLY by REQUEST. There are no SDK builds currently and enrollment is closed for now.*</sub>  
<sub>*²:*Nightly releases are meant to be released weekly, however this is not a guarantee.*</sub>   
<sub>*³:*Release Candidate Builds may be skipped and be sent directly to Release channel if no previewable features*</sub>  

---------
## Funding
### Funding Development
Creating such a large project with so many moving parts requires either lots of time or lots of funding  
and unfortunately I have neither, however I also don't have a way to process payments, therefore I cannot  
currently work on this project as much as I'd like. 

### Usage Funding
This is a community supported project, therefore there is no requirement to pay for Astrus services directly.  
**NO ASTRUS CLIENT OR SERVER-SOFTWARE WILL BE SOLD.** IN-SOFTWARE ADs ARE PROHIBITED. 

### Licensing
All software related to the Astrus Project MUST be licensed under a Share-Alike license. More details soon...

---------
### Credits

* Developer(s): 
   * (incompetent) Lead Dev: [@luaily](https://github.com/luaily)  
* Licensing/Distribution:  
   * Release & Release Candidate Builds: [Luaily Productions (@luailyprod)](https://github.com/luailyprod)  
   * Pre-release Builds: [Socks Softworks](https://https://github.com/luailyprod) a subsidiary of Luaily Productions

Last Updated: `April 28th 2026`

