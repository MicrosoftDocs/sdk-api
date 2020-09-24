---
UID: NF:p2p.PeerCollabInviteContact
title: PeerCollabInviteContact function (p2p.h)
description: Sends an invitation to join a peer collaboration activity to a trusted contact. This call is synchronous and, if successful, obtains a response from the contact.
helpviewer_keywords: ["PeerCollabInviteContact","PeerCollabInviteContact function [Peer Networking]","p2p.peercollabinvitecontact","p2p/PeerCollabInviteContact"]
old-location: p2p\peercollabinvitecontact.htm
tech.root: p2p
ms.assetid: 65c6cdb5-33af-435c-9444-42f8689e13a8
ms.date: 12/05/2018
ms.keywords: PeerCollabInviteContact, PeerCollabInviteContact function [Peer Networking], p2p.peercollabinvitecontact, p2p/PeerCollabInviteContact
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
 - PeerCollabInviteContact
 - p2p/PeerCollabInviteContact
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
 - PeerCollabInviteContact
---

# PeerCollabInviteContact function


## -description

The <b>PeerCollabInviteContact</b> function sends an invitation to join a peer collaboration activity to a trusted contact. This call is synchronous and, if successful, obtains a response from the contact.

## -parameters

### -param pcContact [in]

Pointer to a <a href="/windows/desktop/api/p2p/ns-p2p-peer_contact">PEER_CONTACT</a> structure that contains the contact information associated with the invitee.

### -param pcEndpoint [in]

Pointer to a <a href="/windows/desktop/api/p2p/ns-p2p-peer_endpoint">PEER_ENDPOINT</a> structure that contains information about the invited peer. This peer is sent an invitation when this API is called.

### -param pcInvitation [in]

Pointer to a <a href="/windows/desktop/api/p2p/ns-p2p-peer_invitation">PEER_INVITATION</a> structure that contains the invitation request to send to the endpoint(s)  specified in <i>pcEndpoint</i>. This parameter must not be set to <b>NULL</b>.

### -param ppResponse [out]

Pointer to a <a href="/windows/desktop/api/p2p/ns-p2p-peer_invitation_response">PEER_INVITATION_RESPONSE</a> structure that receives an invited peer endpoint's responses to the invitation request.

If this call fails with an error, this parameter will be <b>NULL</b>.

Free the memory returned by calling <a href="/windows/desktop/api/p2p/nf-p2p-peerfreedata">PeerFreeData</a>.

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
<dt><b>PEER_E_TIMEOUT</b></dt>
</dl>
</td>
<td width="60%">
The recipient of the invitation has not responded within 5 minutes.

</td>
</tr>
</table>

## -remarks

This API ensures the peer that receives the invitation is the contact specified as input. The connection will fail if the specific contact is not present on the endpoint specified.  The use of <b>PeerCollabInviteContact</b> is recommended  in place of the less secure <a href="/windows/desktop/api/p2p/nf-p2p-peercollabinviteendpoint">PeerCollabInviteEndpoint</a>.

A toast will appear for the recipient of the invitation. This toast will be converted to a dialog box in which the user can accept or decline the invitation. When the invitation is successfully accepted, the collaborative application is launched on the recipient's machine.


To successfully receive the invitation, the application must be registered on the recipient's machine using <a href="/windows/desktop/api/p2p/nf-p2p-peercollabregisterapplication">PeerCollabRegisterApplication</a>. It is also possible for the sender of the invite to have  failure codes returned because the recipient has turned off application invites.


If the recipient is accepting invitations only from trusted contacts, then the sender of the invite must be added to the contact store of the recipient machine. The sender must be added to the contact store before the invitation attempt. To add a contact to the contact store, call <a href="/windows/desktop/api/p2p/nf-p2p-peercollabaddcontact">PeerCollabAddContact</a>. 


The recipient of the invitation must respond within 5 minutes to avoid timeout.

## -see-also

<a href="/windows/desktop/api/p2p/ns-p2p-peer_contact">PEER_CONTACT</a>



<a href="/windows/desktop/api/p2p/ns-p2p-peer_endpoint">PEER_ENDPOINT</a>



<a href="/windows/desktop/api/p2p/ns-p2p-peer_invitation">PEER_INVITATION</a>



<a href="/windows/desktop/api/p2p/ns-p2p-peer_invitation_response">PEER_INVITATION_RESPONSE</a>



<a href="/windows/desktop/api/p2p/nf-p2p-peercollabgetapplaunchinfo">PeerCollabGetAppLaunchInfo</a>