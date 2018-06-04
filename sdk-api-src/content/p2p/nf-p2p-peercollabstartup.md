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

# PeerCollabStartup function


## -description


The <b>PeerCollabStartup</b> function initializes the Peer Collaboration infrastructure.


## -parameters




### -param wVersionRequested [in]

Contains the minimum version of the Peer Collaboration infrastructure requested by the peer.


## -returns



Returns S_OK if the function succeeds. Otherwise, the function returns one of the following values.

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
There is not enough memory to support this operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PEER_E_UNSUPPORTED_VERSION</b></dt>
</dl>
</td>
<td width="60%">
The requested version of the Peer Collaboration Infrastructure is not supported.

</td>
</tr>
</table>
 




## -remarks



This function must be called before any other peer collaboration (PeerCollab*) functions are called.

When the application no longer requires the Peer Collaboration infrastructure, it must make a corresponding call to <a href="https://msdn.microsoft.com/4e328188-c8a1-4ba9-817b-3d130a64b985">PeerCollabShutdown</a>. If <b>PeerCollabStartup</b> is called multiple times, there must be a separate corresponding call to <b>PeerCollabShutdown</b>. All of the components of the infrastructure are cleaned up only when the last call to <b>PeerCollabShutdown</b> occurs.

The current supported version is <b>1.0</b>. Call <code>MAKEWORD(1, 0)</code> to generate this version number WORD value.




## -see-also




<a href="https://msdn.microsoft.com/00c3c1f1-c36c-469a-a644-0ec60f02d25e">Peer Collaboration API Functions</a>



<a href="https://msdn.microsoft.com/4e328188-c8a1-4ba9-817b-3d130a64b985">PeerCollabShutdown</a>
 

 

