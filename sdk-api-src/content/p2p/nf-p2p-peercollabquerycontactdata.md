---
UID: NF:p2p.PeerCollabQueryContactData
title: PeerCollabQueryContactData function
author: windows-driver-content
description: Retrieves the contact information for the supplied peer endpoint.
old-location: p2p\peercollabquerycontactdata.htm
old-project: P2PSdk
ms.assetid: 278c7622-988e-441d-a6b9-f62947f881e8
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: PeerCollabQueryContactData, PeerCollabQueryContactData function [Peer Networking], p2p.peercollabquerycontactdata, p2p/PeerCollabQueryContactData
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
-	PeerCollabQueryContactData
product: Windows
targetos: Windows
req.lib: P2P.lib
req.dll: P2P.dll
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# PeerCollabQueryContactData function


## -description


The <b>PeerCollabQueryContactData</b> function retrieves the contact information for the supplied peer endpoint.


## -parameters




### -param pcEndpoint [in, optional]

Pointer to a <a href="https://msdn.microsoft.com/9687b332-14ed-4023-b8c2-437d75fd0298">PEER_ENDPOINT</a> structure that contains the peer endpoint about which to obtain contact information. 

If this parameter is set to <b>NULL</b>, the contact information for the current peer endpoint is obtained.


### -param ppwzContactData [out]

Pointer to a zero-terminated Unicode string buffer that contains the contact data for the endpoint supplied in <i>pcEndpoint</i>. Call <a href="https://msdn.microsoft.com/54288829-c991-42d6-a7c4-874ed28dd106">PeerFreeData</a> to free the data.


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
<dt><b>PEER_E_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The requested contact data does not exist. Try calling  <a href="https://msdn.microsoft.com/ba841da4-de7f-4288-84b7-a06370b55e3c">PeerCollabRefreshEndpointData</a> before making another attempt.

</td>
</tr>
</table>
 




## -remarks



To retrieve contact data for an endpoint  successfully, one of the following must occur:<ul>
<li>The endpoint must have been previously obtained by calling <a href="https://msdn.microsoft.com/c29d089c-1f1e-4d50-9a3a-18c844b4ad1c">PeerCollabEnumEndpoints</a>.
</li>
<li>The local peer must have subscribed to the endpoint by calling <a href="https://msdn.microsoft.com/dfe17235-34dd-4694-9ee5-4268b4406731">PeerCollabSubscribeEndpointData</a>.</li>
<li>The endpoint data must be refreshed by calling <a href="https://msdn.microsoft.com/ba841da4-de7f-4288-84b7-a06370b55e3c">PeerCollabRefreshEndpointData</a> successfully.</li>
</ul>





## -see-also




<a href="https://msdn.microsoft.com/9687b332-14ed-4023-b8c2-437d75fd0298">PEER_ENDPOINT</a>



<a href="https://msdn.microsoft.com/00c3c1f1-c36c-469a-a644-0ec60f02d25e">Peer Collaboration API Functions</a>
 

 

