# Zabbix Template - Dell iDRAC by HTTP (Redfish API)

This is a Zabbix 7.0 compatible template for monitoring Dell iDRAC servers using the Redfish API over HTTP. It allows monitoring of hardware status and disk health without requiring an agent on the iDRAC device.

## 🔍 Features

- **Low-Level Discovery (LLD)** for disks via Redfish
- Monitoring of:
  - SSD remaining life (`RemainingPercent`)
  - Endurance used (`EnduranceUsed`)
  - Storage device health (`Health`)
  - Model and serial number of drives
- Utilizes **Zabbix built-in HTTP agent** (no external scripts or agents needed)

## ✅ Requirements

- Zabbix Server **7.0 or later**
- Dell iDRAC with **Redfish API support** (e.g., iDRAC9)
- Host configured with macros for Redfish authentication

## 🚀 Setup Instructions

1. Log in to Zabbix Frontend
2. Go to **Configuration → Templates → Import**
3. Import the file: `Dell Idrac by HTTP.yaml`
4. Link this template to your iDRAC host
5. Define the following macros in the host:

## 🔐 Required Macros

| Macro               | Description                | Example            |
|--------------------|----------------------------|--------------------|
| `{$IDRAC.USER}`     | iDRAC login username       | `root`             |
| `{$IDRAC.PASSWORD}` | iDRAC login password       | `calvin`           |
| `{$IDRAC.BASEURL}`  | Redfish API base URL       | `https://10.1.3.88`|

## 📂 File Contents

- `Dell Idrac by HTTP.yaml`: Zabbix 7.0 template using HTTP agent

## 📄 License

Licensed under the **MIT License**.
