---
UID: NF:p2p.PeerCollabAddContact
title: PeerCollabAddContact function (p2p.h)
description: Adds a contact to the contact list of a peer.
helpviewer_keywords: ["PeerCollabAddContact","PeerCollabAddContact function [Peer Networking]","p2p.peercollabaddcontact","p2p/PeerCollabAddContact"]
old-location: p2p\peercollabaddcontact.htm
tech.root: p2p
ms.assetid: 0e4ba039-2016-487d-b4df-e96648db1a05
ms.date: 12/05/2018
ms.keywords: PeerCollabAddContact, PeerCollabAddContact function [Peer Networking], p2p.peercollabaddcontact, p2p/PeerCollabAddContact
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
 - PeerCollabAddContact
 - p2p/PeerCollabAddContact
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
 - PeerCollabAddContact
---

# PeerCollabAddContact function


## -description

The <b>PeerCollabAddContact</b> function adds a contact to the contact list of a peer.

## -parameters

### -param pwzContactData [in]

Pointer to a zero-terminated Unicode string buffer that contains the contact data for the peer that is added to the contact list. This string buffer can either be obtained by passing the peer name of the endpoint to add as a contact to <a href="/windows/desktop/api/p2p/nf-p2p-peercollabquerycontactdata">PeerCollabQueryContactData</a>, or through an out-of-band mechanism. 

To  send its own contact data out-of-band, the peer can call <a href="/windows/desktop/api/p2p/nf-p2p-peercollabexportcontact">PeerCollabExportContact</a> with a <b>NULL</b> peer name. This function returns the contact data in XML format.

### -param ppContact [out, optional]

Pointer to a pointer to a <a href="/windows/desktop/api/p2p/ns-p2p-peer_contact">PEER_CONTACT</a> structure. This parameter receives the address of a <b>PEER_CONTACT</b> structure containing peer contact information for the contact supplied in <i>pwzContactData</i>. This parameter may be <b>NULL</b>. 

Call <a href="/windows/desktop/api/p2p/nf-p2p-peerfreedata">PeerFreeData</a> on the address of the <a href="/windows/desktop/api/p2p/ns-p2p-peer_contact">PEER_CONTACT</a> structure to free this data.

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

## -see-also

<a href="/windows/desktop/api/p2p/ns-p2p-peer_contact">PEER_CONTACT</a>



<a href="/windows/desktop/P2PSdk/collaboration-api-functions">Peer Collaboration API Functions</a>



<a href="/windows/desktop/api/p2p/nf-p2p-peercollabexportcontact">PeerCollabExportContact</a>



<a href="/windows/desktop/api/p2p/nf-p2p-peercollabquerycontactdata">PeerCollabQueryContactData</a>