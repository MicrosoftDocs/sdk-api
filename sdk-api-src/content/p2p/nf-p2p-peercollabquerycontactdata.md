---
UID: NF:p2p.PeerCollabQueryContactData
title: PeerCollabQueryContactData function (p2p.h)
description: Retrieves the contact information for the supplied peer endpoint.
helpviewer_keywords: ["PeerCollabQueryContactData","PeerCollabQueryContactData function [Peer Networking]","p2p.peercollabquerycontactdata","p2p/PeerCollabQueryContactData"]
old-location: p2p\peercollabquerycontactdata.htm
tech.root: p2p
ms.assetid: 278c7622-988e-441d-a6b9-f62947f881e8
ms.date: 12/05/2018
ms.keywords: PeerCollabQueryContactData, PeerCollabQueryContactData function [Peer Networking], p2p.peercollabquerycontactdata, p2p/PeerCollabQueryContactData
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
 - PeerCollabQueryContactData
 - p2p/PeerCollabQueryContactData
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
 - PeerCollabQueryContactData
---

# PeerCollabQueryContactData function


## -description

The <b>PeerCollabQueryContactData</b> function retrieves the contact information for the supplied peer endpoint.

## -parameters

### -param pcEndpoint [in, optional]

Pointer to a <a href="/windows/desktop/api/p2p/ns-p2p-peer_endpoint">PEER_ENDPOINT</a> structure that contains the peer endpoint about which to obtain contact information. 

If this parameter is set to <b>NULL</b>, the contact information for the current peer endpoint is obtained.

### -param ppwzContactData [out]

Pointer to a zero-terminated Unicode string buffer that contains the contact data for the endpoint supplied in <i>pcEndpoint</i>. Call <a href="/windows/desktop/api/p2p/nf-p2p-peerfreedata">PeerFreeData</a> to free the data.

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
The requested contact data does not exist. Try calling  <a href="/windows/desktop/api/p2p/nf-p2p-peercollabrefreshendpointdata">PeerCollabRefreshEndpointData</a> before making another attempt.

</td>
</tr>
</table>

## -remarks

To retrieve contact data for an endpoint  successfully, one of the following must occur:<ul>
<li>The endpoint must have been previously obtained by calling <a href="/windows/desktop/api/p2p/nf-p2p-peercollabenumendpoints">PeerCollabEnumEndpoints</a>.
</li>
<li>The local peer must have subscribed to the endpoint by calling <a href="/windows/desktop/api/p2p/nf-p2p-peercollabsubscribeendpointdata">PeerCollabSubscribeEndpointData</a>.</li>
<li>The endpoint data must be refreshed by calling <a href="/windows/desktop/api/p2p/nf-p2p-peercollabrefreshendpointdata">PeerCollabRefreshEndpointData</a> successfully.</li>
</ul>

## -see-also

<a href="/windows/desktop/api/p2p/ns-p2p-peer_endpoint">PEER_ENDPOINT</a>



<a href="/windows/desktop/P2PSdk/collaboration-api-functions">Peer Collaboration API Functions</a>