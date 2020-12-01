---
UID: NF:p2p.PeerCollabEnumContacts
title: PeerCollabEnumContacts function (p2p.h)
description: Returns a handle to an enumerated set that contains all of the peer collaboration network contacts currently available on the calling peer.
helpviewer_keywords: ["PeerCollabEnumContacts","PeerCollabEnumContacts function [Peer Networking]","p2p.peercollabenumcontacts","p2p/PeerCollabEnumContacts"]
old-location: p2p\peercollabenumcontacts.htm
tech.root: p2p
ms.assetid: e5a259e5-c5cb-4a7e-8f60-29e4d7cc6ede
ms.date: 12/05/2018
ms.keywords: PeerCollabEnumContacts, PeerCollabEnumContacts function [Peer Networking], p2p.peercollabenumcontacts, p2p/PeerCollabEnumContacts
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
 - PeerCollabEnumContacts
 - p2p/PeerCollabEnumContacts
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
 - PeerCollabEnumContacts
---

# PeerCollabEnumContacts function


## -description

The <b>PeerCollabEnumContacts</b> function returns a handle to an enumerated set that contains all of the peer collaboration network contacts currently available on the calling peer.

## -parameters

### -param phPeerEnum [out]

Handle to an enumerated set that contains all of the peer collaboration network contacts currently available on the calling peer, excluding the "Me" contact.

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

To obtain the individual peer contacts, pass the returned handle to [PEER_CONTACT](./ns-p2p-peer_contact.md) structures will be returned. To close the enumeration and release the resources associated with it, pass this handle to <a href="/windows/desktop/api/p2p/nf-p2p-peerendenumeration">PeerEndEnumeration</a>. Individual items returned by the enumeration must be released with <a href="/windows/desktop/api/p2p/nf-p2p-peerfreedata">PeerFreeData</a>.

## -see-also

<a href="/windows/desktop/P2PSdk/collaboration-api-functions">Peer Collaboration API Functions</a>