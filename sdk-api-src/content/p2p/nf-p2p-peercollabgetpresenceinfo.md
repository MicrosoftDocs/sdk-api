---
UID: NF:p2p.PeerCollabGetPresenceInfo
title: PeerCollabGetPresenceInfo function (p2p.h)
description: Retrieves the presence information for the endpoint associated with a specific contact.
helpviewer_keywords: ["PeerCollabGetPresenceInfo","PeerCollabGetPresenceInfo function [Peer Networking]","p2p.peercollabgetpresenceinfo","p2p/PeerCollabGetPresenceInfo"]
old-location: p2p\peercollabgetpresenceinfo.htm
tech.root: p2p
ms.assetid: 596191a1-94cf-4497-aaf0-951e2c63b145
ms.date: 12/05/2018
ms.keywords: PeerCollabGetPresenceInfo, PeerCollabGetPresenceInfo function [Peer Networking], p2p.peercollabgetpresenceinfo, p2p/PeerCollabGetPresenceInfo
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
 - PeerCollabGetPresenceInfo
 - p2p/PeerCollabGetPresenceInfo
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
 - PeerCollabGetPresenceInfo
---

# PeerCollabGetPresenceInfo function


## -description

The <b>PeerCollabGetPresenceInfo</b> function retrieves the  presence information for the endpoint associated with a specific contact.

## -parameters

### -param pcEndpoint [in]

Pointer to a <a href="/windows/desktop/api/p2p/ns-p2p-peer_endpoint">PEER_ENDPOINT</a> structure that contains the specific endpoint associated with the contact specified in <i>pcContact</i> for which presence information must be returned.

### -param ppPresenceInfo [out]

Pointer  to the address of the <a href="/windows/desktop/api/p2p/ns-p2p-peer_presence_info">PEER_PRESENCE_INFO</a> structure that contains the requested presence data for the supplied endpoint.

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
The application did not make a previous call to <a href="/windows/desktop/api/p2p/nf-p2p-peercollabstartup">PeerCollabStartup</a>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PEER_E_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The presence information for the specified endpoint was not found in the peer collaboration network.

</td>
</tr>
</table>

## -remarks

To obtain a peer object successfully:<ul>
<li>The endpoint must have been previously obtained by calling <a href="/windows/desktop/api/p2p/nf-p2p-peercollabenumendpoints">PeerCollabEnumEndpoints</a>.
</li>
<li>The local peer must have subscribed to the endpoint by calling <a href="/windows/desktop/api/p2p/nf-p2p-peercollabsubscribeendpointdata">PeerCollabSubscribeEndpointData</a>.</li>
<li>The endpoint data must be refreshed by calling <a href="/windows/desktop/api/p2p/nf-p2p-peercollabrefreshendpointdata">PeerCollabRefreshEndpointData</a> successfully.</li>
</ul>

## -see-also

<a href="/windows/desktop/api/p2p/ns-p2p-peer_contact">PEER_CONTACT</a>



<a href="/windows/desktop/api/p2p/ns-p2p-peer_endpoint">PEER_ENDPOINT</a>



<a href="/windows/desktop/api/p2p/ns-p2p-peer_presence_info">PEER_PRESENCE_INFO</a>



<a href="/windows/desktop/P2PSdk/collaboration-api-functions">Peer Collaboration API Functions</a>