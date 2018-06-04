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

# DrtGetEventData function


## -description


The	<b>DrtGetEventData</b> function retrieves event data associated with a signaled event.


## -parameters




### -param hDrt [in]

Handle to the Distributed Routing Table instance for which the event occurred.


### -param ulEventDataLen [out]

The size, in bytes, of the <i>pEventData</i> buffer.


### -param pEventData [out]

Pointer to a <a href="https://msdn.microsoft.com/b52bf815-d962-4f72-8876-a80769bc3d3d">DRT_EVENT_DATA</a> structure that contains the event data.


## -returns



This function returns S_OK on success. Other possible values include:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
The DRT infrastructure is unaware of the requested search.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The <i>hDrt</i> handle is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DRT_E_INSUFFICIENT_BUFFER</b></dt>
</dl>
</td>
<td width="60%">
The provided buffer is insufficient in size.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DRT_E_NO_MORE</b></dt>
</dl>
</td>
<td width="60%">
No more event data available.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/b52bf815-d962-4f72-8876-a80769bc3d3d">DRT_EVENT_DATA</a>
 

 

