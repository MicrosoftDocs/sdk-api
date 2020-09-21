---
UID: NF:p2p.PeerGraphClose
title: PeerGraphClose function (p2p.h)
description: The PeerGraphClose function invalidates the peer graph handle returned by a call to either PeerGraphCreate or PeerGraphOpen, and closes all network connections for the specified peer graph.
helpviewer_keywords: ["PeerGraphClose","PeerGraphClose function [Peer Networking]","p2p.peergraphclose","p2p/PeerGraphClose"]
old-location: p2p\peergraphclose.htm
tech.root: p2p
ms.assetid: 7600da14-7641-4b5c-b5ba-e33ffc28097c
ms.date: 12/05/2018
ms.keywords: PeerGraphClose, PeerGraphClose function [Peer Networking], p2p.peergraphclose, p2p/PeerGraphClose
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
 - PeerGraphClose
 - p2p/PeerGraphClose
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
 - PeerGraphClose
---

# PeerGraphClose function


## -description

The <b>PeerGraphClose</b> function invalidates the peer graph handle returned by a call to either <a href="/windows/desktop/api/p2p/nf-p2p-peergraphcreate">PeerGraphCreate</a> or <a href="/windows/desktop/api/p2p/nf-p2p-peergraphopen">PeerGraphOpen</a>, and closes  all network connections for the specified peer graph.

## -parameters

### -param hGraph [in]

Handle to the peer graph  to close.

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
The parameter is not valid.

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
The peer graph must be initialized with a call to <a href="/windows/desktop/api/p2p/nf-p2p-peergraphstartup">PeerGraphStartup</a> before using this function.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/p2p/nf-p2p-peergraphcreate">PeerGraphCreate</a>



<a href="/windows/desktop/api/p2p/nf-p2p-peergraphopen">PeerGraphOpen</a>