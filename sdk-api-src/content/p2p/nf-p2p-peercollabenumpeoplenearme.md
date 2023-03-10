---
UID: NF:p2p.PeerCollabEnumPeopleNearMe
title: PeerCollabEnumPeopleNearMe function (p2p.h)
description: Returns a handle to an enumerated set that contains all of the peer collaboration network &quot;people near me&quot; endpoints currently available on the subnet of the calling peer.
helpviewer_keywords: ["PeerCollabEnumPeopleNearMe","PeerCollabEnumPeopleNearMe function [Peer Networking]","p2p.peercollabenumpeoplenearme","p2p/PeerCollabEnumPeopleNearMe"]
old-location: p2p\peercollabenumpeoplenearme.htm
tech.root: p2p
ms.assetid: 4dc53f43-e662-4696-bc16-42b124f3358f
ms.date: 12/05/2018
ms.keywords: PeerCollabEnumPeopleNearMe, PeerCollabEnumPeopleNearMe function [Peer Networking], p2p.peercollabenumpeoplenearme, p2p/PeerCollabEnumPeopleNearMe
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
 - PeerCollabEnumPeopleNearMe
 - p2p/PeerCollabEnumPeopleNearMe
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
 - PeerCollabEnumPeopleNearMe
---

# PeerCollabEnumPeopleNearMe function


## -description

The <b>PeerCollabEnumPeopleNearMe</b> function returns a handle to an enumerated set that contains all of the peer collaboration network "people near me" endpoints currently available on the subnet of the calling peer.

## -parameters

### -param phPeerEnum [out]

Pointer to a handle of an enumerated set that contains all of the peer collaboration network "people near me" endpoints currently available on the subnet of the calling peer.

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

To obtain the individual peer "people near me" contacts, pass the returned handle to <a href="/windows/desktop/api/p2p/nf-p2p-peergetnextitem">PeerGetNextItem</a>. An array of pointers to the <a href="/windows/desktop/api/p2p/ns-p2p-peer_people_near_me">PEER_PEOPLE_NEAR_ME</a> structures are returned. To close the enumeration and release the resources associated with it, pass this handle to <a href="/windows/desktop/api/p2p/nf-p2p-peerendenumeration">PeerEndEnumeration</a>. Individual items returned by the enumeration must be released with <a href="/windows/desktop/api/p2p/nf-p2p-peerfreedata">PeerFreeData</a>.

## -see-also

<a href="/windows/desktop/api/p2p/ns-p2p-peer_people_near_me">PEER_PEOPLE_NEAR_ME</a>



<a href="/windows/desktop/P2PSdk/collaboration-api-functions">Peer Collaboration API Functions</a>



<a href="/windows/desktop/api/p2p/nf-p2p-peercollabsignin">PeerCollabSignin</a>