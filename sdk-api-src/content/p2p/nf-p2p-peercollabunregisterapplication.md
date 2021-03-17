---
UID: NF:p2p.PeerCollabUnregisterApplication
title: PeerCollabUnregisterApplication function (p2p.h)
description: Unregisters the specific applications of a peer from the local computer.
helpviewer_keywords: ["PeerCollabUnregisterApplication","PeerCollabUnregisterApplication function [Peer Networking]","p2p.peercollabunregisterapplication","p2p/PeerCollabUnregisterApplication"]
old-location: p2p\peercollabunregisterapplication.htm
tech.root: p2p
ms.assetid: 2479b726-20f1-4370-9fcf-f29cec44c3ec
ms.date: 12/05/2018
ms.keywords: PeerCollabUnregisterApplication, PeerCollabUnregisterApplication function [Peer Networking], p2p.peercollabunregisterapplication, p2p/PeerCollabUnregisterApplication
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
 - PeerCollabUnregisterApplication
 - p2p/PeerCollabUnregisterApplication
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
 - PeerCollabUnregisterApplication
---

# PeerCollabUnregisterApplication function


## -description

The <b>PeerCollabUnregisterApplication</b> function unregisters the specific applications of a peer from the local computer.

## -parameters

### -param pApplicationId [in]

Pointer to the GUID value that represents a particular peer's application.

### -param registrationType [in]

A <a href="/windows/desktop/api/p2p/ne-p2p-peer_application_registration_type">PEER_APPLICATION_REGISTRATION_TYPE</a> value that describes whether the peer's application is deregistered for the current user or all users of the peer's machine.

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
<dt><b>PEER_E_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The application  requested to unregister was not registered for the given <i>registrationType.</i>

</td>
</tr>
</table>

## -remarks

An <i>application</i> is a set of software or software  features available on the peer's endpoint. Commonly, this refers to software packages that support peer networking activities, like games or other collaborative applications.

The collaboration infrastructure can receive application invites from trusted contacts or from "People Near Me", which are based on what scope the collaboration infrastructure is signed in with using PeerCollabSignin.

A peer's application has a GUID representing a single specific application. When application is registered for a peer, this GUID and the corresponding application can be made available to all trusted contacts of the peer, indicating the activities the peer can participate in. To unregister a peer's application, call <b>PeerCollabUnregisterApplication</b> with this GUID.

To unregister the application for all users, the caller of this API must be elevated.

## -see-also

<a href="/windows/desktop/api/p2p/ne-p2p-peer_application_registration_type">PEER_APPLICATION_REGISTRATION_TYPE</a>



<a href="/windows/desktop/P2PSdk/collaboration-api-functions">Peer Collaboration API Functions</a>



<a href="/windows/desktop/api/p2p/nf-p2p-peercollabregisterapplication">PeerCollabRegisterApplication</a>