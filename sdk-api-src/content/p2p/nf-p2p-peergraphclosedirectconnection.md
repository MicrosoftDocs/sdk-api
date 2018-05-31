---
UID: NF:p2p.PeerGraphCloseDirectConnection
title: PeerGraphCloseDirectConnection function
author: windows-sdk-content
description: The PeerGraphCloseDirectConnection function closes a specified direct connection.
old-location: p2p\peergraphclosedirectconnection.htm
old-project: P2PSdk
ms.assetid: e5547292-7f6f-456c-b47a-5d5948f51a7f
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: PeerGraphCloseDirectConnection, PeerGraphCloseDirectConnection function [Peer Networking], p2p.peergraphclosedirectconnection, p2p/PeerGraphCloseDirectConnection
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
-	PeerGraphCloseDirectConnection
product: Windows
targetos: Windows
req.lib: P2PGraph.lib
req.dll: P2PGraph.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# PeerGraphCloseDirectConnection function


## -description



      The <b>PeerGraphCloseDirectConnection</b> function closes  a specified direct connection.


## -parameters




### -param hGraph [in]

Handle to a peer graph.


### -param ullConnectionId [in]

Specifies the connection ID to disconnect from.


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
One of the parameters is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PEER_E_CONNECTION_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
No connection with the specified ID exists.

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
The graph must be  initialized with a call to <a href="https://msdn.microsoft.com/00ffdec7-f084-4170-a4a1-e6112bab4d61">PeerGraphStartup</a> before using this function.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/0625a2f6-7e16-43c7-8c03-1f0ddeda426f">PeerGraphOpenDirectConnection</a>
 

 

