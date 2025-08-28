# VMware-home-lab-project
# Create a GitHub-ready starter repo for a SysAdmin Home Lab project
import os, textwrap, zipfile, json

base = "/mnt/data/sysadmin-home-lab-starter"
paths = [
    "docs",
    "scripts/powershell",
    "scripts/bash",
    "configs/smb",
    "configs/gpo",
    "configs/dhcp",
    "infra"
]
for p in paths:
    os.makedirs(os.path.join(base, p), exist_ok=True)

readme = f"""# SysAdmin Home Lab: Windows + Linux (AD/DNS/DHCP/Samba/pfSense)

A hands-on lab that simulates a small business network with **Windows Server (AD, DNS, DHCP)**, **pfSense** routing/firewall, **Linux (Samba file server)**, and a **Windows 10/11 client**. Use this repo to document your build, store configs/scripts, and show your process on GitHub.

## Architecture (at a glance)


