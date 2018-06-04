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

# BCLASS_QUERY_TAG_CALLBACK callback function


## -description


<i>BatteryMiniQueryTag</i> returns the current battery tag.


## -parameters




### -param Context [in]

A pointer to the context area allocated by the miniclass driver for the battery device.


### -param BatteryTag [out]

A pointer to a caller-allocated variable in which the miniclass driver returns the battery tag.


## -returns



<i>BatteryMiniQueryTag</i> returns one of the following:

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
A battery is currently installed. 

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
</table>
 




## -remarks



The battery class driver calls <i>BatteryMiniQueryTag</i> to get the value of the current battery tag. If a battery is present, <i>BatteryMiniQueryTag</i> should return the tag in <i>BatteryTag</i> and return STATUS_SUCCESS. 

Each time a battery is inserted, the miniclass driver must increment the value of the tag, regardless of whether this is a new battery or the same battery that was previously present. 

If no battery is present, or if the miniclass driver cannot determine whether a battery is present, it should return STATUS_NO_SUCH_DEVICE and set the value of the tag to BATTERY_TAG_INVALID. 



