---
UID: NF:p2p.PeerGraphExportDatabase
title: PeerGraphExportDatabase function
author: windows-driver-content
description: The PeerGraphExportDatabase function exports a peer graph database into a file that you can move to a different computer. By using PeerGraphImportDatabase, a peer graph database can be imported to a different computer.
old-location: p2p\peergraphexportdatabase.htm
old-project: P2PSdk
ms.assetid: 0f198952-c6d4-4da7-9086-7abd635172cb
ms.author: windowsdriverdev
ms.date: 5/8/2018
ms.keywords: PeerGraphExportDatabase, PeerGraphExportDatabase function [Peer Networking], p2p.peergraphexportdatabase, p2p/PeerGraphExportDatabase
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
req.typenames: PEER_WATCH_PERMISSION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	P2PGraph.dll
api_name:
-	PeerGraphExportDatabase
product: Windows
targetos: Windows
req.lib: P2PGraph.lib
req.dll: P2PGraph.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# PeerGraphExportDatabase function


## -description



      The <b>PeerGraphExportDatabase</b> function exports a peer graph database into a file that you can move to a different computer. By using   <a href="https://msdn.microsoft.com/85f7dc2b-c159-48e0-ac58-8a66eb0ec73b">PeerGraphImportDatabase</a>, a peer graph database can  be  imported to a different computer.


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
A graph must be  initialized with a call to <a href="https://msdn.microsoft.com/00ffdec7-f084-4170-a4a1-e6112bab4d61">PeerGraphStartup</a> before using this function.

</td>
</tr>
</table>
 




## -remarks



If the export of a database fails because of file creation errors, a standard WinErr.h file error  is returned.




## -see-also




<a href="https://msdn.microsoft.com/85f7dc2b-c159-48e0-ac58-8a66eb0ec73b">PeerGraphImportDatabase</a>
 

 

