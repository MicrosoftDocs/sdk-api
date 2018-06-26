---
UID: NF:p2p.PeerCollabSubscribeEndpointData
title: PeerCollabSubscribeEndpointData function
author: windows-sdk-content
description: Creates a subscription to an available endpoint.
old-location: p2p\peercollabsubscribeendpointdata.htm
old-project: P2PSdk
ms.assetid: dfe17235-34dd-4694-9ee5-4268b4406731
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: PeerCollabSubscribeEndpointData, PeerCollabSubscribeEndpointData function [Peer Networking], p2p.peercollabsubscribeendpointdata, p2p/PeerCollabSubscribeEndpointData
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: PEER_WATCH_PERMISSION
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - P2P.dll
api_name:
 - PeerCollabSubscribeEndpointData
product: Windows
targetos: Windows
req.lib: P2P.lib
req.dll: P2P.dll
req.irql: 
req.product: ADAM
---

# PeerCollabSubscribeEndpointData function


## -description


The <b>PeerCollabSubscribeEndpointData</b> function creates  a subscription to an available endpoint.


## -parameters




### -param pcEndpoint [in]

Pointer to a <a href="https://msdn.microsoft.com/9687b332-14ed-4023-b8c2-437d75fd0298">PEER_ENDPOINT</a> structure that contains the peer endpoint used to obtain presence information.


## -returns



Returns S_OK or PEER_S_SUBSCRIPTION_EXISTS  if the function succeeds. Otherwise, the function returns one of the following values.

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



<b>PeerCollabSubscribeEndpointData</b> is an asynchronous call, meaning that the process to subscribe the endpoint has been started but not necessarily completed when this call returns. An application should wait for PEER_EVENT_REQUEST_STATUS_CHANGED to get the result of the subscription request.

This function will timeout at 30 seconds.

<b>PeerCollabSubscribeEndpointData</b> can be called multiple times from different applications for the same endpoint. Each call is reference counted; only when the last reference is released is a peer unsubscribed. To release the reference call <b>PeerCollabUnsubscribeEndpointData</b>.

When an application exits without calling <a href="https://msdn.microsoft.com/af07c7f5-bce2-4479-ad2a-8e501cfb6710">PeerCollabUnsubscribeEndpointData</a>, all of the references for that application are released automatically.

To successfully call the <a href="https://msdn.microsoft.com/596191a1-94cf-4497-aaf0-951e2c63b145">PeerCollabGetPresenceInfo</a>, <a href="https://msdn.microsoft.com/550cbd9d-5569-485e-897d-73d8bab8430a">PeerCollabEnumApplications</a>, <a href="https://msdn.microsoft.com/a9ac2603-b007-4d1c-ac11-c72aeb06e663">PeerCollabEnumObjects</a>, and <a href="https://msdn.microsoft.com/278c7622-988e-441d-a6b9-f62947f881e8">PeerCollabQueryContactData</a> APIs, an application must first call <b>PeerCollabSubscribeEndpointData</b>.




## -see-also




<a href="https://msdn.microsoft.com/550cbd9d-5569-485e-897d-73d8bab8430a">PeerCollabEnumApplications</a>



<a href="https://msdn.microsoft.com/a9ac2603-b007-4d1c-ac11-c72aeb06e663">PeerCollabEnumObjects</a>



<a href="https://msdn.microsoft.com/596191a1-94cf-4497-aaf0-951e2c63b145">PeerCollabGetPresenceInfo</a>



<a href="https://msdn.microsoft.com/278c7622-988e-441d-a6b9-f62947f881e8">PeerCollabQueryContactData</a>



<a href="https://msdn.microsoft.com/af07c7f5-bce2-4479-ad2a-8e501cfb6710">PeerCollabUnsubscribeEndpointData</a>
 

 

