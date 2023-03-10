---
UID: NF:p2p.PeerGraphSetProperties
title: PeerGraphSetProperties function (p2p.h)
description: The PeerGraphSetProperties function sets the peer graph properties.
helpviewer_keywords: ["PeerGraphSetProperties","PeerGraphSetProperties function [Peer Networking]","p2p.peergraphsetproperties","p2p/PeerGraphSetProperties"]
old-location: p2p\peergraphsetproperties.htm
tech.root: p2p
ms.assetid: a9cdf715-bbef-4b5b-96b9-b7c1e35c76ec
ms.date: 12/05/2018
ms.keywords: PeerGraphSetProperties, PeerGraphSetProperties function [Peer Networking], p2p.peergraphsetproperties, p2p/PeerGraphSetProperties
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
 - PeerGraphSetProperties
 - p2p/PeerGraphSetProperties
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
 - PeerGraphSetProperties
---

# PeerGraphSetProperties function


## -description

The <b>PeerGraphSetProperties</b> function sets the peer graph properties.

## -parameters

### -param hGraph [in]

Handle to a graph.

### -param pGraphProperties [in]

Pointer to a <a href="/windows/desktop/api/p2p/ns-p2p-peer_graph_properties">PEER_GRAPH_PROPERTIES</a> structure that specifies new values for   the graph properties  that an application can set.

An application can set only the following fields of <a href="/windows/desktop/api/p2p/ns-p2p-peer_graph_properties">PEER_GRAPH_PROPERTIES</a>:<ul>
<li><b>pwzFriendlyName</b></li>
<li><b>cPresenceMax</b></li>
<li><b>pwzComment</b></li>
<li><b>ulPresenceLifetime</b></li>
</ul>
<div class="alert"><b>Note</b>   If remaining fields are set, then they are ignored.</div>
<div> </div>

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
<dt><b>E_ACCESSDENIED</b></dt>
</dl>
</td>
<td width="60%">
Cannot access a peer  graph.

</td>
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
The graph must be  initialized with a call to <a href="/windows/desktop/api/p2p/nf-p2p-peergraphstartup">PeerGraphStartup</a> before using this function.

</td>
</tr>
</table>

## -remarks

You can modify
the <b>pwzFriendlyName</b>,
<b>cPresenceMax</b>, <b>pwzComment</b> and
<b>ulPresenceLifetime</b> members of the <a href="/windows/desktop/api/p2p/ns-p2p-peer_graph_properties">PEER_GRAPH_PROPERTIES</a> structure.

## -see-also

<a href="/windows/desktop/api/p2p/ns-p2p-peer_graph_properties">PEER_GRAPH_PROPERTIES</a>



<a href="/windows/desktop/api/p2p/nf-p2p-peergraphcreate">PeerGraphCreate</a>



<a href="/windows/desktop/api/p2p/nf-p2p-peergraphgetproperties">PeerGraphGetProperties</a>