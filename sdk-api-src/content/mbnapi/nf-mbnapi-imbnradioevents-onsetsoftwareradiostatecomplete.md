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

# IMbnRadioEvents::OnSetSoftwareRadioStateComplete


## -description


Notification that a set software radio state operation has completed.


## -parameters




### -param newInterface [in]

Pointer to an <a href="https://msdn.microsoft.com/b4b5ccfc-6cbf-4090-aee1-ee97092147f7">IMbnRadio</a> interface representing the device for which a set radio state operation has completed.


### -param requestID [in]

The request ID set by the Mobile Broadband service to identify the request.


### -param status [in]

A status code that indicates the outcome of the set radio state operation.

A calling application can expect one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="S_OK"></a><a id="s_ok"></a><dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The operation was successful.

</td>
</tr>
</table>
 


## -returns



This method must return <b>S_OK</b>.




## -see-also




<a href="https://msdn.microsoft.com/f02fa823-c1ca-4867-981d-cb3107f7291b">IMbnRadioEvents</a>
 

 

