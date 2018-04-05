---
UID: NS:poclass._BATTERY_STATUS
title: "_BATTERY_STATUS"
author: windows-driver-content
description: Contains the current state of the battery.
old-location: base\battery_status_str.htm
old-project: Power
ms.assetid: 514906a1-9d7a-40cb-9798-84f6b93d7bfe
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: "*PBATTERY_STATUS, BATTERY_CHARGING, BATTERY_CRITICAL, BATTERY_DISCHARGING, BATTERY_POWER_ON_LINE, BATTERY_STATUS, BATTERY_STATUS structure, PBATTERY_STATUS, PBATTERY_STATUS structure pointer, _BATTERY_STATUS, _win32_battery_status_str, base.battery_status_str, batclass/BATTERY_STATUS, batclass/PBATTERY_STATUS, poclass/BATTERY_STATUS, poclass/PBATTERY_STATUS"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: poclass.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Pnpxassoc.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: BATTERY_STATUS, *PBATTERY_STATUS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Poclass.h
-	Batclass.h
api_name:
-	BATTERY_STATUS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# _BATTERY_STATUS structure


## -description


Contains the current state of the battery. This structure is used by the 
<a href="https://msdn.microsoft.com/7a7bf429-9b2c-4faf-9f27-fb5fd8dd18df">IOCTL_BATTERY_QUERY_STATUS</a> control code.


## -struct-fields




### -field PowerState

The battery state. This member can be zero, one, or more of the following values. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="BATTERY_CHARGING"></a><a id="battery_charging"></a><dl>
<dt><b>BATTERY_CHARGING</b></dt>
<dt>0x00000004</dt>
</dl>
</td>
<td width="60%">
Indicates that the battery is currently charging.

</td>
</tr>
<tr>
<td width="40%"><a id="BATTERY_CRITICAL"></a><a id="battery_critical"></a><dl>
<dt><b>BATTERY_CRITICAL</b></dt>
<dt>0x00000008</dt>
</dl>
</td>
<td width="60%">
Indicates that battery failure is imminent. See the Remarks section for more information.

</td>
</tr>
<tr>
<td width="40%"><a id="BATTERY_DISCHARGING"></a><a id="battery_discharging"></a><dl>
<dt><b>BATTERY_DISCHARGING</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
Indicates that the battery is currently discharging.

</td>
</tr>
<tr>
<td width="40%"><a id="BATTERY_POWER_ON_LINE"></a><a id="battery_power_on_line"></a><dl>
<dt><b>BATTERY_POWER_ON_LINE</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
Indicates that the system has access to AC power, so no batteries are being discharged.

</td>
</tr>
</table>
 


### -field Capacity

The current battery capacity, in mWh (or relative). This value can be used to generate a "gas gauge" display by dividing it by <b>FullChargedCapacity</b> member of the 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff536283">BATTERY_INFORMATION</a> structure. If the capacity is unavailable, this member is BATTERY_UNKNOWN_CAPACITY.


### -field Voltage

The current battery voltage across the battery terminals, in millivolts (mv). If the voltage is unavailable, this member is BATTERY_UNKNOWN_VOLTAGE.


### -field Rate

The current rate of battery charge or discharge. This value will be in milliwatts  unless the battery rate information is relative, in which case it will be in arbitrary units per hour. To determine if  battery information is relative, examine the BATTERY_CAPACITY_RELATIVE flag in the <b>Capabilities</b> member of the 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff536283">BATTERY_INFORMATION</a> structure. A nonzero, positive rate indicates charging; a negative rate indicates discharging. Some batteries report only discharging rates.  If the rate is unavailable, this member is BATTERY_UNKNOWN_RATE.  If the state of the battery or power source changes, the rate may become available.


## -remarks



The BATTERY_CRITICAL flag in the <b>PowerState</b> member of this structure indicates a hardware "battery critical" condition. This critical level is set by the battery manufacturer, not by the user in the "critical battery alarm." It generally means that the battery system has calculated that the battery is totally drained, and any power being drawn is beyond what is expected.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff536283">BATTERY_INFORMATION</a>



<a href="https://msdn.microsoft.com/7a7bf429-9b2c-4faf-9f27-fb5fd8dd18df">IOCTL_BATTERY_QUERY_STATUS</a>
 

 

