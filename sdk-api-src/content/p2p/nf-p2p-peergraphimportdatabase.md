---
UID: NF:p2p.PeerGraphImportDatabase
title: PeerGraphImportDatabase function (p2p.h)
description: The PeerGraphImportDatabase function imports a file that contains the information from a peer graph database. This function can only be called if the application has not yet called the PeerGraphListen or PeerGraphConnect function.
helpviewer_keywords: ["PeerGraphImportDatabase","PeerGraphImportDatabase function [Peer Networking]","p2p.peergraphimportdatabase","p2p/PeerGraphImportDatabase"]
old-location: p2p\peergraphimportdatabase.htm
tech.root: p2p
ms.assetid: 85f7dc2b-c159-48e0-ac58-8a66eb0ec73b
ms.date: 12/05/2018
ms.keywords: PeerGraphImportDatabase, PeerGraphImportDatabase function [Peer Networking], p2p.peergraphimportdatabase, p2p/PeerGraphImportDatabase
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
 - PeerGraphImportDatabase
 - p2p/PeerGraphImportDatabase
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
 - PeerGraphImportDatabase
---

# PeerGraphImportDatabase function


## -description

The <b>PeerGraphImportDatabase</b> function imports a file that contains the information from a  peer graph database. This function can only be called  if the application has not yet called the <a href="/windows/desktop/api/p2p/nf-p2p-peergraphlisten">PeerGraphListen</a> or <a href="/windows/desktop/api/p2p/nf-p2p-peergraphconnect">PeerGraphConnect</a> function.

## -parameters

### -param hGraph [in]

Handle to the peer graph.

### -param pwzFilePath [in]

Pointer to a string that contains the path to the file in which the imported data is stored.

## -returns

If the function call succeeds, the return value is S_OK. Otherwise, it  returns either one of the WinErr.h values or one of the following values.

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
<dt><b>PEER_E_GRAPH_IN_USE</b></dt>
</dl>
</td>
<td width="60%">
The graph is currently being used, and cannot be imported. Either <a href="/windows/desktop/api/p2p/nf-p2p-peergraphlisten">PeerGraphListen</a> or <a href="/windows/desktop/api/p2p/nf-p2p-peergraphconnect">PeerGraphConnect</a> has been called.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PEER_E_INVALID_DATABASE</b></dt>
</dl>
</td>
<td width="60%">
The specified database is not valid.

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
The graph must be  initialized with a call to <a href="/windows/desktop/api/p2p/nf-p2p-peergraphstartup">PeerGraphStartup</a> before using this function.

</td>
</tr>
</table>

## -remarks

The <b>PeerGraphImportDatabase</b> function cannot be used to import a database from a different peer graph. <b>PeerGraphImportDatabase</b> must be called after <a href="/windows/desktop/api/p2p/nf-p2p-peergraphopen">PeerGraphOpen</a>, not after <a href="/windows/desktop/api/p2p/nf-p2p-peergraphcreate">PeerGraphCreate</a>.

The database being imported must have the same peer graph ID and peer ID.

## -see-also

<a href="/windows/desktop/api/p2p/nf-p2p-peergraphexportdatabase">PeerGraphExportDatabase</a>