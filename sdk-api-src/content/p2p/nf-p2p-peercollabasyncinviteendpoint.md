---
UID: NF:p2p.PeerCollabAsyncInviteEndpoint
title: PeerCollabAsyncInviteEndpoint function
author: windows-sdk-content
description: Sends an invitation to a specified peer endpoint to join the sender's peer collaboration activity. The availability of the response to the invitation is updated through an asynchronous event.
old-location: p2p\peercollabasyncinviteendpoint.htm
tech.root: p2psdk
ms.assetid: 2606d2ef-26d3-4c52-b481-3ea38350295a
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: PeerCollabAsyncInviteEndpoint, PeerCollabAsyncInviteEndpoint function [Peer Networking], p2p.peercollabasyncinviteendpoint, p2p/PeerCollabAsyncInviteEndpoint
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
 - PeerCollabAsyncInviteEndpoint
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PeerCollabAsyncInviteEndpoint function


## -description


The <b>PeerCollabAsyncInviteEndpoint</b> function sends an invitation to a specified peer endpoint to join the sender's peer collaboration activity. The availability of the response to the invitation is updated through an asynchronous event.


## -parameters




### -param pcEndpoint [in]

Pointer to a <a href="https://msdn.microsoft.com/9687b332-14ed-4023-b8c2-437d75fd0298">PEER_ENDPOINT</a> structure that contains information about the invited peer. This peer is sent an invitation when this API is called.

This parameter must not be set to <b>NULL</b>.


### -param pcInvitation [in]

Pointer to a <a href="https://msdn.microsoft.com/b74b45c0-760f-4008-87dd-9fdea0d4be05">PEER_INVITATION</a> structure that contains the invitation request to send to the endpoint  specified in <i>pcEndpoint</i>. E_INVALIDARG is returned if this parameter is set to <b>NULL</b>.


### -param hEvent [in, optional]

Handle to the event for this invitation, created by a previous call to CreateEvent. The event is signaled when the status of the asynchronous invitation is updated. To obtain the response data, call <a href="https://msdn.microsoft.com/f9471e51-5eec-4927-bd12-7d362f5101ee">PeerCollabGetInvitationResponse</a>.

If the event is not provided, the caller must poll for the result by calling <a href="https://msdn.microsoft.com/f9471e51-5eec-4927-bd12-7d362f5101ee">PeerCollabGetInvitationResponse</a>.


### -param phInvitation [out, optional]

A pointer to a handle to the sent invitation. If this parameter is <b>NULL</b>, the framework will cleanup the response information after the invitation response is received. If this parameter is not <b>NULL</b>, the handle must be closed by calling <a href="https://msdn.microsoft.com/fbcf65c7-a133-44b9-b5bb-309b1c257a90">PeerCollabCloseHandle</a>.


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



This API sends an invitation to the endpoint specified as input. It does not guarantee that the recipient of the invite is the specific contact that the user  intended to send the invite to. To ensure that the invitation is sent to the correct contact use <a href="https://msdn.microsoft.com/2101e16e-ee05-417f-835b-c00cba7f6576">PeerCollabAsyncInviteContact</a>.

A toast will appear for the recipient of the invitation. This toast will be converted to a dialog box in which the user can accept or decline the invitation. When the invitation is successfully accepted, the collaborative application is launched on the recipient's machine.


To successfully receive the invitation, the application must be registered on the recipient's machine using <a href="p2p.peercollabregisterapplication">PeerCollabRegisterApplication</a>. It is also possible for the sender of the invite to have  failure codes returned because the recipient has turned off application invites.


The <a href="https://msdn.microsoft.com/f9471e51-5eec-4927-bd12-7d362f5101ee">PeerCollabGetInvitiationResponse</a> function will return PEER_E_CONNECTION_FAILED if the endpoint to which the invitation is being sent is not accepting invitations.



If the recipient is accepting invitations only from trusted contacts, then the sender of the invite must be added to the contact store of the recipient machine. The sender must be added to the contact store before the invitation attempt. To add a contact to the contact store, call <a href="https://msdn.microsoft.com/0e4ba039-2016-487d-b4df-e96648db1a05">PeerCollabAddContact</a>. 





## -see-also




<a href="https://msdn.microsoft.com/9687b332-14ed-4023-b8c2-437d75fd0298">PEER_ENDPOINT</a>



<a href="https://msdn.microsoft.com/b74b45c0-760f-4008-87dd-9fdea0d4be05">PEER_INVITATION</a>



<a href="https://msdn.microsoft.com/00c3c1f1-c36c-469a-a644-0ec60f02d25e">Peer Collaboration API Functions</a>



<a href="https://msdn.microsoft.com/fbcf65c7-a133-44b9-b5bb-309b1c257a90">PeerCollabCloseHandle</a>



<a href="https://msdn.microsoft.com/266a7d80-b4bc-42f2-ba76-a69cab9e2c12">PeerCollabGetAppLaunchInfo</a>



<a href="https://msdn.microsoft.com/f9471e51-5eec-4927-bd12-7d362f5101ee">PeerCollabGetInvitationResponse</a>
 

 

