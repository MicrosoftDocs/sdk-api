---
UID: NF:p2p.PeerCollabEnumEndpoints
title: PeerCollabEnumEndpoints function (p2p.h)
description: Returns the handle to an enumeration that contains the endpoints associated with a specific peer contact.
helpviewer_keywords: ["PeerCollabEnumEndpoints","PeerCollabEnumEndpoints function [Peer Networking]","p2p.peercollabenumendpoints","p2p/PeerCollabEnumEndpoints"]
old-location: p2p\peercollabenumendpoints.htm
tech.root: p2p
ms.assetid: c29d089c-1f1e-4d50-9a3a-18c844b4ad1c
ms.date: 12/05/2018
ms.keywords: PeerCollabEnumEndpoints, PeerCollabEnumEndpoints function [Peer Networking], p2p.peercollabenumendpoints, p2p/PeerCollabEnumEndpoints
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
 - PeerCollabEnumEndpoints
 - p2p/PeerCollabEnumEndpoints
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
 - PeerCollabEnumEndpoints
---

# PeerCollabEnumEndpoints function


## -description

The <b>PeerCollabEnumEndpoints</b> function returns the handle to an enumeration that contains the endpoints associated with a specific peer contact.

## -parameters

### -param pcContact [in]

Pointer to a <a href="/windows/desktop/api/p2p/ns-p2p-peer_contact">PEER_CONTACT</a> structure that contains the contact information for a specific peer. This parameter must not be <b>NULL</b>.

### -param phPeerEnum [out]

Pointer to a handle for the enumerated set of endpoints that are associated with the supplied peer contact. Pass this handle to <a href="/windows/desktop/api/p2p/nf-p2p-peergetnextitem">PeerGetNextItem</a> to obtain each item in the enumerated set.

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

It is recommended that a contact record is updated using <a href="/windows/desktop/api/p2p/nf-p2p-peercollabupdatecontact">PeerCollabUpdateContact</a> prior to calling <b>PeerCollabEnumEndpoints</b>. Failure to do so can result in a return of E_INVALIDARG.

Endpoints will be available only for contacts with <i>fWatch</i> set to <b>true</b>.  Only endpoints that have the "Me" contact of the calling peer saved as a trusted contact and have <i>WatcherPermissions</i> set to <b>allow</b> will be available.  A contact must also be signed-in to the internet. In the event the contact is not signed-in, the error <b>E_INVALIDARG</b> will be returned.

To obtain the individual peer endpoints, pass the returned handle to <a href="/windows/desktop/api/p2p/nf-p2p-peergetnextitem">PeerGetNextItem</a>. An array of pointers to <a href="/windows/desktop/api/p2p/ns-p2p-peer_endpoint">PEER_ENDPOINT</a> structures will be returned. If no endpoints are available, an empty array will be returned. To close the enumeration and release the resources associated with it, pass this handle to <a href="/windows/desktop/api/p2p/nf-p2p-peerendenumeration">PeerEndEnumeration</a>. Individual items returned by the enumeration must be released with <a href="/windows/desktop/api/p2p/nf-p2p-peerfreedata">PeerFreeData</a>.

The limit for connections to a single contact is 50.

## -see-also

<a href="/windows/desktop/api/p2p/ns-p2p-peer_endpoint">PEER_ENDPOINT</a>



<a href="/windows/desktop/P2PSdk/collaboration-api-functions">Peer Collaboration API Functions</a>