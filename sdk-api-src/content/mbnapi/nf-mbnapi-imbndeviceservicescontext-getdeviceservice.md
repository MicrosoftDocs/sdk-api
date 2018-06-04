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

# IMbnDeviceServicesContext::GetDeviceService


## -description


Gets the <a href="IMbnDeviceService">IMbnDeviceService</a> object that can be used for communicating with a device service on the Mobile Broadband device.


## -parameters




### -param deviceServiceID [in]

The <a href="https://msdn.microsoft.com/3AE6D7A6-3974-4517-AEB6-992CAC543247">deviceServiceID</a> of the Mobile Broadband device.


### -param mbnDeviceService [out, retval]

The <a href="IMbnDeviceService">IMbnDeviceService</a> object.


## -returns



The method can return one of the following values.

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
The method completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>Other</b></dt>
</dl>
</td>
<td width="60%">
An error was encountered when executing this method.

</td>
</tr>
</table>
 




## -remarks



<b>GetDeviceService</b> may return an <a href="IMbnDeviceService">IMbnDeviceService</a> object that already has a command or data session open. The calling process can check if the device service is already open.




## -see-also




<a href="https://msdn.microsoft.com/0B97FCCD-0A90-4FA2-9122-B00BD3F1A033">IMbnDeviceServicesContext</a>
 

 

