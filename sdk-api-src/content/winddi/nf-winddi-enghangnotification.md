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

# EngHangNotification function


## -description


The <b>EngHangNotification</b> function notifies the system that a specified device is inoperable or unresponsive.


## -parameters




### -param hdev

TBD


### -param Reserved

Is reserved and must be set to <b>NULL</b>.


#### - hDev

Handle to the physical device that has stopped. This parameter is the GDI handle received by the driver's <a href="https://msdn.microsoft.com/library/windows/hardware/ff556181">DrvCompletePDEV</a> entry point.


## -returns



<b>EngHangNotification</b> returns one of the following values:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>EHN_ERROR</b></dt>
</dl>
</td>
<td width="60%">
The device did not recover from the error.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>EHN_RESTORED</b></dt>
</dl>
</td>
<td width="60%">
The device was restored to working order.

</td>
</tr>
</table>
 




## -remarks



A driver should make this call any time it detects that the hardware is inoperable or unresponsive. If <b>EngHangNotification</b> returns EHN_RESTORED, the driver should retry the operation that detected the inoperable state; otherwise the driver should fail the current call as soon as possible. Any subsequent driver operations that detect a problem should again call <b>EngHangNotification</b>.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff556181">DrvCompletePDEV</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff556275">DrvResetDevice</a>
 

 

