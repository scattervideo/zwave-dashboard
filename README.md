# Z-Wave JS Health Dashboard

A high-density, auto-populating health monitoring table for Z-Wave networks in Home Assistant. This dashboard provides a consolidated view of Node IDs, battery levels, connection statuses, and "last seen" timestamps.

## Features
- **Auto-Discovery:** Automatically finds all Z-Wave devices using the `zwave_js` integration.
- **Deep Linking:** Click any device name to navigate directly to that device's configuration page in Home Assistant.
- **Smart Status Fallback:** Infers "Sleep" status (💤) for battery devices that don't report explicit status but have checked in recently.
- **Resilient Logic:** Prevents `UndefinedError` by validating the existence of entities before attempting to read them.
- **Responsive Design:** Sticky headers and scrollable container for networks with a high node count.

## Prerequisites
1. **Z-Wave JS:** Works with both the official Z-Wave JS integration and Z-Wave JS UI.
2. **card-mod:** (Recommended) Installed via HACS to clean up card styling and borders.

## Installation
1. Create a new **Manual Card** in your Home Assistant Dashboard.
2. Copy the contents of `zwave_health_card.yaml` into the card configuration.
3. Save and enjoy!

## Compatibility
| Integration | Status |
| :--- | :--- |
| Z-Wave JS (Official) | ✅ Supported |
| Z-Wave JS UI | ✅ Supported |
| Legacy Z-Wave (Deprecated) | ❌ Not Supported |
| OpenZWave (Deprecated) | ❌ Not Supported |

## Data Visibility
Shows Zwave ID number for the device, battery level, status (awake, sleeping, dead) and last seen

https://github.com/scattervideo/zwave-dashboard/blob/main/z-wave%20dashboard%20card.png
