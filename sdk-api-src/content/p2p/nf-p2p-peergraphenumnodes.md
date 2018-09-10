---
UID: NF:p2p.PeerGraphEnumNodes
title: PeerGraphEnumNodes function
author: windows-sdk-content
description: The PeerGraphEnumNodes function creates and returns an enumeration handle used to enumerate the nodes in a peer graph.
old-location: p2p\peergraphenumnodes.htm
tech.root: p2psdk
ms.assetid: 68231b0a-6002-4974-84d7-08b0629f3622
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: PeerGraphEnumNodes, PeerGraphEnumNodes function [Peer Networking], p2p.peergraphenumnodes, p2p/PeerGraphEnumNodes
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: p2p.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2 [desktop apps only],Windows XP with SP1 with the Advanced Networking Pack forWindows XP
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: P2PGraph.lib
req.dll: P2PGraph.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - P2PGraph.dll
api_name:
 - PeerGraphEnumNodes
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PeerGraphEnumNodes function


## -description


The <b>PeerGraphEnumNodes</b> function creates and returns an enumeration handle used to enumerate  the nodes in a peer graph.  The enumeration provides  a snapshot of a peer graph at the time an enumeration is performed.   Depending on the policy of a peer graph, and if nodes do not publish presence information, an enumeration does not return some nodes that are connected to a peer graph.


## -parameters




### -param hGraph [in]

Handle to  a  peer graph.


### -param pwzPeerId [in]

The peer ID   to obtain a node enumeration.	Specify <b>NULL</b> to return all nodes in  a peer graph.


### -param phPeerEnum [out]

Receives a handle to an enumeration.  Use <a href="https://msdn.microsoft.com/f595e66d-570f-4642-bef8-ff5cf070649c">PeerGraphGetNextItem</a> to retrieve the actual node information. When this handle is not needed, free it by calling  <a href="https://msdn.microsoft.com/31a18705-b8bf-461c-98e0-c03c6d269b51">PeerGraphEndEnumeration</a>.


## -returns



If a function call succeeds, the return value is <b>S_OK</b>. Otherwise, it  returns one of the following values.

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
One parameter is not valid.

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
A peer graph must be initialized with a call to <a href="https://msdn.microsoft.com/00ffdec7-f084-4170-a4a1-e6112bab4d61">PeerGraphStartup</a> before using this function.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PEER_E_NOT_READY</b></dt>
</dl>
</td>
<td width="60%">
A peer graph is not synchronized completely, and the nodes cannot be enumerated.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PEER_E_PRESENCE_DISABLED</b></dt>
</dl>
</td>
<td width="60%">
A peer graph does not require presence information. Therefore, the nodes cannot be enumerated.

</td>
</tr>
</table>
 




## -remarks



If <a href="https://msdn.microsoft.com/f595e66d-570f-4642-bef8-ff5cf070649c">PeerGraphGetNextItem</a> is called with the handle that   <b>PeerGraphEnumNodes</b> returns, then <b>PeerGraphGetNextItem</b>  returns the data in the  <a href="https://msdn.microsoft.com/51cc6c27-91ca-4d02-95d6-207827450fd5">PEER_NODE_INFO</a> structure.




## -see-also




<a href="https://msdn.microsoft.com/51cc6c27-91ca-4d02-95d6-207827450fd5">PEER_NODE_INFO</a>



<a href="https://msdn.microsoft.com/31a18705-b8bf-461c-98e0-c03c6d269b51">PeerGraphEndEnumeration</a>



<a href="https://msdn.microsoft.com/db97b7e0-6f85-4b61-843f-efb4bc93149b">PeerGraphGetItemCount</a>



<a href="https://msdn.microsoft.com/f595e66d-570f-4642-bef8-ff5cf070649c">PeerGraphGetNextItem</a>
 

 

