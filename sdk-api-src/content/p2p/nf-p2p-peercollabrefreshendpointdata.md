---
UID: NF:p2p.PeerCollabRefreshEndpointData
title: PeerCollabRefreshEndpointData function
author: windows-driver-content
description: Updates the calling peer node with new endpoint data.
old-location: p2p\peercollabrefreshendpointdata.htm
old-project: P2PSdk
ms.assetid: ba841da4-de7f-4288-84b7-a06370b55e3c
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: PeerCollabRefreshEndpointData, PeerCollabRefreshEndpointData function [Peer Networking], p2p.peercollabrefreshendpointdata, p2p/PeerCollabRefreshEndpointData
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
-	PeerCollabRefreshEndpointData
product: Windows
targetos: Windows
req.lib: P2P.lib
req.dll: P2P.dll
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# PeerCollabRefreshEndpointData function


## -description


The <b>PeerCollabRefreshEndpointData</b> function updates the calling peer node with new endpoint data.


## -parameters




### -param pcEndpoint [in]

Pointer to a <a href="https://msdn.microsoft.com/9687b332-14ed-4023-b8c2-437d75fd0298">PEER_ENDPOINT</a> structure that contains the updated peer endpoint information for the current peer node.


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
</table>
 




## -remarks



<b>PeerCollabRefreshEndpointData</b> allows an application to refresh data associated with the endpoint. Upon completion of the API, the PEER_EVENT_REQUEST_STATUS_CHANGED event will be raised. The event will contain a success or failure code. 

On success, the application can call functions like <a href="https://msdn.microsoft.com/596191a1-94cf-4497-aaf0-951e2c63b145">PeerCollabGetPresenceInfo</a>, <a href="https://msdn.microsoft.com/550cbd9d-5569-485e-897d-73d8bab8430a">PeerCollabEnumApplications</a>, <a href="https://msdn.microsoft.com/a9ac2603-b007-4d1c-ac11-c72aeb06e663">PeerCollabEnumObjects</a>, and <a href="https://msdn.microsoft.com/278c7622-988e-441d-a6b9-f62947f881e8">PeerCollabQueryContactData</a> to obtain additional data.
When the data is no longer needed it can be deleted by calling <a href="https://msdn.microsoft.com/bafaef04-d7f6-4873-bd38-db156817b0c8">PeerCollabDeleteEndpointData</a>. 

If a peer is subscribed to the endpoint, the subscribed data takes higher precedence than the data that was  cached by calling PeerCollabRefreshEndpointData
 and will return <b>PEER_EVENT_REQUEST_STATUS_CHANGED</b>.

The <b>PeerCollabRefreshEndpointData</b> API takes a snapshot of the data for the specified endpoint. If endpoint data changes  after this snapshot is taken, the caller will have a stale copy of the data. If PeerCollabRefreshEndpointData is called by an application multiple times for the same endpoint, the latest data received replaces the data stored from an earlier call to the API. However, in order to ensure that the caller is notified of any changes and always has the latest copy, <a href="https://msdn.microsoft.com/dfe17235-34dd-4694-9ee5-4268b4406731">PeerCollabSubscribeEndpointData</a> is recommended instead of <b>PeerCollabRefreshEndpointData</b>.

The <b>PeerCollabRefreshEndpointData</b> function will timeout at 30 seconds.




## -see-also




<a href="https://msdn.microsoft.com/9687b332-14ed-4023-b8c2-437d75fd0298">PEER_ENDPOINT</a>



<a href="https://msdn.microsoft.com/00c3c1f1-c36c-469a-a644-0ec60f02d25e">Peer Collaboration API Functions</a>



<a href="https://msdn.microsoft.com/550cbd9d-5569-485e-897d-73d8bab8430a">PeerCollabEnumApplications</a>



<a href="https://msdn.microsoft.com/a9ac2603-b007-4d1c-ac11-c72aeb06e663">PeerCollabEnumObjects</a>



<a href="https://msdn.microsoft.com/596191a1-94cf-4497-aaf0-951e2c63b145">PeerCollabGetPresenceInfo</a>
 

 

