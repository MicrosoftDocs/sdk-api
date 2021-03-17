---
UID: NF:p2p.PeerGraphEnumConnections
title: PeerGraphEnumConnections function (p2p.h)
description: The PeerGraphEnumConnections function creates and returns an enumeration handle used to enumerate the connections of a local node.
helpviewer_keywords: ["PeerGraphEnumConnections","PeerGraphEnumConnections function [Peer Networking]","p2p.peergraphenumconnections","p2p/PeerGraphEnumConnections"]
old-location: p2p\peergraphenumconnections.htm
tech.root: p2p
ms.assetid: ef4ea3e2-fd71-48d8-a9a8-db38ef06df20
ms.date: 12/05/2018
ms.keywords: PeerGraphEnumConnections, PeerGraphEnumConnections function [Peer Networking], p2p.peergraphenumconnections, p2p/PeerGraphEnumConnections
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
 - PeerGraphEnumConnections
 - p2p/PeerGraphEnumConnections
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
 - PeerGraphEnumConnections
---

# PeerGraphEnumConnections function


## -description

The <b>PeerGraphEnumConnections</b> function creates and returns an enumeration handle used to enumerate the connections of a local node.

## -parameters

### -param hGraph [in]

Handle to a peer graph.

### -param dwFlags [in]

The  type of connection to enumerate. This parameter is required. Valid values are specified by <a href="/windows/desktop/api/p2p/ne-p2p-peer_connection_flags">PEER_CONNECTION_FLAGS</a>.

### -param phPeerEnum [out]

Receives a handle to an  enumeration.  Use <a href="/windows/desktop/api/p2p/nf-p2p-peergraphgetnextitem">PeerGraphGetNextItem</a> to retrieve the actual connection information. When this handle is not required, free it by calling  <a href="/windows/desktop/api/p2p/nf-p2p-peergraphendenumeration">PeerGraphEndEnumeration</a>.

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
The peer graph must be  initialized with a call to <a href="/windows/desktop/api/p2p/nf-p2p-peergraphstartup">PeerGraphStartup</a> before using this function.

</td>
</tr>
</table>

## -remarks

When <a href="/windows/desktop/api/p2p/nf-p2p-peergraphgetnextitem">PeerGraphGetNextItem</a> is called with the enumeration handle returned by <b>PeerGraphEnumConnections</b>, <b>PeerGraphGetNextItem</b> returns a <a href="/windows/desktop/api/p2p/ns-p2p-peer_connection_info">PEER_CONNECTION_INFO</a> structure.

## -see-also

<a href="/windows/desktop/api/p2p/ns-p2p-peer_connection_info">PEER_CONNECTION_INFO</a>



<a href="/windows/desktop/api/p2p/nf-p2p-peergraphendenumeration">PeerGraphEndEnumeration</a>



<a href="/windows/desktop/api/p2p/nf-p2p-peergraphgetitemcount">PeerGraphGetItemCount</a>



<a href="/windows/desktop/api/p2p/nf-p2p-peergraphgetnextitem">PeerGraphGetNextItem</a>