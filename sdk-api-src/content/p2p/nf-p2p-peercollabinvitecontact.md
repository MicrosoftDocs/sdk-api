---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# PeerCollabInviteContact function


## -description


The <b>PeerCollabInviteContact</b> function sends an invitation to join a peer collaboration activity to a trusted contact. This call is synchronous and, if successful, obtains a response from the contact.


## -parameters




### -param pcContact [in]

Pointer to a <a href="https://msdn.microsoft.com/b84a17fc-35d6-4098-9bb3-18e708541a80">PEER_CONTACT</a> structure that contains the contact information associated with the invitee.


### -param pcEndpoint [in]

Pointer to a <a href="https://msdn.microsoft.com/9687b332-14ed-4023-b8c2-437d75fd0298">PEER_ENDPOINT</a> structure that contains information about the invited peer. This peer is sent an invitation when this API is called.


### -param pcInvitation [in]

Pointer to a <a href="https://msdn.microsoft.com/b74b45c0-760f-4008-87dd-9fdea0d4be05">PEER_INVITATION</a> structure that contains the invitation request to send to the endpoint(s)  specified in <i>pcEndpoint</i>. This parameter must not be set to <b>NULL</b>.


### -param ppResponse [out]

Pointer to a <a href="https://msdn.microsoft.com/9f77c471-ef05-442f-aeae-afe67319b0ff">PEER_INVITATION_RESPONSE</a> structure that receives an invited peer endpoint's responses to the invitation request.

If this call fails with an error, this parameter will be <b>NULL</b>.

Free the memory returned by calling <a href="https://msdn.microsoft.com/54288829-c991-42d6-a7c4-874ed28dd106">PeerFreeData</a>.


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



This API ensures the peer that receives the invitation is the contact specified as input. The connection will fail if the specific contact is not present on the endpoint specified.  The use of <b>PeerCollabInviteContact</b> is recommended  in place of the less secure <a href="https://msdn.microsoft.com/c77eee5b-6fee-4eaa-ac0e-94a0fd3df92e">PeerCollabInviteEndpoint</a>.

A toast will appear for the recipient of the invitation. This toast will be converted to a dialog box in which the user can accept or decline the invitation. When the invitation is successfully accepted, the collaborative application is launched on the recipient's machine.


To successfully receive the invitation, the application must be registered on the recipient's machine using <a href="https://msdn.microsoft.com/962982a6-171f-4c13-ae03-84698482dea4">PeerCollabRegisterApplication</a>. It is also possible for the sender of the invite to have  failure codes returned because the recipient has turned off application invites.


If the recipient is accepting invitations only from trusted contacts, then the sender of the invite must be added to the contact store of the recipient machine. The sender must be added to the contact store before the invitation attempt. To add a contact to the contact store, call <a href="https://msdn.microsoft.com/0e4ba039-2016-487d-b4df-e96648db1a05">PeerCollabAddContact</a>. 


The recipient of the invitation must respond within 5 minutes to avoid timeout.




## -see-also




<a href="https://msdn.microsoft.com/b84a17fc-35d6-4098-9bb3-18e708541a80">PEER_CONTACT</a>



<a href="https://msdn.microsoft.com/9687b332-14ed-4023-b8c2-437d75fd0298">PEER_ENDPOINT</a>



<a href="https://msdn.microsoft.com/b74b45c0-760f-4008-87dd-9fdea0d4be05">PEER_INVITATION</a>



<a href="https://msdn.microsoft.com/9f77c471-ef05-442f-aeae-afe67319b0ff">PEER_INVITATION_RESPONSE</a>



<a href="https://msdn.microsoft.com/266a7d80-b4bc-42f2-ba76-a69cab9e2c12">PeerCollabGetAppLaunchInfo</a>
 

 

