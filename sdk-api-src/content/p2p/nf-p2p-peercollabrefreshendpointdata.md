---
UID: NF:p2p.PeerCollabRefreshEndpointData
title: PeerCollabRefreshEndpointData function (p2p.h)
description: Updates the calling peer node with new endpoint data.
helpviewer_keywords: ["PeerCollabRefreshEndpointData","PeerCollabRefreshEndpointData function [Peer Networking]","p2p.peercollabrefreshendpointdata","p2p/PeerCollabRefreshEndpointData"]
old-location: p2p\peercollabrefreshendpointdata.htm
tech.root: p2p
ms.assetid: ba841da4-de7f-4288-84b7-a06370b55e3c
ms.date: 12/05/2018
ms.keywords: PeerCollabRefreshEndpointData, PeerCollabRefreshEndpointData function [Peer Networking], p2p.peercollabrefreshendpointdata, p2p/PeerCollabRefreshEndpointData
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
 - PeerCollabRefreshEndpointData
 - p2p/PeerCollabRefreshEndpointData
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
 - PeerCollabRefreshEndpointData
---

# PeerCollabRefreshEndpointData function


## -description

The <b>PeerCollabRefreshEndpointData</b> function updates the calling peer node with new endpoint data.

## -parameters

### -param pcEndpoint [in]

Pointer to a <a href="/windows/desktop/api/p2p/ns-p2p-peer_endpoint">PEER_ENDPOINT</a> structure that contains the updated peer endpoint information for the current peer node.

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

On success, the application can call functions like <a href="/windows/desktop/api/p2p/nf-p2p-peercollabgetpresenceinfo">PeerCollabGetPresenceInfo</a>, <a href="/windows/desktop/api/p2p/nf-p2p-peercollabenumapplications">PeerCollabEnumApplications</a>, <a href="/windows/desktop/api/p2p/nf-p2p-peercollabenumobjects">PeerCollabEnumObjects</a>, and <a href="/windows/desktop/api/p2p/nf-p2p-peercollabquerycontactdata">PeerCollabQueryContactData</a> to obtain additional data.
When the data is no longer needed it can be deleted by calling <a href="/windows/desktop/api/p2p/nf-p2p-peercollabdeleteendpointdata">PeerCollabDeleteEndpointData</a>. 

If a peer is subscribed to the endpoint, the subscribed data takes higher precedence than the data that was  cached by calling PeerCollabRefreshEndpointDataand will return <b>PEER_EVENT_REQUEST_STATUS_CHANGED</b>.

The <b>PeerCollabRefreshEndpointData</b> API takes a snapshot of the data for the specified endpoint. If endpoint data changes  after this snapshot is taken, the caller will have a stale copy of the data. If PeerCollabRefreshEndpointData is called by an application multiple times for the same endpoint, the latest data received replaces the data stored from an earlier call to the API. However, in order to ensure that the caller is notified of any changes and always has the latest copy, <a href="/windows/desktop/api/p2p/nf-p2p-peercollabsubscribeendpointdata">PeerCollabSubscribeEndpointData</a> is recommended instead of <b>PeerCollabRefreshEndpointData</b>.

The <b>PeerCollabRefreshEndpointData</b> function will timeout at 30 seconds.

## -see-also

<a href="/windows/desktop/api/p2p/ns-p2p-peer_endpoint">PEER_ENDPOINT</a>



<a href="/windows/desktop/P2PSdk/collaboration-api-functions">Peer Collaboration API Functions</a>



<a href="/windows/desktop/api/p2p/nf-p2p-peercollabenumapplications">PeerCollabEnumApplications</a>



<a href="/windows/desktop/api/p2p/nf-p2p-peercollabenumobjects">PeerCollabEnumObjects</a>



<a href="/windows/desktop/api/p2p/nf-p2p-peercollabgetpresenceinfo">PeerCollabGetPresenceInfo</a>