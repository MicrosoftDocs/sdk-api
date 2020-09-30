---
UID: NF:p2p.PeerGraphEnumNodes
title: PeerGraphEnumNodes function (p2p.h)
description: The PeerGraphEnumNodes function creates and returns an enumeration handle used to enumerate the nodes in a peer graph.
helpviewer_keywords: ["PeerGraphEnumNodes","PeerGraphEnumNodes function [Peer Networking]","p2p.peergraphenumnodes","p2p/PeerGraphEnumNodes"]
old-location: p2p\peergraphenumnodes.htm
tech.root: p2p
ms.assetid: 68231b0a-6002-4974-84d7-08b0629f3622
ms.date: 12/05/2018
ms.keywords: PeerGraphEnumNodes, PeerGraphEnumNodes function [Peer Networking], p2p.peergraphenumnodes, p2p/PeerGraphEnumNodes
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PeerGraphEnumNodes
 - p2p/PeerGraphEnumNodes
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - P2PGraph.dll
api_name:
 - PeerGraphEnumNodes
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

Receives a handle to an enumeration.  Use <a href="/windows/desktop/api/p2p/nf-p2p-peergraphgetnextitem">PeerGraphGetNextItem</a> to retrieve the actual node information. When this handle is not needed, free it by calling  <a href="/windows/desktop/api/p2p/nf-p2p-peergraphendenumeration">PeerGraphEndEnumeration</a>.

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
A peer graph must be initialized with a call to <a href="/windows/desktop/api/p2p/nf-p2p-peergraphstartup">PeerGraphStartup</a> before using this function.

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

If <a href="/windows/desktop/api/p2p/nf-p2p-peergraphgetnextitem">PeerGraphGetNextItem</a> is called with the handle that   <b>PeerGraphEnumNodes</b> returns, then <b>PeerGraphGetNextItem</b>  returns the data in the  <a href="/windows/desktop/api/p2p/ns-p2p-peer_node_info">PEER_NODE_INFO</a> structure.

## -see-also

<a href="/windows/desktop/api/p2p/ns-p2p-peer_node_info">PEER_NODE_INFO</a>



<a href="/windows/desktop/api/p2p/nf-p2p-peergraphendenumeration">PeerGraphEndEnumeration</a>



<a href="/windows/desktop/api/p2p/nf-p2p-peergraphgetitemcount">PeerGraphGetItemCount</a>



<a href="/windows/desktop/api/p2p/nf-p2p-peergraphgetnextitem">PeerGraphGetNextItem</a>