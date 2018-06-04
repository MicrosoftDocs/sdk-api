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

# PeerPnrpEndResolve function


## -description


The <b>PeerPnrpEndResolve</b> function closes the handle for an asynchronous PNRP resolution operation initiated with a previous call to <a href="https://msdn.microsoft.com/140ecca5-85fe-480e-bc69-86e0bc69ad2e">PeerPnrpStartResolve</a>.


## -parameters




### -param hResolve [in]

The handle to the asynchronous peer name resolution operation returned by a previous call to <a href="https://msdn.microsoft.com/140ecca5-85fe-480e-bc69-86e0bc69ad2e">PeerPnrpStartResolve</a>.


## -returns



If the function call succeeds, the return value is <b>S_OK</b>. Otherwise, it  returns one of the following values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One of the parameters is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
There is not enough memory to perform the specified operation.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/140ecca5-85fe-480e-bc69-86e0bc69ad2e">PeerPnrpStartResolve</a>
 

 

