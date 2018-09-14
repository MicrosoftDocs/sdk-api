---
UID: NF:p2p.PeerCollabInviteEndpoint
title: PeerCollabInviteEndpoint function
author: windows-sdk-content
description: Sends an invitation to a specified peer endpoint to join the sender's peer collaboration activity. This call is synchronous and, if successful, obtains a response from the peer endpoint.
old-location: p2p\peercollabinviteendpoint.htm
tech.root: p2psdk
ms.assetid: c77eee5b-6fee-4eaa-ac0e-94a0fd3df92e
ms.author: windowssdkdev
ms.date: 08/31/2018
ms.keywords: PeerCollabInviteEndpoint, PeerCollabInviteEndpoint function [Peer Networking], p2p.peercollabinviteendpoint, p2p/PeerCollabInviteEndpoint
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - P2P.dll
api_name:
 - PeerCollabInviteEndpoint
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PeerCollabInviteEndpoint function


## -description


The <b>PeerCollabInviteEndpoint</b> function sends an invitation to a specified peer endpoint to join the sender's peer collaboration activity. This call is synchronous and, if successful, obtains a response from the peer endpoint.


## -parameters




### -param pcEndpoint [in]

Pointer to a <a href="https://msdn.microsoft.com/9687b332-14ed-4023-b8c2-437d75fd0298">PEER_ENDPOINT</a> structure that contains information about the invited peer. This peer is sent an invitation when this API is called.

This parameter must not be set to <b>NULL</b>.


### -param pcInvitation [in]

Pointer to a <a href="https://msdn.microsoft.com/b74b45c0-760f-4008-87dd-9fdea0d4be05">PEER_INVITATION</a> structure that contains the invitation request to send to the endpoint  specified in <i>pcEndpoint</i>. This parameter must not be set to <b>NULL</b>.


### -param ppResponse [out]

Pointer to a   <a href="https://msdn.microsoft.com/9f77c471-ef05-442f-aeae-afe67319b0ff">PEER_INVITATION_RESPONSE</a> structure that receives an invited peer endpoint's responses to the invitation request.

If this call fails with an error, on output this parameter will be <b>NULL</b>.

Free the memory associated with this structure by pass it to <a href="https://msdn.microsoft.com/54288829-c991-42d6-a7c4-874ed28dd106">PeerFreeData</a>.


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



This API sends an invitation to the endpoint specified as input. It does not guarantee that the recipient of the invite is the specific contact that the user  intended to send the invite to. To ensure that the invitation is sent to the correct contact, call <a href="https://msdn.microsoft.com/65c6cdb5-33af-435c-9444-42f8689e13a8">PeerCollabInviteContact</a>.

A toast will appear for the recipient of the invitation. This toast will be converted to a dialog box in which the user can accept or decline the invitation. When the invitation is successfully accepted, the collaborative application is launched on the recipient's machine.


To successfully receive the invitation, the application must be registered on the recipient's machine using <a href="p2p.peercollabregisterapplication">PeerCollabRegisterApplication</a>. It is also possible for the sender of the invite to have  failure codes returned because the recipient has turned off application invites.


The recipient of the invitation must respond within 5 minutes to avoid timeout.




## -see-also




<a href="https://msdn.microsoft.com/9687b332-14ed-4023-b8c2-437d75fd0298">PEER_ENDPOINT</a>



<a href="https://msdn.microsoft.com/b74b45c0-760f-4008-87dd-9fdea0d4be05">PEER_INVITATION</a>



<a href="https://msdn.microsoft.com/9f77c471-ef05-442f-aeae-afe67319b0ff">PEER_INVITATION_RESPONSE</a>



<a href="https://msdn.microsoft.com/00c3c1f1-c36c-469a-a644-0ec60f02d25e">Peer Collaboration API Functions</a>



<a href="https://msdn.microsoft.com/266a7d80-b4bc-42f2-ba76-a69cab9e2c12">PeerCollabGetAppLaunchInfo</a>
 

 

