---
UID: NF:p2p.PeerCollabUpdateContact
title: PeerCollabUpdateContact function (p2p.h)
description: Updates the information associated with a peer contact specified in the local contact store of the caller.
helpviewer_keywords: ["PeerCollabUpdateContact","PeerCollabUpdateContact function [Peer Networking]","p2p.peercollabupdatecontact","p2p/PeerCollabUpdateContact"]
old-location: p2p\peercollabupdatecontact.htm
tech.root: p2p
ms.assetid: 66a72629-6be1-4f1e-aeb1-e9b484c74732
ms.date: 12/05/2018
ms.keywords: PeerCollabUpdateContact, PeerCollabUpdateContact function [Peer Networking], p2p.peercollabupdatecontact, p2p/PeerCollabUpdateContact
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
 - PeerCollabUpdateContact
 - p2p/PeerCollabUpdateContact
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
 - PeerCollabUpdateContact
---

# PeerCollabUpdateContact function


## -description

The <b>PeerCollabUpdateContact</b> function updates the information associated with a peer contact specified in the local contact store of the caller.

## -parameters

### -param pContact [in]

Pointer to a <a href="/windows/desktop/api/p2p/ns-p2p-peer_contact">PEER_CONTACT</a> structure that contains the updated information for a specific peer contact.

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

If the contact provided is the 'Me' contact, only the nickname, display name and email address can be changed. If a nickname is changed for a contact signed in to "People Near Me", the structure  <a href="/windows/desktop/api/p2p/ns-p2p-peer_event_people_near_me_changed_data">PEER_EVENT_PEOPLE_NEAR_ME_CHANGED_DATA</a> with <i>changeType</i> of PEER_CHANGE_UPDATED will be raised.

The <b>PeerCollabUpdateContact</b> function will timeout at 30 seconds.

## -see-also

<a href="/windows/desktop/P2PSdk/collaboration-api-functions">Peer Collaboration API Functions</a>