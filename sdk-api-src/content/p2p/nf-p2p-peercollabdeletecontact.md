---
UID: NF:p2p.PeerCollabDeleteContact
title: PeerCollabDeleteContact function (p2p.h)
description: Deletes a contact from the local contact store associated with the caller.
helpviewer_keywords: ["PeerCollabDeleteContact","PeerCollabDeleteContact function [Peer Networking]","p2p.peercollabdeletecontact","p2p/PeerCollabDeleteContact"]
old-location: p2p\peercollabdeletecontact.htm
tech.root: p2p
ms.assetid: b901ec82-69d2-4a1c-b316-37f209af2b19
ms.date: 12/05/2018
ms.keywords: PeerCollabDeleteContact, PeerCollabDeleteContact function [Peer Networking], p2p.peercollabdeletecontact, p2p/PeerCollabDeleteContact
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
 - PeerCollabDeleteContact
 - p2p/PeerCollabDeleteContact
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
 - PeerCollabDeleteContact
---

# PeerCollabDeleteContact function


## -description

The <b>PeerCollabDeleteContact</b> function deletes a contact from the local contact store associated with the caller.

## -parameters

### -param pwzPeerName [in]

Pointer to a zero-terminated Unicode string that contains the peer name of the contact to delete. This parameter must not be <b>NULL</b>. You cannot delete the 'Me' contact.

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

Once a contact is deleted using <b>PeerCollabDeleteContact</b>, the presence updates  provided by a subscription will no longer be available for that contact. If the contact is being watched (<i>fWatch</i> is set to <b>TRUE</b>) than PEER_EVENT_WATCHLIST_CHANGED will be raised.

## -see-also

<a href="/windows/desktop/P2PSdk/collaboration-api-functions">Peer Collaboration API Functions</a>