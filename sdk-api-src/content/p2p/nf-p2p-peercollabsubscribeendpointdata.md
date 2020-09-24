---
UID: NF:p2p.PeerCollabSubscribeEndpointData
title: PeerCollabSubscribeEndpointData function (p2p.h)
description: Creates a subscription to an available endpoint.
helpviewer_keywords: ["PeerCollabSubscribeEndpointData","PeerCollabSubscribeEndpointData function [Peer Networking]","p2p.peercollabsubscribeendpointdata","p2p/PeerCollabSubscribeEndpointData"]
old-location: p2p\peercollabsubscribeendpointdata.htm
tech.root: p2p
ms.assetid: dfe17235-34dd-4694-9ee5-4268b4406731
ms.date: 12/05/2018
ms.keywords: PeerCollabSubscribeEndpointData, PeerCollabSubscribeEndpointData function [Peer Networking], p2p.peercollabsubscribeendpointdata, p2p/PeerCollabSubscribeEndpointData
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
req.lib: P2P.lib
req.dll: P2P.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PeerCollabSubscribeEndpointData
 - p2p/PeerCollabSubscribeEndpointData
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - P2P.dll
api_name:
 - PeerCollabSubscribeEndpointData
---

# PeerCollabSubscribeEndpointData function


## -description

The <b>PeerCollabSubscribeEndpointData</b> function creates  a subscription to an available endpoint.

## -parameters

### -param pcEndpoint [in]

Pointer to a <a href="/windows/desktop/api/p2p/ns-p2p-peer_endpoint">PEER_ENDPOINT</a> structure that contains the peer endpoint used to obtain presence information.

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

When an application exits without calling <a href="/windows/desktop/api/p2p/nf-p2p-peercollabunsubscribeendpointdata">PeerCollabUnsubscribeEndpointData</a>, all of the references for that application are released automatically.

To successfully call the <a href="/windows/desktop/api/p2p/nf-p2p-peercollabgetpresenceinfo">PeerCollabGetPresenceInfo</a>, <a href="/windows/desktop/api/p2p/nf-p2p-peercollabenumapplications">PeerCollabEnumApplications</a>, <a href="/windows/desktop/api/p2p/nf-p2p-peercollabenumobjects">PeerCollabEnumObjects</a>, and <a href="/windows/desktop/api/p2p/nf-p2p-peercollabquerycontactdata">PeerCollabQueryContactData</a> APIs, an application must first call <b>PeerCollabSubscribeEndpointData</b>.

## -see-also

<a href="/windows/desktop/api/p2p/nf-p2p-peercollabenumapplications">PeerCollabEnumApplications</a>



<a href="/windows/desktop/api/p2p/nf-p2p-peercollabenumobjects">PeerCollabEnumObjects</a>



<a href="/windows/desktop/api/p2p/nf-p2p-peercollabgetpresenceinfo">PeerCollabGetPresenceInfo</a>



<a href="/windows/desktop/api/p2p/nf-p2p-peercollabquerycontactdata">PeerCollabQueryContactData</a>



<a href="/windows/desktop/api/p2p/nf-p2p-peercollabunsubscribeendpointdata">PeerCollabUnsubscribeEndpointData</a>