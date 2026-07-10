# Network-Setup-So-Easy-Your-GrandParents-Could-Do-It
Easy Setup Technical note on Network Setup for medium and large network installations or residential/commercial network configuration.
Wireless Controller (XWC-1000), Accesspoint (XAP-1610), Network Switch (AMS-4424P Managed Switch) and Router (XWR-3150, ABR-5000)

## Scenario 1 — Medium Installation (280–370 sq. meters)

Setup of **XWR-3150 Router** with an added **XAP-1610 Access Point**.

### XWR-3150 Connections

| Port | Function |
|---|---|
| Internet port | From ISP modem |
| On/Off | Power button |
| Power | Plug in the power cable |
| LAN Ports | Connect to network devices |
| Reset button | Restores factory settings |
| Antenna | Wireless router offering 2.4 GHz and 5 GHz communication |

### Adding an XAP-1610 Access Point

Connect the PoE injector's **IN** port to the router's LAN port, then run the **OUT** port into the access point.

```
Router (LAN) → PoE Injector (IN) → PoE Injector (OUT) → Access Point
```

### Modem Tips & Tricks

> Don't let the IP address of your Luxul router fall within the range of the ISP's IP address.

| Just a Modem | Modem/Router Combo |
|---|---|
| Generally used when ISP is Cable | Serves a LAN IP address (e.g. `192.168.x.x`) |
| Serves a single WAN IP address | Verify the router's subnet differs from the modem/router combo's subnet |
| Connection Type: DHCP | Connection Type: DHCP |
| Can authenticate one device at a time | Example: `192.168.0.1` – Luxul / `192.168.1.1` – Modem |
| Commonly requires a reboot when connecting a new device | |

---

## Scenario 2 — Larger Installation (560+ sq. meters)

For an automation system with many wired devices and up to 50 wireless devices.

Setup: **ABR-5000 Router**, **AMS-4424P Managed Switch**, **XWC-1000 Wireless Controller**

### Epic 5 ABR-5000 Connections

| Port | Function |
|---|---|
| WAN Ports (x2) | From ISP modem |
| On/Off | Power button |
| Power | Plug in the power cable |
| LAN 1 | To switch |

> The switch is like the engine — all data/power comes from it.

### XWC-1000 (Wireless Controller) Connections

- Can handle up to **16 access points**
- LAN port connects **from the switch**
- Includes standard power cable connection

### AMS-4424P (Managed Switch) Connections

No PoE injector is needed here.

| Port | Function |
|---|---|
| Port 1 | From router |
| Port 2 | To controller |
| Ports 3 & 4 | To access points |
| Remaining ports | To network devices |

---

## Easy Setup App

### What It Does

The Easy Setup App allows configuration of wireless routers and attached access points directly from a mobile phone — no laptop required. It can:

- Change the login password
- Update firmware if necessary
- Add access points if necessary
- Name the 2.4 GHz and 5 GHz SSIDs
- Set the Wi-Fi password
- Share network info if necessary

### Notes on Using the App

Available on the **Google Play Store**.

**Router requirements**
- Compatible only with **XWR-1200** and **XWR-3150** wireless routers
- Router must be in factory default state:
  - Default SSIDs broadcasting with no password
  - Default admin password
  - Firmware version **6.3.1 or higher**

**Android**
- All permissions must be granted, including location services

**iOS**
- iOS requires user approval every time the app wants to join a network — the **JOIN** button must be pressed

**Acknowledgement**
- Homemation, Luxul, Control4
