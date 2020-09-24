---
UID: NF:p2p.PeerCollabCancelInvitation
title: PeerCollabCancelInvitation function (p2p.h)
description: Cancels an invitation previously sent by the caller to a contact.
helpviewer_keywords: ["PeerCollabCancelInvitation","PeerCollabCancelInvitation function [Peer Networking]","p2p.peercollabcancelinvitation","p2p/PeerCollabCancelInvitation"]
old-location: p2p\peercollabcancelinvitation.htm
tech.root: p2p
ms.assetid: 733c4ece-283b-4d25-8dab-1351f6ca7d12
ms.date: 12/05/2018
ms.keywords: PeerCollabCancelInvitation, PeerCollabCancelInvitation function [Peer Networking], p2p.peercollabcancelinvitation, p2p/PeerCollabCancelInvitation
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
 - PeerCollabCancelInvitation
 - p2p/PeerCollabCancelInvitation
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
 - PeerCollabCancelInvitation
---

# PeerCollabCancelInvitation function


## -description

The <b>PeerCollabCancelInvitation</b> function cancels an invitation previously sent by the caller to a contact.

## -parameters

### -param hInvitation [in]

Handle to a previously sent invitation.

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
The provided handle is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PEER_E_NOT_INITIALIZED</b></dt>
</dl>
</td>
<td width="60%">
The application did not make a previous call to <a href="/windows/desktop/api/p2p/nf-p2p-peercollabstartup">PeerCollabStartup</a>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The handle specified is invalid.

</td>
</tr>
</table>

## -remarks

 When <b>PeerCollabCancelInvitation</b> is called, depending on the state of the invitation, it will perform one or more of the following actions:


<ul>
<li>If the connection to the receiver is not yet established, it will cancel the connection creation process and the receiver will not see the invitation.</li>
<li>If the invitation has been received, but not responded to, it will notify the recipient contact that the invitation has been canceled. As a result, the receiver will not be able to respond to the invitation.</li>
<li>If the receiver has already responded to the invitation, the call performs a no-op.
After canceling the invitation, you must call <a href="/windows/desktop/api/p2p/nf-p2p-peercollabclosehandle">PeerCollabCloseHandle</a>.
</li>
</ul>

## -see-also

<a href="/windows/desktop/P2PSdk/collaboration-api-functions">Peer Collaboration API Functions</a>



<a href="/windows/desktop/api/p2p/nf-p2p-peercollabclosehandle">PeerCollabCloseHandle</a>