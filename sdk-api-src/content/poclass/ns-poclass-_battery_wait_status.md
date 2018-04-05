---
UID: NS:poclass._BATTERY_WAIT_STATUS
title: "_BATTERY_WAIT_STATUS"
author: windows-driver-content
description: Contains information about the conditions under which the battery status is to be retrieved.
old-location: base\battery_wait_status_str.htm
old-project: Power
ms.assetid: 1750fe0f-ba3d-4118-938c-789c6d62c3f7
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: "*PBATTERY_WAIT_STATUS, BATTERY_CHARGING, BATTERY_CRITICAL, BATTERY_DISCHARGING, BATTERY_POWER_ON_LINE, BATTERY_WAIT_STATUS, BATTERY_WAIT_STATUS structure, PBATTERY_WAIT_STATUS, PBATTERY_WAIT_STATUS structure pointer, _BATTERY_WAIT_STATUS, _win32_battery_wait_status_str, base.battery_wait_status_str, batclass/BATTERY_WAIT_STATUS, batclass/PBATTERY_WAIT_STATUS, poclass/BATTERY_WAIT_STATUS, poclass/PBATTERY_WAIT_STATUS"
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
req.typenames: BATTERY_WAIT_STATUS, *PBATTERY_WAIT_STATUS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Poclass.h
-	Batclass.h
api_name:
-	BATTERY_WAIT_STATUS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# _BATTERY_WAIT_STATUS structure


## -description


Contains information about the conditions under which the battery status is to be retrieved. This structure is used by the 
<a href="https://msdn.microsoft.com/7a7bf429-9b2c-4faf-9f27-fb5fd8dd18df">IOCTL_BATTERY_QUERY_STATUS</a> control code.


## -struct-fields




### -field BatteryTag

The current battery tag for the battery. Only information for a battery matching the tag can be returned. Whenever this value does not match the battery's current tag, the <a href="https://msdn.microsoft.com/1d35c087-6672-4fc6-baa1-a886dd9d3878">DeviceIoControl</a> operation will fail with an error code of ERROR_FILE_NOT_FOUND, which indicates to the caller that the battery for which it has a tag is no longer installed The caller may opt to use the 
<a href="https://msdn.microsoft.com/0bbe59ba-e037-47ce-a54a-6500ea7c9bc5">IOCTL_BATTERY_QUERY_TAG</a> operation to determine the tag of the newly installed battery, if any. In addition, if the request is in progress when the battery is removed, or the tag changes, the operation is aborted with the status of ERROR_FILE_NOT_FOUND. (See 
<a href="https://msdn.microsoft.com/3580b37d-611c-46b4-9300-4943833d6852">Battery Tags</a> for more information.)


### -field Timeout

The number of milliseconds the request will wait for the condition specified by the <b>PowerState</b>, <b>LowCapacity</b>, and <b>HighCapacity</b> members before completing. A value of -1 indicates that the request will wait indefinitely for the conditions to be satisfied. A value of zero indicates that the requested battery information is to be returned immediately, regardless of the other conditions. Any other value indicates that the request should wait that length of time, or until any one of the other conditions is satisfied. 




If the computer has entered sleep mode, the clock will continue to run, but exhausting the count will not wake the computer up. If the count is exhausted when the computer is awoken, and other conditions are satisfied, the call will return immediately on awakening.


### -field PowerState

Zero, one, or more of the following status bits, which indicate the state of the battery. It is identical to the <b>PowerState</b> member of the 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff536290">BATTERY_STATUS</a> structure. 



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
Indicates that the battery has access to AC power.

</td>
</tr>
</table>
 


### -field LowCapacity

The current battery capacity, in mWh (or relative). This value is identical to the <b>Capacity</b> member of the 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff536290">BATTERY_STATUS</a> structure.


### -field HighCapacity

The current battery capacity, in mWh (or relative). This value is identical to the <b>Capacity</b> member of the 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff536290">BATTERY_STATUS</a> structure.


## -remarks



Requests for battery information are postponed until one of the following occurs:

<ul>
<li>The time-out expires (assuming <b>Timeout</b> is not -1).</li>
<li>The battery's current status does not match <b>PowerState</b>.</li>
<li>The battery's capacity is below <b>LowCapacity</b>.</li>
<li>The battery's capacity is above <b>HighCapacity</b>.</li>
<li>The battery tag changes.</li>
</ul>
When any one of these conditions is satisfied, the data is collected and the operation returns. This allows applications to monitor typical dynamic battery information without polling the device.

Before using either of the two Capacity conditions, make sure the battery supports them by using the 
<a href="https://msdn.microsoft.com/7a7bf429-9b2c-4faf-9f27-fb5fd8dd18df">IOCTL_BATTERY_QUERY_STATUS</a> control code with a time-out of zero. Examine the results to determine if the <b>Capacity</b> member is supported (that is, not BATTERY_UNKNOWN_CAPACITY).




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff536290">BATTERY_STATUS</a>



<a href="https://msdn.microsoft.com/7a7bf429-9b2c-4faf-9f27-fb5fd8dd18df">IOCTL_BATTERY_QUERY_STATUS</a>



<a href="https://msdn.microsoft.com/0bbe59ba-e037-47ce-a54a-6500ea7c9bc5">IOCTL_BATTERY_QUERY_TAG</a>
 

 

