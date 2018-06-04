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

# PeerGraphGetNodeInfo function


## -description



      The <b>PeerGraphGetNodeInfo</b> function retrieves information about a specific node.


## -parameters




### -param hGraph [in]

Handle to a peer graph.


### -param ullNodeId [in]

Specifies  the ID of a node   that an application receives  information about. Specify zero (0) to  retrieve information about the local node.


### -param ppNodeInfo [out]

Receives a pointer to a <a href="https://msdn.microsoft.com/51cc6c27-91ca-4d02-95d6-207827450fd5">PEER_NODE_INFO</a> structure that contains the requested information. When the handle is not needed, free it by calling <a href="https://msdn.microsoft.com/a5b7d563-214a-48e0-b184-0c12d62fb125">PeerGraphFreeData</a>.


## -returns



If the function succeeds, the return value is <b>S_OK</b>. Otherwise, the function returns one of the following error codes.

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
One  parameter is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
There is not enough memory to perform a specified operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PEER_E_INVALID_GRAPH</b></dt>
</dl>
</td>
<td width="60%">
The handle to a peer graph is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PEER_E_NOT_INITIALIZED</b></dt>
</dl>
</td>
<td width="60%">
A peer graph must be  initialized by using a call to <a href="https://msdn.microsoft.com/00ffdec7-f084-4170-a4a1-e6112bab4d61">PeerGraphStartup</a> before using this function.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PEER_E_NODE_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
A specified node is not found.

</td>
</tr>
</table>
 




## -remarks



There can be several nodes of a graph on a computer. For example, multiple users may have joined the graph on a specific computer, so the information that <b>PeerGraphGetNodeInfo</b> returns is    about each node—not each computer.




## -see-also




<a href="https://msdn.microsoft.com/51cc6c27-91ca-4d02-95d6-207827450fd5">
        PEER_NODE_INFO</a>



<a href="https://msdn.microsoft.com/a5b7d563-214a-48e0-b184-0c12d62fb125">PeerGraphFreeData</a>
 

 

