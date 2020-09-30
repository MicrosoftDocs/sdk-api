---
UID: NF:p2p.PeerGraphOpenDirectConnection
title: PeerGraphOpenDirectConnection function (p2p.h)
description: The PeerGraphOpenDirectConnection function allows an application to establish a direct connection with a node in a peer graph.
helpviewer_keywords: ["PeerGraphOpenDirectConnection","PeerGraphOpenDirectConnection function [Peer Networking]","p2p.peergraphopendirectconnection","p2p/PeerGraphOpenDirectConnection"]
old-location: p2p\peergraphopendirectconnection.htm
tech.root: p2p
ms.assetid: 0625a2f6-7e16-43c7-8c03-1f0ddeda426f
ms.date: 12/05/2018
ms.keywords: PeerGraphOpenDirectConnection, PeerGraphOpenDirectConnection function [Peer Networking], p2p.peergraphopendirectconnection, p2p/PeerGraphOpenDirectConnection
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
 - PeerGraphOpenDirectConnection
 - p2p/PeerGraphOpenDirectConnection
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
 - PeerGraphOpenDirectConnection
---

# PeerGraphOpenDirectConnection function


## -description

The <b>PeerGraphOpenDirectConnection</b> function allows an application to establish a direct connection with a node in a peer graph. The connection can only be made if the node to which  the application is connecting has subscribed to the <b>PEER_GRAPH_EVENT_DIRECT_CONNECTION</b> event. The application can then   send data directly to another node.  A call to this function is asynchronous.

## -parameters

### -param hGraph [in]

Handle to a peer graph.

### -param pwzPeerId [in]

Pointer to  the unique ID of a user or node to connect to. This parameter is used to identify a specific user because multiple identities can be attached to the specified address.

### -param pAddress [in]

Pointer to a <a href="/windows/desktop/api/p2p/ns-p2p-peer_address">PEER_ADDRESS</a> structure that contains the address of the node to  connect to.

### -param pullConnectionId [out]

Receives the connection ID for the requested connection.

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
<dt><b>PEER_E_INVALID_GRAPH</b></dt>
</dl>
</td>
<td width="60%">
The handle to the graph is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PEER_E_NOT_INITIALIZED</b></dt>
</dl>
</td>
<td width="60%">
The graph must be  initialized with a call to <a href="/windows/desktop/api/p2p/nf-p2p-peergraphstartup">PeerGraphStartup</a>—before using this function.

</td>
</tr>
</table>

## -remarks

A call to <b>PeerGraphOpenDirectConnection</b> is an asynchronous call.  A <b>PEER_GRAPH_EVENT_DIRECT_CONNECTION</b> event is triggered to inform the application of the direct connection's success or failure. The actual status of the function's success or failure is given in the <a href="/windows/desktop/api/p2p/ns-p2p-peer_graph_event_data">PEER_GRAPH_EVENT_DATA</a> structure.

## -see-also

<a href="/windows/desktop/api/p2p/ns-p2p-peer_address">PEER_ADDRESS</a>



<a href="/windows/desktop/api/p2p/nf-p2p-peergraphclosedirectconnection">PeerGraphCloseDirectConnection</a>



<a href="/windows/desktop/api/p2p/nf-p2p-peergraphenumconnections">PeerGraphEnumConnections</a>