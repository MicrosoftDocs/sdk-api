---
UID: NF:p2p.PeerGraphExportDatabase
title: PeerGraphExportDatabase function (p2p.h)
description: The PeerGraphExportDatabase function exports a peer graph database into a file that you can move to a different computer. By using PeerGraphImportDatabase, a peer graph database can be imported to a different computer.
helpviewer_keywords: ["PeerGraphExportDatabase","PeerGraphExportDatabase function [Peer Networking]","p2p.peergraphexportdatabase","p2p/PeerGraphExportDatabase"]
old-location: p2p\peergraphexportdatabase.htm
tech.root: p2p
ms.assetid: 0f198952-c6d4-4da7-9086-7abd635172cb
ms.date: 12/05/2018
ms.keywords: PeerGraphExportDatabase, PeerGraphExportDatabase function [Peer Networking], p2p.peergraphexportdatabase, p2p/PeerGraphExportDatabase
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
 - PeerGraphExportDatabase
 - p2p/PeerGraphExportDatabase
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
 - PeerGraphExportDatabase
---

# PeerGraphExportDatabase function


## -description

The <b>PeerGraphExportDatabase</b> function exports a peer graph database into a file that you can move to a different computer. By using   <a href="/windows/desktop/api/p2p/nf-p2p-peergraphimportdatabase">PeerGraphImportDatabase</a>, a peer graph database can  be  imported to a different computer.

## -parameters

### -param hGraph [in]

Handle to a peer graph.

### -param pwzFilePath [in]

Pointer to a string that contains the file path  to store exported data. If a data storage file  exists and contains  data when new data is exported to it, then the new data overwrites the old data.

## -returns

If the function call succeeds, the return value is <b>S_OK</b>. Otherwise, it  returns either an error located in WinErr.h, or  one of the following values.

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
One parameter is not valid.

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
<dt><b>PEER_E_INVALID_GRAPH</b></dt>
</dl>
</td>
<td width="60%">
The handle to a graph is invalid.

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

## -remarks

If the export of a database fails because of file creation errors, a standard WinErr.h file error  is returned.

## -see-also

<a href="/windows/desktop/api/p2p/nf-p2p-peergraphimportdatabase">PeerGraphImportDatabase</a>