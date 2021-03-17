---
UID: NF:p2p.PeerCollabAsyncInviteEndpoint
title: PeerCollabAsyncInviteEndpoint function (p2p.h)
description: Sends an invitation to a specified peer endpoint to join the sender's peer collaboration activity. The availability of the response to the invitation is updated through an asynchronous event.
helpviewer_keywords: ["PeerCollabAsyncInviteEndpoint","PeerCollabAsyncInviteEndpoint function [Peer Networking]","p2p.peercollabasyncinviteendpoint","p2p/PeerCollabAsyncInviteEndpoint"]
old-location: p2p\peercollabasyncinviteendpoint.htm
tech.root: p2p
ms.assetid: 2606d2ef-26d3-4c52-b481-3ea38350295a
ms.date: 12/05/2018
ms.keywords: PeerCollabAsyncInviteEndpoint, PeerCollabAsyncInviteEndpoint function [Peer Networking], p2p.peercollabasyncinviteendpoint, p2p/PeerCollabAsyncInviteEndpoint
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
 - PeerCollabAsyncInviteEndpoint
 - p2p/PeerCollabAsyncInviteEndpoint
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
 - PeerCollabAsyncInviteEndpoint
---

# PeerCollabAsyncInviteEndpoint function


## -description

The <b>PeerCollabAsyncInviteEndpoint</b> function sends an invitation to a specified peer endpoint to join the sender's peer collaboration activity. The availability of the response to the invitation is updated through an asynchronous event.

## -parameters

### -param pcEndpoint [in]

Pointer to a <a href="/windows/desktop/api/p2p/ns-p2p-peer_endpoint">PEER_ENDPOINT</a> structure that contains information about the invited peer. This peer is sent an invitation when this API is called.

This parameter must not be set to <b>NULL</b>.

### -param pcInvitation [in]

Pointer to a <a href="/windows/desktop/api/p2p/ns-p2p-peer_invitation">PEER_INVITATION</a> structure that contains the invitation request to send to the endpoint  specified in <i>pcEndpoint</i>. E_INVALIDARG is returned if this parameter is set to <b>NULL</b>.

### -param hEvent [in, optional]

Handle to the event for this invitation, created by a previous call to CreateEvent. The event is signaled when the status of the asynchronous invitation is updated. To obtain the response data, call <a href="/windows/desktop/api/p2p/nf-p2p-peercollabgetinvitationresponse">PeerCollabGetInvitationResponse</a>.

If the event is not provided, the caller must poll for the result by calling <a href="/windows/desktop/api/p2p/nf-p2p-peercollabgetinvitationresponse">PeerCollabGetInvitationResponse</a>.

### -param phInvitation [out, optional]

A pointer to a handle to the sent invitation. If this parameter is <b>NULL</b>, the framework will cleanup the response information after the invitation response is received. If this parameter is not <b>NULL</b>, the handle must be closed by calling <a href="/windows/desktop/api/p2p/nf-p2p-peercollabclosehandle">PeerCollabCloseHandle</a>.

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

This API sends an invitation to the endpoint specified as input. It does not guarantee that the recipient of the invite is the specific contact that the user  intended to send the invite to. To ensure that the invitation is sent to the correct contact use <a href="/windows/desktop/api/p2p/nf-p2p-peercollabasyncinvitecontact">PeerCollabAsyncInviteContact</a>.

A toast will appear for the recipient of the invitation. This toast will be converted to a dialog box in which the user can accept or decline the invitation. When the invitation is successfully accepted, the collaborative application is launched on the recipient's machine.


To successfully receive the invitation, the application must be registered on the recipient's machine using <a href="/windows/desktop/api/p2p/nf-p2p-peercollabregisterapplication">PeerCollabRegisterApplication</a>. It is also possible for the sender of the invite to have  failure codes returned because the recipient has turned off application invites.


The <a href="/windows/desktop/api/p2p/nf-p2p-peercollabgetinvitationresponse">PeerCollabGetInvitiationResponse</a> function will return PEER_E_CONNECTION_FAILED if the endpoint to which the invitation is being sent is not accepting invitations.



If the recipient is accepting invitations only from trusted contacts, then the sender of the invite must be added to the contact store of the recipient machine. The sender must be added to the contact store before the invitation attempt. To add a contact to the contact store, call <a href="/windows/desktop/api/p2p/nf-p2p-peercollabaddcontact">PeerCollabAddContact</a>.

## -see-also

<a href="/windows/desktop/api/p2p/ns-p2p-peer_endpoint">PEER_ENDPOINT</a>



<a href="/windows/desktop/api/p2p/ns-p2p-peer_invitation">PEER_INVITATION</a>



<a href="/windows/desktop/P2PSdk/collaboration-api-functions">Peer Collaboration API Functions</a>



<a href="/windows/desktop/api/p2p/nf-p2p-peercollabclosehandle">PeerCollabCloseHandle</a>



<a href="/windows/desktop/api/p2p/nf-p2p-peercollabgetapplaunchinfo">PeerCollabGetAppLaunchInfo</a>



<a href="/windows/desktop/api/p2p/nf-p2p-peercollabgetinvitationresponse">PeerCollabGetInvitationResponse</a>