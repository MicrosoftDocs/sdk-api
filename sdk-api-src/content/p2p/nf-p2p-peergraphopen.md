---
UID: NF:p2p.PeerGraphOpen
title: PeerGraphOpen function (p2p.h)
description: The PeerGraphOpen function opens a peer graph that is created previously by either the local node or a remote node. A handle to the peer graph is returned, but a network connection is not established.
helpviewer_keywords: ["PeerGraphOpen","PeerGraphOpen function [Peer Networking]","p2p.peergraphopen","p2p/PeerGraphOpen"]
old-location: p2p\peergraphopen.htm
tech.root: p2p
ms.assetid: a34656f1-3e29-4bcb-a8a7-0eed19368184
ms.date: 12/05/2018
ms.keywords: PeerGraphOpen, PeerGraphOpen function [Peer Networking], p2p.peergraphopen, p2p/PeerGraphOpen
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
 - PeerGraphOpen
 - p2p/PeerGraphOpen
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
 - PeerGraphOpen
---

# PeerGraphOpen function


## -description

The <b>PeerGraphOpen</b> function opens a peer graph that is created  previously by either the local node or a remote node. A handle to the peer graph is returned, but a network connection is not established.

## -parameters

### -param pwzGraphId [in]

Specifies the ID of the peer graph to open. This identifier must be the same as the ID used in the call to <a href="/windows/desktop/api/p2p/nf-p2p-peergraphcreate">PeerGraphCreate</a>.

<div class="alert"><b>Note</b>  A peer who specifies an invalid (long)  graph ID  can open and connect successfully to a graph, but the peer cannot publish records to the graph, because the records cannot be validated.
</div>
<div> </div>

### -param pwzPeerId [in]

Specifies the unique ID of the peer opening the graph.

<div class="alert"><b>Note</b>  A peer who specifies an invalid (long)  graph ID  can open and connect successfully to a graph, but the peer cannot publish records to the graph, because the records cannot be validated.</div>
<div> </div>

### -param pwzDatabaseName [in]

Specifies the name of the database that is associated with this peer graph at the time the graph was  created or opened for the first time.

### -param pSecurityInterface [in]

Specifies the security provider for a peer graph.  This parameter must specify the same value as  the <i>pSecurityInterface</i> specified in the original call to <a href="/windows/desktop/api/p2p/nf-p2p-peergraphcreate">PeerGraphCreate</a>.

### -param cRecordTypeSyncPrecedence [in]

Specifies the number of record types in the <i>pRecordTypeSyncPrecedence</i> parameter.

### -param pRecordTypeSyncPrecedence [in]

Points to an array of record types.  This array specifies the order  in which records of the specified record types are synchronized. The order can be zero (0) to N, where 0 is the first record type to be synchronized.  If a record type is not specified in the array, it is  synchronized in the default order after the types specified in the array are synchronized.

Specify <b>NULL</b> to use the default order. This parameter must be <b>NULL</b> if <i>cRecordTypeSyncPrecedence</i> is zero (0).

### -param phGraph [out]

Receives a handle to the peer graph that is opened. When this handle is not required or needed, free it by calling <a href="/windows/desktop/api/p2p/nf-p2p-peergraphclose">PeerGraphClose</a>.

## -returns

Returns S_OK  if an existing database was successfully opened. Otherwise, the function returns one of the following values:

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
There is not enough memory to perform the specified operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PEER_S_GRAPH_DATA_CREATED</b></dt>
</dl>
</td>
<td width="60%">
An existing database is not found, and a new one is created successfully. If an existing database is found and opened successfully, <b>S_OK</b> is returned.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PEER_E_INVALID_GRAPH</b></dt>
</dl>
</td>
<td width="60%">
The handle to the peer graph is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PEER_E_NOT_INITIALIZED</b></dt>
</dl>
</td>
<td width="60%">
The peer graph must be  initialized by using a call to <a href="/windows/desktop/api/p2p/nf-p2p-peergraphstartup">PeerGraphStartup</a> before using this function.

</td>
</tr>
</table>

## -remarks

If you have developed your own SSP, your application must not call the PeerGraphing API to access data in the graphing database, because that can lead to a deadlock situation.  Instead, the application should look at a cached copy of the information.

After   <b>PeerGraphOpen</b> is called, an  application can subscribe to events or import a database, or both.

Until a peer graph is synchronized at least one time, many functions are not available (for example, <a href="/windows/desktop/api/p2p/nf-p2p-peergraphlisten">PeerGraphListen</a> or any of the record management functions), and any calls made to these functions fail. A peer graph is  synchronized at least one time when one of the following occurs:

<ul>
<li>A call to <b>PeerGraphOpen</b> returns <b>S_OK</b>, which means that  an already synchronized database has been found.</li>
<li>The <a href="/windows/desktop/api/p2p/nf-p2p-peergraphcreate">PeerGraphCreate</a>  function has been called.</li>
<li>The <b>PEER_GRAPH_EVENT_STATUS_CHANGED</b> event has been triggered, and  the PEER_GRAPH_STATUS_SYNCHRONIZED flag of the   <b>dwStatus</b> member has been set.</li>
</ul>

## -see-also

<a href="/windows/desktop/api/p2p/ns-p2p-peer_security_interface">PEER_SECURITY_INTERFACE</a>



<a href="/windows/desktop/api/p2p/nf-p2p-peergraphclose">PeerGraphClose</a>



<a href="/windows/desktop/api/p2p/nf-p2p-peergraphcreate">PeerGraphCreate</a>



<a href="/windows/desktop/api/p2p/nf-p2p-peergraphlisten">PeerGraphListen</a>