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

# PeerGraphStartup function


## -description



      The <b>PeerGraphStartup</b> function  indicates to the Peer Graphing Infrastructure what version of the Peer protocols the calling application requires.  <b>PeerGraphStartup</b> must be called before any other peer graphing functions. It must be matched by a call to <a href="https://msdn.microsoft.com/036f1bd6-f8aa-47ba-841e-f731ff486860">PeerGraphShutdown</a>.


## -parameters




### -param wVersionRequested [in]

Specify PEER_GRAPH_VERSION.


### -param pVersionData [out]

Pointer to a <a href="https://msdn.microsoft.com/b212101f-8c34-41d1-92b9-4daf3591200e">PEER_VERSION_DATA</a> structure that receives the 
version of the Peer Infrastructure installed on the local computer.


## -returns



Returns S_OK if the operation succeeds; otherwise, the function returns one of the following values:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
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
<tr>
<td width="40%">
<dl>
<dt><b>PEER_E_UNSUPPORTED_VERSION</b></dt>
</dl>
</td>
<td width="60%">
The version requested is not supported by the Peer Infrastructure .dll installed on the local computer.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/b212101f-8c34-41d1-92b9-4daf3591200e">
        PEER_VERSION_DATA</a>



<a href="https://msdn.microsoft.com/036f1bd6-f8aa-47ba-841e-f731ff486860">PeerGraphShutdown</a>
 

 

