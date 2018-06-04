---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# BCLASS_DISABLE_STATUS_NOTIFY_CALLBACK callback function


## -description


<i>BatteryMiniDisableStatusNotify</i> disables status notification for a battery device.

This callback function is specified in the <a href="https://msdn.microsoft.com/3266126A-AEFC-445C-89D3-736545101522">BATTERY_MINIPORT_INFO_V1_1</a> structure.


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




<a href="https://msdn.microsoft.com/library/windows/hardware/ff536269">BatteryClassStatusNotify</a>



<a href="https://msdn.microsoft.com/ec463202-4c08-475a-b612-73413f1376fc">BatteryMiniSetStatusNotify</a>
 

 

