---
UID: NF:p2p.PeerGraphGetStatus
title: PeerGraphGetStatus function
author: windows-driver-content
description: The PeerGraphGetStatus function returns the current status of the peer graph.
old-location: p2p\peergraphgetstatus.htm
old-project: P2PSdk
ms.assetid: a7d23640-4f69-4ce0-996f-562807db7768
ms.author: windowsdriverdev
ms.date: 5/8/2018
ms.keywords: PeerGraphGetStatus, PeerGraphGetStatus function [Peer Networking], p2p.peergraphgetstatus, p2p/PeerGraphGetStatus
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
-	PeerGraphGetStatus
product: Windows
targetos: Windows
req.lib: P2PGraph.lib
req.dll: P2PGraph.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# PeerGraphGetStatus function


## -description



      The <b>PeerGraphGetStatus</b> function returns the current status of the peer graph.


## -parameters




### -param hGraph [in]

Handle to the peer graph.


### -param pdwStatus [out]

Receives the current status of the peer graph.  Returns one or more of the <a href="https://msdn.microsoft.com/71910437-4ebd-4fcc-977c-0a56c5f26d61">PEER_GRAPH_STATUS_FLAGS</a> values.


## -returns



This function can return one of these values.

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
The peer graph must be  initialized with a call to <a href="https://msdn.microsoft.com/00ffdec7-f084-4170-a4a1-e6112bab4d61">PeerGraphStartup</a> before using this function.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/71910437-4ebd-4fcc-977c-0a56c5f26d61">PEER_GRAPH_STATUS_FLAGS</a>
 

 

