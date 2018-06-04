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

# IDeviceIoControl::CancelOperation


## -description


The <b>CancelOperation</b> method attempts to cancel a previously issued call by using the <a href="https://msdn.microsoft.com/550eadd0-c03b-40b3-9f08-639085365f4b">DeviceIoControlAsync</a> method.


## -parameters




### -param cancelContext [in]

The cancel context that a previous call to <a href="https://msdn.microsoft.com/550eadd0-c03b-40b3-9f08-639085365f4b">DeviceIoControlAsync</a> returned.


## -returns



This method supports standard return values, in addition to these:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The operation was still outstanding, and cancellation was attempted.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The operation was no longer outstanding.

</td>
</tr>
</table>
 




## -remarks



Regardless of whether cancellation is successful, the result of the operation is available in the callback that's provided to the asynchronous call.




## -see-also




<a href="https://msdn.microsoft.com/d285e04e-04d0-4c2a-b9f0-72eebebf4f4b">IDeviceIoControl</a>
 

 

