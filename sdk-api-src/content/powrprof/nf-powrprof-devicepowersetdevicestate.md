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

# DevicePowerSetDeviceState function


## -description


Modifies the specified data on the specified device.


## -parameters




### -param DeviceDescription [in]

The name or hardware identifier string of the device to be modified.


### -param SetFlags [in]

The properties of the device that are to be modified.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="DEVICEPOWER_SET_WAKEENABLED"></a><a id="devicepower_set_wakeenabled"></a><dl>
<dt><b>DEVICEPOWER_SET_WAKEENABLED</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
Enables the specified device to wake the system.

</td>
</tr>
<tr>
<td width="40%"><a id="DEVICEPOWER_CLEAR_WAKEENABLED"></a><a id="devicepower_clear_wakeenabled"></a><dl>
<dt><b>DEVICEPOWER_CLEAR_WAKEENABLED</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
Stops the specified device from being able to wake the system.

</td>
</tr>
</table>
 


### -param SetData [in]

Reserved, must be <b>NULL</b>.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
	      <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -see-also




<a href="https://msdn.microsoft.com/aaa776e5-3fc2-41bd-a805-6c09ef73807b">Device Power Management</a>
 

 

