---
UID: NF:p2p.PeerCollabEnumObjects
title: PeerCollabEnumObjects function (p2p.h)
description: Returns the handle to an enumeration that contains the peer objects associated with a specific peer's endpoint.
helpviewer_keywords: ["PeerCollabEnumObjects","PeerCollabEnumObjects function [Peer Networking]","p2p.peercollabenumobjects","p2p/PeerCollabEnumObjects"]
old-location: p2p\peercollabenumobjects.htm
tech.root: p2p
ms.assetid: a9ac2603-b007-4d1c-ac11-c72aeb06e663
ms.date: 12/05/2018
ms.keywords: PeerCollabEnumObjects, PeerCollabEnumObjects function [Peer Networking], p2p.peercollabenumobjects, p2p/PeerCollabEnumObjects
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
 - PeerCollabEnumObjects
 - p2p/PeerCollabEnumObjects
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
 - PeerCollabEnumObjects
---

# PeerCollabEnumObjects function


## -description

The <b>PeerCollabEnumObjects</b> function returns the handle to an enumeration that contains the peer objects associated with a specific peer's endpoint.

## -parameters

### -param pcEndpoint [in]

Pointer to a <a href="/windows/desktop/api/p2p/ns-p2p-peer_endpoint">PEER_ENDPOINT</a> structure that contains the endpoint information for a peer whose objects will be enumerated. 

If this parameter is <b>NULL</b> the published objects of the  local peer's contacts are returned.

### -param pObjectId [in, optional]

Pointer to a GUID value that uniquely identifies a peer object with the supplied peer. If this parameter is supplied, the only peer object returned is the one that matches this GUID.

### -param phPeerEnum [out]

Pointer to the handle for the enumerated set of peer objects that correspond to the GUID returned in <i>pObjectId</i>. Pass this handle to <a href="/windows/desktop/api/p2p/nf-p2p-peergetnextitem">PeerGetNextItem</a> to obtain each item in the enumerated set.

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
<tr>
<td width="40%">
<dl>
<dt><b>PEER_E_NOT_SIGNED_IN</b></dt>
</dl>
</td>
<td width="60%">
The operation requires the user to be signed in.

</td>
</tr>
</table>

## -remarks

Peer objects are run-time data items associated with a particular application, such as a picture, an avatar, a certificate, or a specific description. Each peer object must be smaller than 16K in size.

<b>PeerCollabEnumObjects</b> will return all of the objects published for the local peer. The objects can be published by more than one application.

To obtain the individual peer objects, pass the returned handle to <a href="/windows/desktop/api/p2p/nf-p2p-peergetnextitem">PeerGetNextItem</a>. The peer objects are returned as an array of pointers to the <a href="/windows/desktop/api/p2p/ns-p2p-peer_object">PEER_OBJECT</a> structures. If the endpoint is not publishing any objects, an empty array will be returned. To close the enumeration and release the resources associated with it, pass this handle to <a href="/windows/desktop/api/p2p/nf-p2p-peerendenumeration">PeerEndEnumeration</a>. Individual items returned by the enumeration must be released with <a href="/windows/desktop/api/p2p/nf-p2p-peerfreedata">PeerFreeData</a>.

To obtain a peer object successfully:<ul>
<li>The endpoint must have been previously obtained by calling <a href="/windows/desktop/api/p2p/nf-p2p-peercollabenumendpoints">PeerCollabEnumEndpoints</a>.
</li>
<li>The local peer must have subscribed to the endpoint by calling <a href="/windows/desktop/api/p2p/nf-p2p-peercollabsubscribeendpointdata">PeerCollabSubscribeEndpointData</a>.</li>
<li>The endpoint data must be refreshed by calling <a href="/windows/desktop/api/p2p/nf-p2p-peercollabrefreshendpointdata">PeerCollabRefreshEndpointData</a> successfully.</li>
</ul>


If the user is publishing a picture, the picture can be obtained by retrieving the corresponding object. The GUID for the picture object is PEER_COLLAB_OBJECTID_USER_PICTURE.

## -see-also

[PEER_CONTACT](./ns-p2p-peer_contact.md)



<a href="/windows/desktop/api/p2p/ns-p2p-peer_endpoint">PEER_ENDPOINT</a>



<a href="/windows/desktop/api/p2p/ns-p2p-peer_object">PEER_OBJECT</a>



<a href="/windows/desktop/P2PSdk/collaboration-api-functions">Peer Collaboration API Functions</a>