---
UID: NC:batclass.BCLASS_DISABLE_STATUS_NOTIFY_CALLBACK
title: BCLASS_DISABLE_STATUS_NOTIFY_CALLBACK (batclass.h)
description: BatteryMiniDisableStatusNotify disables status notification for a battery device.
helpviewer_keywords: ["BCLASS_DISABLE_STATUS_NOTIFY_CALLBACK","BCLASS_DISABLE_STATUS_NOTIFY_CALLBACK callback","BatteryMiniDisableStatusNotify","BatteryMiniDisableStatusNotify callback function [Battery Devices]","bat-mini_2e5f13bc-0046-486c-a1f9-be94bf309559.xml","batclass/BatteryMiniDisableStatusNotify","battery.batteryminidisablestatusnotify"]
old-location: battery\batteryminidisablestatusnotify.htm
tech.root: battery
ms.assetid: 5120205f-0d55-4391-a560-3089fbe11d82
ms.date: 12/05/2018
ms.keywords: BCLASS_DISABLE_STATUS_NOTIFY_CALLBACK, BCLASS_DISABLE_STATUS_NOTIFY_CALLBACK callback, BatteryMiniDisableStatusNotify, BatteryMiniDisableStatusNotify callback function [Battery Devices], bat-mini_2e5f13bc-0046-486c-a1f9-be94bf309559.xml, batclass/BatteryMiniDisableStatusNotify, battery.batteryminidisablestatusnotify
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
 - BCLASS_DISABLE_STATUS_NOTIFY_CALLBACK
 - batclass/BCLASS_DISABLE_STATUS_NOTIFY_CALLBACK
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
 - BatteryMiniDisableStatusNotify
---

# BCLASS_DISABLE_STATUS_NOTIFY_CALLBACK callback function


## -description

<i>BatteryMiniDisableStatusNotify</i> disables status notification for a battery device.

This callback function is specified in the <a href="/windows/desktop/api/batclass/ns-batclass-battery_miniport_info_v1_1">BATTERY_MINIPORT_INFO_V1_1</a> structure.

## -parameters

### -param Context [in]

A pointer to the context area allocated by the miniclass driver for the battery device.

## -returns

<i>BatteryMiniDisableStatusNotify</i> returns one of the following:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_SUCCESS </b></dt>
</dl>
</td>
<td width="60%">
A battery is currently installed and status notification has been disabled. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_NO_SUCH_DEVICE</b></dt>
</dl>
</td>
<td width="60%">
No battery is present.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_NOT_SUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
No functionality is provided for this routine.

</td>
</tr>
</table>

## -remarks

The battery class driver calls <i>BatteryMiniDisableStatusNotify</i> when it no longer requires notification of battery conditions set in an earlier call to <i>BatteryMiniSetStatusNotify</i>.

Miniclass drivers that supply a fully functional <i>BatteryMiniDisableStatusNotify</i> routine must also supply a fully functional <i>BatteryMiniSetStatusNotify</i> routine, and vice versa.

## -see-also

<a href="/windows/desktop/api/batclass/nf-batclass-batteryclassstatusnotify">BatteryClassStatusNotify</a>



<a href="/windows/desktop/api/batclass/nc-batclass-bclass_set_status_notify_callback">BatteryMiniSetStatusNotify</a>