---
UID: NF:p2p.PeerCollabAsyncInviteContact
title: PeerCollabAsyncInviteContact function (p2p.h)
description: Sends an invitation to a trusted peer contact to join the sender's peer collaboration activity over a secured connection. The availability of the invitation response is updated through an asynchronous event.
helpviewer_keywords: ["PeerCollabAsyncInviteContact","PeerCollabAsyncInviteContact function [Peer Networking]","p2p.peercollabasyncinvitecontact","p2p/PeerCollabAsyncInviteContact"]
old-location: p2p\peercollabasyncinvitecontact.htm
tech.root: p2p
ms.assetid: 2101e16e-ee05-417f-835b-c00cba7f6576
ms.date: 12/05/2018
ms.keywords: PeerCollabAsyncInviteContact, PeerCollabAsyncInviteContact function [Peer Networking], p2p.peercollabasyncinvitecontact, p2p/PeerCollabAsyncInviteContact
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
 - PeerCollabAsyncInviteContact
 - p2p/PeerCollabAsyncInviteContact
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
 - PeerCollabAsyncInviteContact
---

# PeerCollabAsyncInviteContact function


## -description

The <b>PeerCollabAsyncInviteContact</b> function sends an invitation to a trusted peer contact to join the sender's peer collaboration activity over a secured connection. The availability of the invitation response is updated through an asynchronous event.

## -parameters

### -param pcContact [in, optional]

Pointer to a <a href="/windows/desktop/api/p2p/ns-p2p-peer_contact">PEER_CONTACT</a> structure that contains the contact information associated with the recipient of the invite. This parameter is optional.

To invite the endpoint of the calling peer specified in <i>pcEndpoint</i>, set the pointer value to <b>NULL</b>.

### -param pcEndpoint [in]

Pointer to a <a href="/windows/desktop/api/p2p/ns-p2p-peer_endpoint">PEER_ENDPOINT</a> structure that contains information about the invited peer's endpoint. The endpoint must be associated with the peer contact specified in <i>pcContact</i>.

### -param pcInvitation [in]

Pointer to a <a href="/windows/desktop/api/p2p/ns-p2p-peer_invitation">PEER_INVITATION</a> structure that contains the invitation request to send to the endpoint  specified in <i>pcEndpoint</i>. E_INVALIDARG is returned if this parameter is set to <b>NULL</b>.

### -param hEvent [in, optional]

Handle to the event for this invitation, created by a previous call to CreateEvent. The event is signaled when the status of the asynchronous invitation is updated. To obtain the response data, call <a href="/windows/desktop/api/p2p/nf-p2p-peercollabgetinvitationresponse">PeerCollabGetInvitationResponse</a>.

If the event is not provided the caller must poll for the result by calling <a href="/windows/desktop/api/p2p/nf-p2p-peercollabgetinvitationresponse">PeerCollabGetInvitationResponse</a>.

### -param phInvitation [optional]

A pointer to a handle to the sent invitation. The framework will cleanup the response information after the invitation response is received if <b>NULL</b> is specified. When <b>NULL</b> is not the specified handle to the invitation provided, it must be closed by calling <a href="/windows/desktop/api/p2p/nf-p2p-peercollabclosehandle">PeerCollabCloseHandle</a>.

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
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
<i>pcEndpoint</i> is <b>NULL</b>.

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

This API ensures the peer that receives the invitation is the contact specified as input. The connection will fail if the specific contact is not present on the endpoint specified.  The use of <b>PeerCollabAsyncInviteContact</b> is recommended  in place of the less secure <a href="/windows/desktop/api/p2p/nf-p2p-peercollabasyncinviteendpoint">PeerCollabAsyncInviteEndpoint</a>.

A toast will appear for the recipient of the invitation. This toast will be converted to a dialog box in which the user can accept or decline the invitation. When the invitation is successfully accepted, the collaborative application is launched on the recipient's machine.


To successfully receive the invitation the application must be registered on the recipient's machine using <a href="/windows/desktop/api/p2p/nf-p2p-peercollabregisterapplication">PeerCollabRegisterApplication</a>. It is also possible for the sender of the invite to have  failure codes returned because the recipient has turned off application invites.


The <a href="/windows/desktop/api/p2p/nf-p2p-peercollabgetinvitationresponse">PeerCollabGetInvitiationResponse</a> function will return PEER_E_CONNECTION_FAILED if the contact to which the invitation is being sent is not accepting invitations.

If the recipient is accepting invitations only from trusted contacts, then the sender of the invite must be added to the contact store of the recipient machine. The sender must be added to the contact store before the invitation attempt. To add a contact to the contact store, call <a href="/windows/desktop/api/p2p/nf-p2p-peercollabaddcontact">PeerCollabAddContact</a>. 


To cancel an outstanding invitation, call <a href="/windows/desktop/api/p2p/nf-p2p-peercollabcancelinvitation">PeerCollabCancelInvitation</a>.

## -see-also

<a href="/windows/desktop/api/p2p/ns-p2p-peer_contact">PEER_CONTACT</a>



<a href="/windows/desktop/api/p2p/ns-p2p-peer_endpoint">PEER_ENDPOINT</a>



<a href="/windows/desktop/api/p2p/ns-p2p-peer_invitation">PEER_INVITATION</a>



<a href="/windows/desktop/P2PSdk/collaboration-api-functions">Peer Collaboration API Functions</a>



<a href="/windows/desktop/api/p2p/nf-p2p-peercollabaddcontact">PeerCollabAddContact</a>



<a href="/windows/desktop/api/p2p/nf-p2p-peercollabcancelinvitation">PeerCollabCancelInvitation</a>



<a href="/windows/desktop/api/p2p/nf-p2p-peercollabclosehandle">PeerCollabCloseHandle</a>



<a href="/windows/desktop/api/p2p/nf-p2p-peercollabgetapplaunchinfo">PeerCollabGetAppLaunchInfo</a>



<a href="/windows/desktop/api/p2p/nf-p2p-peercollabgetinvitationresponse">PeerCollabGetInvitationResponse</a>