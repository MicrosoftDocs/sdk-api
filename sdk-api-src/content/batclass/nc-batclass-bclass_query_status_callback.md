---
UID: NC:batclass.BCLASS_QUERY_STATUS_CALLBACK
title: BCLASS_QUERY_STATUS_CALLBACK (batclass.h)
description: BatteryMiniQueryStatus returns status information about the given battery device.
helpviewer_keywords: ["BCLASS_QUERY_STATUS_CALLBACK","BCLASS_QUERY_STATUS_CALLBACK callback","BatteryMiniQueryStatus","BatteryMiniQueryStatus callback function [Battery Devices]","bat-mini_49ffd352-4020-4dd0-92ab-7af4c0dd9074.xml","batclass/BatteryMiniQueryStatus","battery.batteryminiquerystatus"]
old-location: battery\batteryminiquerystatus.htm
tech.root: battery
ms.assetid: 04811f63-8a57-4b39-84c5-c9b7f803c057
ms.date: 12/05/2018
ms.keywords: BCLASS_QUERY_STATUS_CALLBACK, BCLASS_QUERY_STATUS_CALLBACK callback, BatteryMiniQueryStatus, BatteryMiniQueryStatus callback function [Battery Devices], bat-mini_49ffd352-4020-4dd0-92ab-7af4c0dd9074.xml, batclass/BatteryMiniQueryStatus, battery.batteryminiquerystatus
req.header: batclass.h
req.include-header: Batclass.h
req.target-type: Desktop
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: PASSIVE_LEVEL
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - BCLASS_QUERY_STATUS_CALLBACK
 - batclass/BCLASS_QUERY_STATUS_CALLBACK
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Batclass.h
api_name:
 - BatteryMiniQueryStatus
---

# BCLASS_QUERY_STATUS_CALLBACK callback function


## -description

<i>BatteryMiniQueryStatus</i> returns status information about the given battery device.

## -parameters

### -param Context [in]

A pointer to the context area allocated by the miniclass driver for the battery device.

### -param BatteryTag [in]

A battery tag value previously returned by <i>BatteryMiniQueryTag</i>.

### -param BatteryStatus [out]

A pointer to a <a href="/previous-versions/ff536290(v=vs.85)">BATTERY_STATUS</a> structure in which the miniclass driver returns information.

## -returns

<i>BatteryMiniQueryStatus</i> returns one of the following:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_SUCCESS</b></dt>
</dl>
</td>
<td width="60%">
The battery designated by <i>BatteryTag</i> is currently installed. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_NO_SUCH_DEVICE</b></dt>
</dl>
</td>
<td width="60%">
The battery designated by <i>BatteryTag</i> is not present.

</td>
</tr>
</table>

## -remarks

The battery class driver calls <i>BatteryMiniQueryStatus</i> to get status information about the battery. The status information includes the battery's power state, capacity, voltage, and the amount of current flowing at the time of the request.

If the miniclass driver does not supply fully functional <a href="/windows/desktop/api/batclass/nc-batclass-bclass_set_status_notify_callback">BatteryMiniSetStatusNotify</a> and <a href="/windows/desktop/api/batclass/nc-batclass-bclass_disable_status_notify_callback">BatteryMiniDisableStatusNotify</a> routines, the battery class driver calls <i>BatteryMiniQueryStatus</i> at regular but infrequent intervals to poll the battery's status. Otherwise, the class driver calls this routine after the miniclass driver has notified it of a change in battery status.

Before reporting a critically low, discharging battery (BATTERY_DISCHARGING and BATTERY_CRITICAL), the miniclass driver should ensure that the problem is legitimate (rather than a transitory state) and if so, should attempt to solve the problem. Possible solutions might include switching to AC power or to another battery. When the miniclass driver reports that a battery is critical and discharging, the system assumes that battery failure is imminent and prepares to shut down.

## -see-also

<a href="/windows/desktop/api/batclass/nf-batclass-batteryclassstatusnotify">BatteryClassStatusNotify</a>



<a href="/windows/desktop/api/batclass/nc-batclass-bclass_disable_status_notify_callback">BatteryMiniDisableStatusNotify</a>



<a href="/windows/desktop/api/batclass/nc-batclass-bclass_set_status_notify_callback">BatteryMiniSetStatusNotify</a>