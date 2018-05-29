---
UID: NF:p2p.PeerGraphImportDatabase
title: PeerGraphImportDatabase function
author: windows-sdk-content
description: The PeerGraphImportDatabase function imports a file that contains the information from a peer graph database. This function can only be called if the application has not yet called the PeerGraphListen or PeerGraphConnect function.
old-location: p2p\peergraphimportdatabase.htm
old-project: P2PSdk
ms.assetid: 85f7dc2b-c159-48e0-ac58-8a66eb0ec73b
ms.author: windowssdkdev
ms.date: 05/08/2018
ms.keywords: PeerGraphImportDatabase, PeerGraphImportDatabase function [Peer Networking], p2p.peergraphimportdatabase, p2p/PeerGraphImportDatabase
ms.prod: windows
ms.technology: windows-sdk
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
-	PeerGraphImportDatabase
product: Windows
targetos: Windows
req.lib: P2PGraph.lib
req.dll: P2PGraph.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# PeerGraphImportDatabase function


## -description



      The <b>PeerGraphImportDatabase</b> function imports a file that contains the information from a  peer graph database. This function can only be called  if the application has not yet called the <a href="https://msdn.microsoft.com/bac893d4-8f4d-4e1f-953b-1b289c5f18be">PeerGraphListen</a> or <a href="https://msdn.microsoft.com/76a2c54d-4424-4aa3-9b62-3ebe88b63c9f">PeerGraphConnect</a> function.


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
The graph is currently being used, and cannot be imported. Either <a href="https://msdn.microsoft.com/bac893d4-8f4d-4e1f-953b-1b289c5f18be">PeerGraphListen</a> or <a href="https://msdn.microsoft.com/76a2c54d-4424-4aa3-9b62-3ebe88b63c9f">PeerGraphConnect</a> has been called.

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
The graph must be  initialized with a call to <a href="https://msdn.microsoft.com/00ffdec7-f084-4170-a4a1-e6112bab4d61">PeerGraphStartup</a> before using this function.

</td>
</tr>
</table>
 




## -remarks



The <b>PeerGraphImportDatabase</b> function cannot be used to import a database from a different peer graph. <b>PeerGraphImportDatabase</b> must be called after <a href="https://msdn.microsoft.com/a34656f1-3e29-4bcb-a8a7-0eed19368184">PeerGraphOpen</a>, not after <a href="https://msdn.microsoft.com/62e3ec57-378c-4322-9ad4-a40d98e03dab">PeerGraphCreate</a>.

The database being imported must have the same peer graph ID and peer ID.




## -see-also




<a href="https://msdn.microsoft.com/0f198952-c6d4-4da7-9086-7abd635172cb">PeerGraphExportDatabase</a>
 

 

