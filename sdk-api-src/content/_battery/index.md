---
UID: TP:battery
ms.assetid: 7433fa8b-bcff-3cc7-a61e-27c29a2f632b
ms.author: windowsdriverdev
ms.date: 05/07/18
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: portal
---

# Battery Devices Reference



Overview of the Battery Devices Reference technology.

To develop Battery Devices Reference, you need these headers:

 * [batclass.h](..\batclass\index.md)

For the programming guide, see [Battery Devices Reference](https://review.docs.microsoft.com/en-us/win32-test/battery).

## Functions

| Title   | Description   |
| ---- |:---- |
| [BatteryClassInitializeDevice function](..\batclass\nf-batclass-batteryclassinitializedevice.md) | The BatteryClassInitializeDevice routine initializes a new battery device for the class driver. |
| [BatteryClassIoctl function](..\batclass\nf-batclass-batteryclassioctl.md) | BatteryClassIoctl handles system-defined battery IOCTLs. |
| [BatteryClassQueryWmiDataBlock function](..\batclass\nf-batclass-batteryclassquerywmidatablock.md) | The BatteryClassQueryWmiDataBlock routine is used by battery miniclass drivers inside their DpWmiQueryDataBlock routines to allow the battery class driver to process the WMI data block query requests it handles on behalf of the driver. |
| [BatteryClassStatusNotify function](..\batclass\nf-batclass-batteryclassstatusnotify.md) | BatteryClassStatusNotify notifies the battery class driver of changes in battery status. |
| [BatteryClassSystemControl function](..\batclass\nf-batclass-batteryclasssystemcontrol.md) | The BatteryClassSystemControl routine processes WMI IRPs on behalf of a battery miniclass driver. |
| [BatteryClassUnload function](..\batclass\nf-batclass-batteryclassunload.md) | BatteryClassUnload frees resources for a battery device that is no longer in use. |

## Callback functions

| Title   | Description   |
| ---- |:---- |
| [BCLASS_DISABLE_STATUS_NOTIFY_CALLBACK callback function](..\batclass\nc-batclass-bclass_disable_status_notify_callback.md) | BatteryMiniDisableStatusNotify disables status notification for a battery device. |
| [BCLASS_QUERY_INFORMATION_CALLBACK callback function](..\batclass\nc-batclass-bclass_query_information_callback.md) | BatteryMiniQueryInformation returns information about the given battery device. |
| [BCLASS_QUERY_STATUS_CALLBACK callback function](..\batclass\nc-batclass-bclass_query_status_callback.md) | BatteryMiniQueryStatus returns status information about the given battery device. |
| [BCLASS_QUERY_TAG_CALLBACK callback function](..\batclass\nc-batclass-bclass_query_tag_callback.md) | BatteryMiniQueryTag returns the current battery tag. |
| [BCLASS_SET_INFORMATION_CALLBACK callback function](..\batclass\nc-batclass-bclass_set_information_callback.md) | BatteryMiniSetInformation requests that a battery enter the charging or discharging state, or sets a critical bias value for the battery. |
| [BCLASS_SET_STATUS_NOTIFY_CALLBACK callback function](..\batclass\nc-batclass-bclass_set_status_notify_callback.md) | BatteryMiniSetStatusNotify sets the battery capacity and power state levels at which the class driver requires notification. |

## Structures

| Title   | Description   |
| ---- |:---- |
| [BATTERY_MINIPORT_INFO structure](..\batclass\ns-batclass-battery_miniport_info.md) | Battery miniclass drivers fill in this structure before calling the battery class driver's BatteryClassInitializeDevice routine. |
| [BATTERY_MINIPORT_INFO_V1_1 structure](..\batclass\ns-batclass-battery_miniport_info_v1_1.md) | Battery miniclass drivers fill in the BATTERY_MINIPORT_INFO_V1_1 structure before calling the battery class driver's BatteryClassInitializeDevice routine. BATTERY_MINIPORT_INFO_V1_1 is an updated version of the previous structure BATTERY_MINIPORT_INFO. |
| [BATTERY_NOTIFY structure](..\batclass\ns-batclass-battery_notify.md) | A battery miniclass driver receives a BATTERY_NOTIFY structure when its BatteryMiniSetStatusNotify routine is called. |
| [_BATTERY_TAG_CHANGE structure](..\batclass\ns-batclass-_battery_tag_change.md) | This structure is reserved for system use. |
| [_BATTERY_WMI_CYCLE_COUNT structure](..\batclass\ns-batclass-_battery_wmi_cycle_count.md) | Defines information about number of charge cycles of a battery for use with the BatteryClassQueryWmiDataBlock function. |
| [_BATTERY_WMI_FULL_CHARGED_CAPACITY structure](..\batclass\ns-batclass-_battery_wmi_full_charged_capacity.md) | Defines information about the capacity of a battery for use with the BatteryClassQueryWmiDataBlock). |
| [_BATTERY_WMI_RUNTIME structure](..\batclass\ns-batclass-_battery_wmi_runtime.md) | Defines information about the estimated runtime of a battery for use with the BatteryClassQueryWmiDataBlock function. |
| [_BATTERY_WMI_STATIC_DATA structure](..\batclass\ns-batclass-_battery_wmi_static_data.md) | Defines static data about a battery. |
| [_BATTERY_WMI_STATUS structure](..\batclass\ns-batclass-_battery_wmi_status.md) | Defines battery status information. |
| [_BATTERY_WMI_STATUS_CHANGE structure](..\batclass\ns-batclass-_battery_wmi_status_change.md) | This structure is reserved for system use. |
| [_BATTERY_WMI_TEMPERATURE structure](..\batclass\ns-batclass-_battery_wmi_temperature.md) | Defines information about temperature of the battery for use with the BatteryClassQueryWmiDataBlock function. |
