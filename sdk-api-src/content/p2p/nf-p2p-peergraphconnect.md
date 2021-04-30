---
UID: NF:p2p.PeerGraphConnect
title: PeerGraphConnect function (p2p.h)
description: The PeerGraphConnect function attempts to make a connection to a specified node in a peer graph.
helpviewer_keywords: ["PeerGraphConnect","PeerGraphConnect function [Peer Networking]","p2p.peergraphconnect","p2p/PeerGraphConnect"]
old-location: p2p\peergraphconnect.htm
tech.root: p2p
ms.assetid: 76a2c54d-4424-4aa3-9b62-3ebe88b63c9f
ms.date: 12/05/2018
ms.keywords: PeerGraphConnect, PeerGraphConnect function [Peer Networking], p2p.peergraphconnect, p2p/PeerGraphConnect
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
 - PeerGraphConnect
 - p2p/PeerGraphConnect
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
 - PeerGraphConnect
---

# PeerGraphConnect function


## -description

The <b>PeerGraphConnect</b> function attempts to make a connection to a specified node in a peer graph.  This function starts an asynchronous operation.  The calling application must wait for a <b>PEER_GRAPH_EVENT_NEIGHBOR_CONNECTION</b>  event to determine if the connection attempt is successful.

## -parameters

### -param hGraph [in]

Handle to a peer graph.

### -param pwzPeerId [in]

The unique ID of a peer to connect to at  <i>pAddress</i>. Specify <b>NULL</b> to connect to any peer listening at a specified address in the same peer graph.

### -param pAddress [in]

Pointer to a <a href="/windows/desktop/api/p2p/ns-p2p-peer_address">PEER_ADDRESS</a> structure that identifies a node to connect to.

### -param pullConnectionId [out]

Receives the pointer to an <b>ULONGLONG</b> that contains  the connection ID. This ID can be used with the direct communication functions.

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
<dt><b>PEER_E_ALREADY_EXISTS</b></dt>
</dl>
</td>
<td width="60%">
A neighbor connection to a specified node already exists.

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
A graph must be  initialized with a call to <a href="/windows/desktop/api/p2p/nf-p2p-peergraphstartup">PeerGraphStartup</a> before using this function.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/p2p/ns-p2p-peer_address">PEER_ADDRESS</a>



<a href="/windows/desktop/api/p2p/nf-p2p-peergraphgeteventdata">PeerGraphGetEventData</a>



<a href="/windows/desktop/api/p2p/nf-p2p-peergraphlisten">PeerGraphListen</a>



<a href="/windows/desktop/api/p2p/nf-p2p-peergraphopendirectconnection">PeerGraphOpenDirectConnection</a>



<a href="/windows/desktop/api/p2p/nf-p2p-peergraphsenddata">PeerGraphSendData</a>