---
UID: NF:p2p.PeerGraphCreate
title: PeerGraphCreate function (p2p.h)
description: The PeerGraphCreate function creates a new peer graph. An application can specify information about a peer graph, and the type of security that a peer graph uses. A handle to a peer graph is returned, but a network connection is not established.
helpviewer_keywords: ["PeerGraphCreate","PeerGraphCreate function [Peer Networking]","p2p.peergraphcreate","p2p/PeerGraphCreate"]
old-location: p2p\peergraphcreate.htm
tech.root: p2p
ms.assetid: 62e3ec57-378c-4322-9ad4-a40d98e03dab
ms.date: 12/05/2018
ms.keywords: PeerGraphCreate, PeerGraphCreate function [Peer Networking], p2p.peergraphcreate, p2p/PeerGraphCreate
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
 - PeerGraphCreate
 - p2p/PeerGraphCreate
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
 - PeerGraphCreate
---

# PeerGraphCreate function


## -description

The <b>PeerGraphCreate</b> function creates a  new peer graph.  An application can  specify information about a peer graph, and the type of security that a  peer graph uses. A handle to a peer graph is returned, but a network connection is not established.

## -parameters

### -param pGraphProperties [in]

All of the properties of a peer graph in the <a href="/windows/desktop/api/p2p/ns-p2p-peer_graph_properties">PEER_GRAPH_PROPERTIES</a> structure.

### -param pwzDatabaseName [in]

The name of a record database to associate with a peer graph when it is created. The record database name must be a valid file name. Do not include a path with the file name.  For a complete list of rules regarding file names, see  the Naming a File item in the list of  <a href="/windows/desktop/P2PSdk/graphing-reference-links">Graphing Reference_Links</a>.

### -param pSecurityInterface [in]

The information about a security provider for a peer graph in the <a href="/windows/desktop/api/p2p/ns-p2p-peer_security_interface">PEER_SECURITY_INTERFACE</a> structure.

### -param phGraph [out]

Receives a handle to the peer graph that is created. When this handle is not required anymore, free it by calling <a href="/windows/desktop/api/p2p/nf-p2p-peergraphclose">PeerGraphClose</a>.

## -returns

Returns <b>S_OK</b> if the operation succeeds. Otherwise, the function returns one of the following values.

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
<dt><b>PEER_E_DUPLICATE_GRAPH</b></dt>
</dl>
</td>
<td width="60%">
A database with a specified peer graph ID that already exists.

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

If you develop your own Security Service Provider (SSP), your application must not call the Peer Graphing API to access data in the peer graphing database, because that can cause a deadlock situation.  Instead, the application must use a cached copy of the information. The cached copy is not created by the Peer Graphing API. The application must provide a mechanism for caching this data.

After   <b>PeerGraphCreate</b> is called, the  application can subscribe to events before it calls <a href="/windows/desktop/api/p2p/nf-p2p-peergraphlisten">PeerGraphListen</a>.

## -see-also

<a href="/windows/desktop/api/p2p/ns-p2p-peer_graph_properties">PEER_GRAPH_PROPERTIES</a>



<a href="/windows/desktop/api/p2p/ns-p2p-peer_security_interface">PEER_SECURITY_INTERFACE</a>



<a href="/windows/desktop/api/p2p/nf-p2p-peergraphclose">PeerGraphClose</a>



<a href="/windows/desktop/api/p2p/nf-p2p-peergraphconnect">PeerGraphConnect</a>



<a href="/windows/desktop/api/p2p/nf-p2p-peergraphlisten">PeerGraphListen</a>



<a href="/windows/desktop/api/p2p/nf-p2p-peergraphopen">PeerGraphOpen</a>