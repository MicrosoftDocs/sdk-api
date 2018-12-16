---
UID: NF:p2p.PeerGraphEnumConnections
title: PeerGraphEnumConnections function
author: windows-sdk-content
description: The PeerGraphEnumConnections function creates and returns an enumeration handle used to enumerate the connections of a local node.
old-location: p2p\peergraphenumconnections.htm
tech.root: P2PSdk
ms.assetid: ef4ea3e2-fd71-48d8-a9a8-db38ef06df20
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: PeerGraphEnumConnections, PeerGraphEnumConnections function [Peer Networking], p2p.peergraphenumconnections, p2p/PeerGraphEnumConnections
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
 - PeerGraphEnumConnections
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PeerGraphEnumConnections function


## -description


The <b>PeerGraphEnumConnections</b> function creates and returns an enumeration handle used to enumerate the connections of a local node.


## -parameters




### -param hGraph [in]

Handle to a peer graph.


### -param dwFlags [in]

The  type of connection to enumerate. This parameter is required. Valid values are specified by <a href="https://msdn.microsoft.com/24723421-18e4-4333-8c25-f5ee08182f7f">PEER_CONNECTION_FLAGS</a>.


### -param phPeerEnum [out]

Receives a handle to an  enumeration.  Use <a href="https://msdn.microsoft.com/f595e66d-570f-4642-bef8-ff5cf070649c">PeerGraphGetNextItem</a> to retrieve the actual connection information. When this handle is not required, free it by calling  <a href="https://msdn.microsoft.com/31a18705-b8bf-461c-98e0-c03c6d269b51">PeerGraphEndEnumeration</a>.


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
The peer graph must be  initialized with a call to <a href="https://msdn.microsoft.com/00ffdec7-f084-4170-a4a1-e6112bab4d61">PeerGraphStartup</a> before using this function.

</td>
</tr>
</table>
 




## -remarks



When <a href="https://msdn.microsoft.com/f595e66d-570f-4642-bef8-ff5cf070649c">PeerGraphGetNextItem</a> is called with the enumeration handle returned by <b>PeerGraphEnumConnections</b>, <b>PeerGraphGetNextItem</b> returns a <a href="https://msdn.microsoft.com/039fa00e-c193-46fd-b7e6-41eb7baeab3e">PEER_CONNECTION_INFO</a> structure.




## -see-also




<a href="https://msdn.microsoft.com/039fa00e-c193-46fd-b7e6-41eb7baeab3e">PEER_CONNECTION_INFO</a>



<a href="https://msdn.microsoft.com/31a18705-b8bf-461c-98e0-c03c6d269b51">PeerGraphEndEnumeration</a>



<a href="https://msdn.microsoft.com/db97b7e0-6f85-4b61-843f-efb4bc93149b">PeerGraphGetItemCount</a>



<a href="https://msdn.microsoft.com/f595e66d-570f-4642-bef8-ff5cf070649c">PeerGraphGetNextItem</a>
 

 

