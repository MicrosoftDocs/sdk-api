---
UID: NF:p2p.PeerCollabUnsubscribeEndpointData
title: PeerCollabUnsubscribeEndpointData function
author: windows-driver-content
description: Removes a subscription to an endpoint created with PeerCollabSubscribeEndpointData.
old-location: p2p\peercollabunsubscribeendpointdata.htm
old-project: P2PSdk
ms.assetid: af07c7f5-bce2-4479-ad2a-8e501cfb6710
ms.author: windowsdriverdev
ms.date: 4/23/2018
ms.keywords: PeerCollabUnsubscribeEndpointData, PeerCollabUnsubscribeEndpointData function [Peer Networking], p2p.peercollabunsubscribeendpointdata, p2p/PeerCollabUnsubscribeEndpointData
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: p2p.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
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
-	P2P.dll
api_name:
-	PeerCollabUnsubscribeEndpointData
product: Windows
targetos: Windows
req.lib: P2P.lib
req.dll: P2P.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# PeerCollabUnsubscribeEndpointData function


## -description


The <b>PeerCollabUnsubscribeEndpointData</b> function  removes a  subscription to an endpoint created with <a href="https://msdn.microsoft.com/dfe17235-34dd-4694-9ee5-4268b4406731">PeerCollabSubscribeEndpointData</a>.


## -parameters




### -param pcEndpoint [in]

Pointer to a <a href="https://msdn.microsoft.com/9687b332-14ed-4023-b8c2-437d75fd0298">PEER_ENDPOINT</a> structure that contains the peer endpoint that is used to remove the subscription.


## -returns



Returns S_OK if the function succeeds. Otherwise, the function returns one of the following values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
There is not enough memory to support this operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One of the arguments is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PEER_E_NOT_INITIALIZED</b></dt>
</dl>
</td>
<td width="60%">
The Windows Peer infrastructure is not initialized. Calling the relevant initialization function  is required.

</td>
</tr>
</table>
 




## -remarks



Each call is reference counted. As a result, the peer is unsubscribed only when the last reference is released.

The <b>PeerCollabUnsubscribeEndpointData</b> function will timeout at 30 seconds.




## -see-also




<a href="https://msdn.microsoft.com/dfe17235-34dd-4694-9ee5-4268b4406731">PeerCollabSubscribeEndpointData</a>
 

 

