---
UID: NF:p2p.PeerGraphGetRecord
title: PeerGraphGetRecord function (p2p.h)
description: The PeerGraphGetRecord function retrieves a specific record based on the specified record ID. The returned record should be freed by calling PeerGraphFreeData.
helpviewer_keywords: ["PeerGraphGetRecord","PeerGraphGetRecord function [Peer Networking]","p2p.peergraphgetrecord","p2p/PeerGraphGetRecord"]
old-location: p2p\peergraphgetrecord.htm
tech.root: p2p
ms.assetid: 5e777c02-980c-42f9-add7-9568c86c2efe
ms.date: 12/05/2018
ms.keywords: PeerGraphGetRecord, PeerGraphGetRecord function [Peer Networking], p2p.peergraphgetrecord, p2p/PeerGraphGetRecord
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
 - PeerGraphGetRecord
 - p2p/PeerGraphGetRecord
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
 - PeerGraphGetRecord
---

# PeerGraphGetRecord function


## -description

The <b>PeerGraphGetRecord</b> function retrieves a specific record based on the specified record ID. The returned record should be freed by calling <a href="/windows/desktop/api/p2p/nf-p2p-peergraphfreedata">PeerGraphFreeData</a>.

## -parameters

### -param hGraph [in]

Handle to the peer graph.

### -param pRecordId [in]

Pointer to record ID to retrieve.

### -param ppRecord [out]

Receives the requested record. When this structure is no longer required, free it by calling <a href="/windows/desktop/api/p2p/nf-p2p-peergraphfreedata">PeerGraphFreeData</a>.

## -returns

If the function call succeeds, the return value is S_OK. Otherwise, it  returns one of the following values.

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
<dt><b>PEER_E_GRAPH_NOT_READY</b></dt>
</dl>
</td>
<td width="60%">
The peer graph has never been synchronized. Records cannot be retrieved until the peer graph has been synchronized.

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
The peer graph must be  initialized with a call to <a href="/windows/desktop/api/p2p/nf-p2p-peergraphstartup">PeerGraphStartup</a> before using this function.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PEER_E_RECORD_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The specified record was not found.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/p2p/ns-p2p-peer_record">PEER_RECORD</a>



<a href="/windows/desktop/api/p2p/nf-p2p-peergraphfreedata">PeerGraphFreeData</a>