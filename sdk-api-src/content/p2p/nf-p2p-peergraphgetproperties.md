---
UID: NF:p2p.PeerGraphGetProperties
title: PeerGraphGetProperties function (p2p.h)
description: The PeerGraphGetProperties function retrieves the current peer graph properties.
helpviewer_keywords: ["PeerGraphGetProperties","PeerGraphGetProperties function [Peer Networking]","p2p.peergraphgetproperties","p2p/PeerGraphGetProperties"]
old-location: p2p\peergraphgetproperties.htm
tech.root: p2p
ms.assetid: f62fadf8-8cc2-4597-93b0-e076258ccd6a
ms.date: 12/05/2018
ms.keywords: PeerGraphGetProperties, PeerGraphGetProperties function [Peer Networking], p2p.peergraphgetproperties, p2p/PeerGraphGetProperties
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
 - PeerGraphGetProperties
 - p2p/PeerGraphGetProperties
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
 - PeerGraphGetProperties
---

# PeerGraphGetProperties function


## -description

The <b>PeerGraphGetProperties</b> function retrieves the current peer graph properties.

## -parameters

### -param hGraph [in]

Handle to a peer graph.

### -param ppGraphProperties [out]

Receives a pointer to a <a href="/windows/desktop/api/p2p/ns-p2p-peer_graph_properties">PEER_GRAPH_PROPERTIES</a> structure.  When the structure is not needed, free it by calling <a href="/windows/desktop/api/p2p/nf-p2p-peergraphfreedata">PeerGraphFreeData</a>.

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
<dt><b>PEER_E_GRAPH_NOT_READY</b></dt>
</dl>
</td>
<td width="60%">
The graph is not synchronized. Data cannot be retrieved until a peer graph is synchronized.

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
A peer graph must be  initialized with a call to <a href="/windows/desktop/api/p2p/nf-p2p-peergraphstartup">PeerGraphStartup</a> before using this function.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/p2p/ns-p2p-peer_graph_properties">PEER_GRAPH_PROPERTIES</a>



<a href="/windows/desktop/api/p2p/nf-p2p-peergraphcreate">PeerGraphCreate</a>



<a href="/windows/desktop/api/p2p/nf-p2p-peergraphfreedata">PeerGraphFreeData</a>