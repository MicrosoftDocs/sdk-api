---
UID: NF:p2p.PeerCollabSetObject
title: PeerCollabSetObject function (p2p.h)
description: Creates or updates a peer data object used in a peer collaboration network.
helpviewer_keywords: ["PeerCollabSetObject","PeerCollabSetObject function [Peer Networking]","p2p.peercollabsetobject","p2p/PeerCollabSetObject"]
old-location: p2p\peercollabsetobject.htm
tech.root: p2p
ms.assetid: 99a3e206-7d76-4773-956c-bbd101766392
ms.date: 12/05/2018
ms.keywords: PeerCollabSetObject, PeerCollabSetObject function [Peer Networking], p2p.peercollabsetobject, p2p/PeerCollabSetObject
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
 - PeerCollabSetObject
 - p2p/PeerCollabSetObject
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
 - PeerCollabSetObject
---

# PeerCollabSetObject function


## -description

The <b>PeerCollabSetObject</b> function creates or updates a peer data object used in a peer collaboration network.

## -parameters

### -param pcObject [in]

Pointer to a <a href="/windows/desktop/api/p2p/ns-p2p-peer_object">PEER_OBJECT</a> structure that contains the peer object on the peer collaboration network.

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

Peer objects are run-time data items associated with a particular application, such as a picture, an avatar, a certificate, or a specific description. Each peer object must be smaller than 16K in size and cannot be 0.

If an object is already published, <b>PeerCollabSetObject</b> will update the existing   object data.
The last application that updates the object will take ownership of the object. As a result, if  the application is terminated the object is deleted.

If an object's 'published' status is removed due to sign-out rather than the closure of the associated application, the application is responsible for publishing the object the next time the user signs on.


Trusted contacts watching this peer object will have a <b>PEER_EVENT_OBJECT_CHANGED</b> event raised locally, signaling this peer object's change in status.

<b>PeerCollabSetObject</b> can be used to publish at most 128 objects.

There is one object with a given <i>GUID</i> published at any given time.

## -see-also

<a href="/windows/desktop/api/p2p/ns-p2p-peer_object">PEER_OBJECT</a>



<a href="/windows/desktop/P2PSdk/collaboration-api-functions">Peer Collaboration API Functions</a>