---
UID: NF:p2p.PeerGraphConnect
title: PeerGraphConnect function
author: windows-driver-content
description: The PeerGraphConnect function attempts to make a connection to a specified node in a peer graph.
old-location: p2p\peergraphconnect.htm
old-project: P2PSdk
ms.assetid: 76a2c54d-4424-4aa3-9b62-3ebe88b63c9f
ms.author: windowsdriverdev
ms.date: 4/23/2018
ms.keywords: PeerGraphConnect, PeerGraphConnect function [Peer Networking], p2p.peergraphconnect, p2p/PeerGraphConnect
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
-	PeerGraphConnect
product: Windows
targetos: Windows
req.lib: P2PGraph.lib
req.dll: P2PGraph.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# PeerGraphConnect function


## -description



      The <b>PeerGraphConnect</b> function attempts to make a connection to a specified node in a peer graph.  This function starts an asynchronous operation.  The calling application must wait for a <b>PEER_GRAPH_EVENT_NEIGHBOR_CONNECTION</b>  event to determine if the connection attempt is successful.


## -parameters




### -param hGraph [in]

Handle to a peer graph.


### -param pwzPeerId [in]

The unique ID of a peer to connect to at  <i>pAddress</i>. Specify <b>NULL</b> to connect to any peer listening at a specified address in the same peer graph.


### -param pAddress [in]

Pointer to a <a href="https://msdn.microsoft.com/09476d3b-ec65-40a2-90ee-a20be230deca">PEER_ADDRESS</a> structure that identifies a node to connect to.


### -param pullConnectionId [out]

Receives the pointer to an <b>ULONGLONG</b> that contains  the connection ID. This ID can be used with the direct communication functions.


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
<dt><b>PEER_E_ALREADY_EXISTS</b></dt>
</dl>
</td>
<td width="60%">
A neighbor connection to a specified node already exists.

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
A graph must be  initialized with a call to <a href="https://msdn.microsoft.com/00ffdec7-f084-4170-a4a1-e6112bab4d61">PeerGraphStartup</a> before using this function.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/09476d3b-ec65-40a2-90ee-a20be230deca">
        PEER_ADDRESS</a>



<a href="https://msdn.microsoft.com/b64bb920-3fbc-4927-a1b1-39c99850bdd5">PeerGraphGetEventData</a>



<a href="https://msdn.microsoft.com/bac893d4-8f4d-4e1f-953b-1b289c5f18be">PeerGraphListen</a>



<a href="https://msdn.microsoft.com/0625a2f6-7e16-43c7-8c03-1f0ddeda426f">PeerGraphOpenDirectConnection</a>



<a href="https://msdn.microsoft.com/8ccb6f37-cb1b-41fd-a852-5a84cb5506f5">PeerGraphSendData</a>
 

 

