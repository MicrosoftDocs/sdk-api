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

# DrvResetDevice function


## -description


The <b>DrvResetDevice</b> function resets a device that is inoperable or unresponsive.


## -parameters




### -param dhpdev

Handle to the physical device's PDEV that describes the physical device that has stopped. This is the value returned by <a href="https://msdn.microsoft.com/library/windows/hardware/ff556211">DrvEnablePDEV</a>.


### -param Reserved

Is reserved and must be set to <b>NULL</b>.


## -returns



<b>DrvResetDevice</b> should return one of the following values:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DRD_ERROR</b></dt>
</dl>
</td>
<td width="60%">
The device did not recover from the error.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DRD_SUCCESS</b></dt>
</dl>
</td>
<td width="60%">
The device is currently in working order.

</td>
</tr>
</table>
 




## -remarks



This function is available in Windows XP and later.

<b>DrvResetDevice</b> is usually called in response to <a href="https://msdn.microsoft.com/library/windows/hardware/ff564958">EngHangNotification</a>. A driver should take any steps necessary to restore the device to working order, and should do so with no data loss or as little as possible.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff556211">DrvEnablePDEV</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff564958">EngHangNotification</a>
 

 

