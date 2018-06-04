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

# BCLASS_QUERY_STATUS_CALLBACK callback function


## -description


<i>BatteryMiniQueryStatus</i> returns status information about the given battery device.


## -parameters




### -param Context [in]

A pointer to the context area allocated by the miniclass driver for the battery device.


### -param BatteryTag [in]

A battery tag value previously returned by <i>BatteryMiniQueryTag</i>.


### -param BatteryStatus [out]

A pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff536290">BATTERY_STATUS</a> structure in which the miniclass driver returns information. 


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
<dt><b>STATUS_SUCCESS </b></dt>
</dl>
</td>
<td width="60%">
The battery designated by <i>BatteryTag </i>is currently installed. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_NO_SUCH_DEVICE</b></dt>
</dl>
</td>
<td width="60%">
The battery designated by <i>BatteryTag </i>is not present.

</td>
</tr>
</table>
 




## -remarks



The battery class driver calls <i>BatteryMiniQueryStatus</i> to get status information about the battery. The status information includes the battery's power state, capacity, voltage, and the amount of current flowing at the time of the request.

If the miniclass driver does not supply fully functional <a href="https://msdn.microsoft.com/ec463202-4c08-475a-b612-73413f1376fc">BatteryMiniSetStatusNotify</a> and <a href="https://msdn.microsoft.com/5120205f-0d55-4391-a560-3089fbe11d82">BatteryMiniDisableStatusNotify</a> routines, the battery class driver calls <i>BatteryMiniQueryStatus</i> at regular but infrequent intervals to poll the battery's status. Otherwise, the class driver calls this routine after the miniclass driver has notified it of a change in battery status.

Before reporting a critically low, discharging battery (BATTERY_DISCHARGING and BATTERY_CRITICAL), the miniclass driver should ensure that the problem is legitimate (rather than a transitory state) and if so, should attempt to solve the problem. Possible solutions might include switching to AC power or to another battery. When the miniclass driver reports that a battery is critical and discharging, the system assumes that battery failure is imminent and prepares to shut down.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff536269">BatteryClassStatusNotify</a>



<a href="https://msdn.microsoft.com/5120205f-0d55-4391-a560-3089fbe11d82">BatteryMiniDisableStatusNotify</a>



<a href="https://msdn.microsoft.com/ec463202-4c08-475a-b612-73413f1376fc">BatteryMiniSetStatusNotify</a>
 

 

