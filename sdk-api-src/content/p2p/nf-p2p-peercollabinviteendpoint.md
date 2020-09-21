---
UID: NF:p2p.PeerCollabInviteEndpoint
title: PeerCollabInviteEndpoint function (p2p.h)
description: Sends an invitation to a specified peer endpoint to join the sender's peer collaboration activity. This call is synchronous and, if successful, obtains a response from the peer endpoint.
helpviewer_keywords: ["PeerCollabInviteEndpoint","PeerCollabInviteEndpoint function [Peer Networking]","p2p.peercollabinviteendpoint","p2p/PeerCollabInviteEndpoint"]
old-location: p2p\peercollabinviteendpoint.htm
tech.root: p2p
ms.assetid: c77eee5b-6fee-4eaa-ac0e-94a0fd3df92e
ms.date: 12/05/2018
ms.keywords: PeerCollabInviteEndpoint, PeerCollabInviteEndpoint function [Peer Networking], p2p.peercollabinviteendpoint, p2p/PeerCollabInviteEndpoint
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
 - PeerCollabInviteEndpoint
 - p2p/PeerCollabInviteEndpoint
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
 - PeerCollabInviteEndpoint
---

# PeerCollabInviteEndpoint function


## -description

The <b>PeerCollabInviteEndpoint</b> function sends an invitation to a specified peer endpoint to join the sender's peer collaboration activity. This call is synchronous and, if successful, obtains a response from the peer endpoint.

## -parameters

### -param pcEndpoint [in]

Pointer to a <a href="/windows/desktop/api/p2p/ns-p2p-peer_endpoint">PEER_ENDPOINT</a> structure that contains information about the invited peer. This peer is sent an invitation when this API is called.

This parameter must not be set to <b>NULL</b>.

### -param pcInvitation [in]

Pointer to a <a href="/windows/desktop/api/p2p/ns-p2p-peer_invitation">PEER_INVITATION</a> structure that contains the invitation request to send to the endpoint  specified in <i>pcEndpoint</i>. This parameter must not be set to <b>NULL</b>.

### -param ppResponse [out]

Pointer to a   <a href="/windows/desktop/api/p2p/ns-p2p-peer_invitation_response">PEER_INVITATION_RESPONSE</a> structure that receives an invited peer endpoint's responses to the invitation request.

If this call fails with an error, on output this parameter will be <b>NULL</b>.

Free the memory associated with this structure by pass it to <a href="/windows/desktop/api/p2p/nf-p2p-peerfreedata">PeerFreeData</a>.

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

This API sends an invitation to the endpoint specified as input. It does not guarantee that the recipient of the invite is the specific contact that the user  intended to send the invite to. To ensure that the invitation is sent to the correct contact, call <a href="/windows/desktop/api/p2p/nf-p2p-peercollabinvitecontact">PeerCollabInviteContact</a>.

A toast will appear for the recipient of the invitation. This toast will be converted to a dialog box in which the user can accept or decline the invitation. When the invitation is successfully accepted, the collaborative application is launched on the recipient's machine.


To successfully receive the invitation, the application must be registered on the recipient's machine using <a href="/windows/desktop/api/p2p/nf-p2p-peercollabregisterapplication">PeerCollabRegisterApplication</a>. It is also possible for the sender of the invite to have  failure codes returned because the recipient has turned off application invites.


The recipient of the invitation must respond within 5 minutes to avoid timeout.

## -see-also

<a href="/windows/desktop/api/p2p/ns-p2p-peer_endpoint">PEER_ENDPOINT</a>



<a href="/windows/desktop/api/p2p/ns-p2p-peer_invitation">PEER_INVITATION</a>



<a href="/windows/desktop/api/p2p/ns-p2p-peer_invitation_response">PEER_INVITATION_RESPONSE</a>



<a href="/windows/desktop/P2PSdk/collaboration-api-functions">Peer Collaboration API Functions</a>



<a href="/windows/desktop/api/p2p/nf-p2p-peercollabgetapplaunchinfo">PeerCollabGetAppLaunchInfo</a>