---
UID: NF:p2p.PeerGraphDeleteRecord
title: PeerGraphDeleteRecord function (p2p.h)
description: The PeerGraphDeleteRecord function marks a record as deleted within a peer graph. The record is not available on a local node to function calls, for example, calls to PeerGraphGetRecord and PeerGraphEnumRecords.
helpviewer_keywords: ["PeerGraphDeleteRecord","PeerGraphDeleteRecord function [Peer Networking]","p2p.peergraphdeleterecord","p2p/PeerGraphDeleteRecord"]
old-location: p2p\peergraphdeleterecord.htm
tech.root: p2p
ms.assetid: d6ecc762-8702-4366-81fc-c2b168dc8cb3
ms.date: 12/05/2018
ms.keywords: PeerGraphDeleteRecord, PeerGraphDeleteRecord function [Peer Networking], p2p.peergraphdeleterecord, p2p/PeerGraphDeleteRecord
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
 - PeerGraphDeleteRecord
 - p2p/PeerGraphDeleteRecord
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
 - PeerGraphDeleteRecord
---

# PeerGraphDeleteRecord function


## -description

The <b>PeerGraphDeleteRecord</b> function marks a record as deleted within a peer graph.  The record is not  available on a local node to function calls, for example, calls   to <a href="/windows/desktop/api/p2p/nf-p2p-peergraphgetrecord">PeerGraphGetRecord</a> and  <a href="/windows/desktop/api/p2p/nf-p2p-peergraphenumrecords">PeerGraphEnumRecords</a>.

## -parameters

### -param hGraph [in]

Handle to a peer graph.

### -param pRecordId [in]

Pointer to a record ID to delete.

### -param fLocal [in]

Specify <b>TRUE</b> to remove a record from only  a local database without notifying the rest of  a peer graph about the change.  Specify FALSE to delete the record from an entire peer graph.

<div class="alert"><b>Note</b>   Specifying <b>TRUE</b> does not prevent  a record from being added again during the next graph synchronization with a neighbor. Specifying <b>TRUE</b> is only effective if PEER_SECURITY_INTERFACE is specified in a call to <a href="/windows/desktop/api/p2p/nf-p2p-peergraphopen">PeerGraphOpen</a> or <a href="/windows/desktop/api/p2p/nf-p2p-peergraphcreate">PeerGraphCreate</a>, and only if  PEER_SECURITY_INTERFACE contains a <a href="/windows/desktop/api/p2p/nc-p2p-pfnpeer_validate_record">PFNPEER_VALIDATE_RECORD</a> function that returns PEER_E_INVALID_RECORD when validating the record.</div>
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
Cannot access a  peer graph.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PEER_E_GRAPH_NOT_READY</b></dt>
</dl>
</td>
<td width="60%">
The peer graph is not synchronized. Records cannot be deleted until the graph is synchronized.

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
The peer graph must be initialized with a call to <a href="/windows/desktop/api/p2p/nf-p2p-peergraphstartup">PeerGraphStartup</a> before using this function.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PEER_E_RECORD_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The specified record cannot be found.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/p2p/nf-p2p-peergraphgetrecord">PeerGraphAddRecord</a>



<a href="/windows/desktop/api/p2p/nf-p2p-peergraphenumrecords">PeerGraphEnumRecords</a>



<b>PeerGraphGetRecord</b>



<a href="/windows/desktop/api/p2p/nf-p2p-peergraphupdaterecord">PeerGraphUpdateRecord</a>