---
UID: NF:p2p.PeerCollabSetPresenceInfo
title: PeerCollabSetPresenceInfo function (p2p.h)
description: Updates the caller's presence information to any contacts watching it.
helpviewer_keywords: ["PeerCollabSetPresenceInfo","PeerCollabSetPresenceInfo function [Peer Networking]","p2p.peercollabsetpresenceinfo","p2p/PeerCollabSetPresenceInfo"]
old-location: p2p\peercollabsetpresenceinfo.htm
tech.root: p2p
ms.assetid: fd90e7d2-5126-4bcf-b633-466855abd60a
ms.date: 12/05/2018
ms.keywords: PeerCollabSetPresenceInfo, PeerCollabSetPresenceInfo function [Peer Networking], p2p.peercollabsetpresenceinfo, p2p/PeerCollabSetPresenceInfo
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
 - PeerCollabSetPresenceInfo
 - p2p/PeerCollabSetPresenceInfo
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
 - PeerCollabSetPresenceInfo
---

# PeerCollabSetPresenceInfo function


## -description

The <b>PeerCollabSetPresenceInfo</b> function updates the caller's presence information to any contacts watching it.

## -parameters

### -param pcPresenceInfo [in]

Pointer to a <a href="/windows/desktop/api/p2p/ns-p2p-peer_presence_info">PEER_PRESENCE_INFO</a> structure that contains the new presence information to publish for the calling peer application.

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
<dt><b>PEER_E_NOT_INITIALIZED</b></dt>
</dl>
</td>
<td width="60%">
 The Windows Peer infrastructure is not initialized. Calling the relevant initialization function  is required.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PEER_E_NOT_SIGNED_IN</b></dt>
</dl>
</td>
<td width="60%">
The operation requires the user to be signed in.

</td>
</tr>
</table>

## -remarks

Contacts watching this peer's presence will have a PEER_EVENT_PRESENCE_CHANGED event raised locally that signals this peer's change in presence status. A peer's presence status cannot be set to offline while signed-in. By default,   a peer's presence status is 'online' and the descriptive text is <b>NULL</b> when signing in. 

Any  descriptive text for presence status is limited to 255 Unicode characters.

## -see-also

<a href="/windows/desktop/P2PSdk/collaboration-api-functions">Peer Collaboration API Functions</a>