---
UID: NF:p2p.PeerCollabCloseHandle
title: PeerCollabCloseHandle function (p2p.h)
description: Closes the handle to a Peer Collaboration activity invitation.
helpviewer_keywords: ["PeerCollabCloseHandle","PeerCollabCloseHandle function [Peer Networking]","p2p.peercollabclosehandle","p2p/PeerCollabCloseHandle"]
old-location: p2p\peercollabclosehandle.htm
tech.root: p2p
ms.assetid: fbcf65c7-a133-44b9-b5bb-309b1c257a90
ms.date: 12/05/2018
ms.keywords: PeerCollabCloseHandle, PeerCollabCloseHandle function [Peer Networking], p2p.peercollabclosehandle, p2p/PeerCollabCloseHandle
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
 - PeerCollabCloseHandle
 - p2p/PeerCollabCloseHandle
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
 - PeerCollabCloseHandle
---

# PeerCollabCloseHandle function


## -description

The <b>PeerCollabCloseHandle</b> function closes the handle to a Peer Collaboration activity invitation.

## -parameters

### -param hInvitation [in]

Handle obtained by a previous call to <a href="/windows/desktop/api/p2p/nf-p2p-peercollabasyncinvitecontact">PeerCollabAsyncInviteContact</a> or <a href="/windows/desktop/api/p2p/nf-p2p-peercollabasyncinviteendpoint">PeerCollabAsyncInviteEndpoint</a>.

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
<dt><b>E_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The handle specified is invalid.

</td>
</tr>
</table>

## -remarks

You must call this API after the handle has been signaled for an event and any data associated with the event has been obtained.

## -see-also

<a href="/windows/desktop/P2PSdk/collaboration-api-functions">Peer Collaboration API Functions</a>



<a href="/windows/desktop/api/p2p/nf-p2p-peercollabasyncinvitecontact">PeerCollabAsyncInviteContact</a>



<a href="/windows/desktop/api/p2p/nf-p2p-peercollabasyncinviteendpoint">PeerCollabAsyncInviteEndpoint</a>