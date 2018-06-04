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

# ITfMouseTracker::UnadviseMouseSink


## -description




## -parameters




### -param dwCookie [in]

Specifies the mouse advise sink identifier. This value is obtained by a call to <a href="https://msdn.microsoft.com/d73b2b9b-8904-4507-9b32-dcb8946fb887">ITfMouseTracker::AdviseMouseSink</a>.


## -returns



This method can return one of these values.

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method was successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TF_E_DISCONNECTED</b></dt>
</dl>
</td>
<td width="60%">
The context object is not on a document stack.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
The context owner does not support mouse event sinks.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/aad07b35-99e0-4c76-ba65-93c2c972303d">ITfMouseTracker</a>



<a href="https://msdn.microsoft.com/d73b2b9b-8904-4507-9b32-dcb8946fb887">ITfMouseTracker::AdviseMouseSink
      </a>
 

 

