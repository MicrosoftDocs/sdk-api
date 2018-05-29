---
UID: NF:p2p.PeerGraphSendData
title: PeerGraphSendData function
author: windows-sdk-content
description: The PeerGraphSendData function sends data to a neighbor node or a directly connected node.
old-location: p2p\peergraphsenddata.htm
old-project: P2PSdk
ms.assetid: 8ccb6f37-cb1b-41fd-a852-5a84cb5506f5
ms.author: windowssdkdev
ms.date: 05/08/2018
ms.keywords: PeerGraphSendData, PeerGraphSendData function [Peer Networking], p2p.peergraphsenddata, p2p/PeerGraphSendData
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
-	PeerGraphSendData
product: Windows
targetos: Windows
req.lib: P2PGraph.lib
req.dll: P2PGraph.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# PeerGraphSendData function


## -description



      The <b>PeerGraphSendData</b> function sends data to a  neighbor node  or a directly  connected node.


## -parameters




### -param hGraph [in]

Handle to the peer graph.


### -param ullConnectionId [in]

Specifies the unique ID of  the connection to send data on.


### -param pType [in]

Specifies an application-defined data type to send. 	This parameter cannot be <b>NULL</b>.


### -param cbData [in]

Specifies the number of bytes pointed to by <i>pvData</i>.


### -param pvData [in]

Pointer to the  data to send.


## -returns



Returns S_OK  if the operation succeeds; otherwise, the function returns one of the following values:

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
No connection with the given ID exists.

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




        The <b>PeerGraphSendData</b> function returns as soon as data has been sent to the network layer; the peer graphing layer does not wait for an acknowledgement from the other side of the connection.

<div class="alert"><b>Note</b>  In order to be able to receive data with a direct connection, an application must register for a peer event of type <b>PEER_GRAPH_EVENT_INCOMING_DATA</b>. See <a href="https://msdn.microsoft.com/3ed963ba-0b9d-4de8-a610-b07cf49ed27f">PeerGraphRegisterEvent</a>.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/ef4ea3e2-fd71-48d8-a9a8-db38ef06df20">PeerGraphEnumConnections</a>



<a href="https://msdn.microsoft.com/0625a2f6-7e16-43c7-8c03-1f0ddeda426f">PeerGraphOpenDirectConnection</a>



<a href="https://msdn.microsoft.com/3ed963ba-0b9d-4de8-a610-b07cf49ed27f">PeerGraphRegisterEvent</a>
 

 

