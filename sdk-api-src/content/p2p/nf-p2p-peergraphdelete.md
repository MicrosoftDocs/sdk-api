---
UID: NF:p2p.PeerGraphDelete
title: PeerGraphDelete function (p2p.h)
description: The PeerGraphDelete function deletes the data associated with a specified peer graph.
helpviewer_keywords: ["PeerGraphDelete","PeerGraphDelete function [Peer Networking]","p2p.peergraphdelete","p2p/PeerGraphDelete"]
old-location: p2p\peergraphdelete.htm
tech.root: p2p
ms.assetid: 7962e425-ca74-4695-a394-5495e74bd460
ms.date: 12/05/2018
ms.keywords: PeerGraphDelete, PeerGraphDelete function [Peer Networking], p2p.peergraphdelete, p2p/PeerGraphDelete
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
 - PeerGraphDelete
 - p2p/PeerGraphDelete
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
 - PeerGraphDelete
---

# PeerGraphDelete function


## -description

The <b>PeerGraphDelete</b> function deletes the data  associated with a specified peer graph.

## -parameters

### -param pwzGraphId [in]

The name of a peer graph to delete data for.  Specify the same ID used in calls to <a href="/windows/desktop/api/p2p/nf-p2p-peergraphcreate">PeerGraphCreate</a> or <a href="/windows/desktop/api/p2p/nf-p2p-peergraphopen">PeerGraphOpen</a>.

### -param pwzPeerId [in]

The peer ID to delete  data for. Specify the same ID used in calls to  <a href="/windows/desktop/api/p2p/nf-p2p-peergraphcreate">PeerGraphCreate</a> or <a href="/windows/desktop/api/p2p/nf-p2p-peergraphopen">PeerGraphOpen</a>.

### -param pwzDatabaseName [in]

The name of  a database associated with a peer graph. Specify the same ID used in calls to  <a href="/windows/desktop/api/p2p/nf-p2p-peergraphcreate">PeerGraphCreate</a> or <a href="/windows/desktop/api/p2p/nf-p2p-peergraphopen">PeerGraphOpen</a>.

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
Access to a  graph is denied.

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
<dt><b>PEER_E_NOT_INITIALIZED</b></dt>
</dl>
</td>
<td width="60%">
A graph must be initialized with a call to <a href="/windows/desktop/api/p2p/nf-p2p-peergraphstartup">PeerGraphStartup</a> before using this function.

</td>
</tr>
</table>

## -remarks

A peer graph must be closed by using <a href="/windows/desktop/api/p2p/nf-p2p-peergraphclose">PeerGraphClose</a> before it can be deleted.

If  a delete operation fails, a Windows file error code is returned.

## -see-also

<a href="/windows/desktop/api/p2p/nf-p2p-peergraphclose">PeerGraphClose</a>



<a href="/windows/desktop/api/p2p/nf-p2p-peergraphcreate">PeerGraphCreate</a>



<a href="/windows/desktop/api/p2p/nf-p2p-peergraphopen">PeerGraphOpen</a>



<a href="/windows/desktop/api/p2p/nf-p2p-peergraphstartup">PeerGraphStartup</a>