# Azureproject
🌐 Multi-Region Azure Architecture with Traffic Manager

This project showcases a *highly available and resilient cloud architecture* using Microsoft Azure services. It demonstrates a global traffic distribution system with *Azure Traffic Manager, regional **Application Gateways, and **Virtual Machines (VMs)* distributed across two Azure regions: *East US 2* and *Central India*.

## 🛠 Architecture Overview

### 🔷 Azure Components Used:
- *Azure Traffic Manager*: Routes user traffic to the nearest healthy region.
- *Application Gateway* (Region-wise):
  - Acts as a load balancer within each region.
  - Routes requests to backend VMs.
- *Virtual Network (VNet)*:
  - Isolated regional networks.
  - Contains backend VMs.
- *Virtual Machines (VMs)*:
  - Hosts the application or services.
- *VNet Peering*:
  - Enables secure communication between VNets across regions.

## 🗺 Architecture Diagram

## 📍 Regions Used
- 🇺🇸 *East US 2*
  - Application Gateway 1
  - VNet 1 with VM1, VM2
- 🇮🇳 *Central India*
  - Application Gateway 2
  - VNet 2 with VM1, VM2

## 🔄 Workflow

1. *User Request* is sent to Azure Traffic Manager.
2. Traffic Manager evaluates region based on routing method (e.g., *Performance, **Priority, **Failover*).
3. Request is directed to *Application Gateway* in the selected region.
4. Application Gateway routes it to one of the VMs within that region's VNet.
5. *VNet Peering* ensures secure cross-region communication if needed.

## ✅ Benefits

- 🌍 *Global Traffic Distribution*
- 🧭 *Geo-redundancy and Disaster Recovery*
- ⚙ *Scalability and Load Balancing*
- 🔐 *Secure Inter-VNet Communication*

## 📦 Use Cases

- Multi-region deployment for web apps or APIs
- Disaster recovery and failover setup
- Performance-based traffic routing
- Secure inter-region workload communication

