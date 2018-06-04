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

# ITAgentSessionEvent::get_Event


## -description


The 
<b>get_Event</b> method gets an 
<a href="https://msdn.microsoft.com/44eb7669-6c0b-4b9c-a209-9f15f27a1ba9">AGENT_SESSION_EVENT</a> descriptor of the event that occurred.


## -parameters




### -param pEvent [out]

Pointer to the 
<a href="https://msdn.microsoft.com/44eb7669-6c0b-4b9c-a209-9f15f27a1ba9">AGENT_SESSION_EVENT</a> descriptor of the event.


## -returns



This method can return one of these values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory exists to perform the operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>pEvent</i> parameter is not a valid pointer.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/44eb7669-6c0b-4b9c-a209-9f15f27a1ba9">AGENT_SESSION_EVENT</a>



<a href="https://msdn.microsoft.com/70d37d06-b1a6-4f7e-bfe5-731d1b4cd66b">ITAgentSessionEvent</a>
 

 

