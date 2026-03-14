# Lab 3 — Enterprise Router Configuration

## Scenario

Southern Star Logistics Pty Ltd recently deployed a new Windows Server in their internal infrastructure.

The server must communicate with the enterprise router (default gateway) in order to reach external networks and internet services.

The IT team must verify that the server has correct network configuration and routing information.

---

## Lab Objectives

• Verify IP configuration  
• Validate default gateway (enterprise router)  
• Inspect routing table  
• Test connectivity across the network  

---

## Lab Environment

Virtualization Platform: Virtual Machine  
Server OS: Windows Server  
Host System: macOS  

---

## Lab Environment Screenshot

<img src="./images/windows-server-environment.png" width="700">

Figure 1: Windows Server virtual machine used for enterprise router configuration testing.

---

## Commands Used
```
ipconfig
route print
ping 8.8.8.8
tracert google.com

```
---

## Screenshots
### IP Configuration Verification

<img src="./images/route-table.png" width="700">

The routing table was examined using the `route print` command in Windows Server.

This table shows how the operating system decides where to forward network traffic.

The default route entry:

```
0.0.0.0 → 10.0.2.2
```


indicates that all traffic destined for external networks is forwarded to the default gateway.

This confirms that the server correctly uses the configured router to reach external networks such as the internet.
