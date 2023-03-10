---
UID: NF:p2p.PeerGraphGetNodeInfo
title: PeerGraphGetNodeInfo function (p2p.h)
description: The PeerGraphGetNodeInfo function retrieves information about a specific node.
helpviewer_keywords: ["PeerGraphGetNodeInfo","PeerGraphGetNodeInfo function [Peer Networking]","p2p.peergraphgetnodeinfo","p2p/PeerGraphGetNodeInfo"]
old-location: p2p\peergraphgetnodeinfo.htm
tech.root: p2p
ms.assetid: 7149aba3-d44b-4492-aa56-4d8dbfba7b7c
ms.date: 12/05/2018
ms.keywords: PeerGraphGetNodeInfo, PeerGraphGetNodeInfo function [Peer Networking], p2p.peergraphgetnodeinfo, p2p/PeerGraphGetNodeInfo
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
 - PeerGraphGetNodeInfo
 - p2p/PeerGraphGetNodeInfo
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
 - PeerGraphGetNodeInfo
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

Receives a pointer to a <a href="/windows/desktop/api/p2p/ns-p2p-peer_node_info">PEER_NODE_INFO</a> structure that contains the requested information. When the handle is not needed, free it by calling <a href="/windows/desktop/api/p2p/nf-p2p-peergraphfreedata">PeerGraphFreeData</a>.

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
A peer graph must be  initialized by using a call to <a href="/windows/desktop/api/p2p/nf-p2p-peergraphstartup">PeerGraphStartup</a> before using this function.

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

<a href="/windows/desktop/api/p2p/ns-p2p-peer_node_info">PEER_NODE_INFO</a>



<a href="/windows/desktop/api/p2p/nf-p2p-peergraphfreedata">PeerGraphFreeData</a>