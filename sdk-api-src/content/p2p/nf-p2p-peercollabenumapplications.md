---
UID: NF:p2p.PeerCollabEnumApplications
title: PeerCollabEnumApplications function (p2p.h)
description: Returns the handle to an enumeration that contains the applications registered to a specific peer's endpoint(s).
helpviewer_keywords: ["PeerCollabEnumApplications","PeerCollabEnumApplications function [Peer Networking]","p2p.peercollabenumapplications","p2p/PeerCollabEnumApplications"]
old-location: p2p\peercollabenumapplications.htm
tech.root: p2p
ms.assetid: 550cbd9d-5569-485e-897d-73d8bab8430a
ms.date: 12/05/2018
ms.keywords: PeerCollabEnumApplications, PeerCollabEnumApplications function [Peer Networking], p2p.peercollabenumapplications, p2p/PeerCollabEnumApplications
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
 - PeerCollabEnumApplications
 - p2p/PeerCollabEnumApplications
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
 - PeerCollabEnumApplications
---

# PeerCollabEnumApplications function


## -description

The <b>PeerCollabEnumApplications</b> function returns the handle to an enumeration that contains the applications registered to a specific peer's endpoint(s).

## -parameters

### -param pcEndpoint [in, optional]

Pointer to a <a href="/windows/desktop/api/p2p/ns-p2p-peer_endpoint">PEER_ENDPOINT</a> structure that contains the endpoint information for a peer whose applications will be enumerated. 

If this parameter is set to <b>NULL</b>, the published application information for the local peer's endpoint is enumerated.

### -param pApplicationId [in, optional]

Pointer to the GUID value that uniquely identifies a particular application of the supplied peer. If this parameter is supplied, the only peer application returned is the one that matches this GUID.

### -param phPeerEnum [out]

Pointer to the handle for the enumerated set of registered applications that correspond to the GUID returned in <i>pObjectId</i>. Pass this handle to <a href="/windows/desktop/api/p2p/nf-p2p-peergetnextitem">PeerGetNextItem</a> to obtain each item in the enumerated set.

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

In order to enumerate the applications for the specified endpoint  successfully, application data must be available on the endpoint. For application data to be available, one of the following must occur:<ul>
<li>The endpoint must have been previously obtained by calling <a href="/windows/desktop/api/p2p/nf-p2p-peercollabenumendpoints">PeerCollabEnumEndpoints</a>.
</li>
<li>The local peer must have subscribed to the endpoint by calling <a href="/windows/desktop/api/p2p/nf-p2p-peercollabsubscribeendpointdata">PeerCollabSubscribeEndpointData</a>.</li>
<li>The endpoint data must be refreshed by calling <a href="/windows/desktop/api/p2p/nf-p2p-peercollabrefreshendpointdata">PeerCollabRefreshEndpointData</a> successfully.</li>
</ul>


To obtain the individual peer applications, pass the returned handle to <a href="/windows/desktop/api/p2p/nf-p2p-peergetnextitem">PeerGetNextItem</a>. To close the enumeration and release the resources associated with it, pass this handle to <a href="/windows/desktop/api/p2p/nf-p2p-peerendenumeration">PeerEndEnumeration</a>. Individual items returned by the enumeration must be released with <a href="/windows/desktop/api/p2p/nf-p2p-peerfreedata">PeerFreeData</a>.

Peer application data items are returned as individual <a href="/windows/desktop/api/p2p/ns-p2p-peer_application">PEER_APPLICATION</a> structures.

The <b>PeerCollabEnumApplications</b> function returns an empty array for endpoints on the subnet that are not trusted contacts.

## -see-also

<a href="/windows/desktop/api/p2p/ns-p2p-peer_application">PEER_APPLICATION</a>



<a href="/windows/desktop/api/p2p/ns-p2p-peer_contact">PEER_CONTACT</a>



<a href="/windows/desktop/api/p2p/ns-p2p-peer_endpoint">PEER_ENDPOINT</a>



<a href="/windows/desktop/P2PSdk/collaboration-api-functions">Peer Collaboration API Functions</a>