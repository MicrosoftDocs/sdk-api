---
UID: NF:p2p.PeerCollabGetApplicationRegistrationInfo
title: PeerCollabGetApplicationRegistrationInfo function (p2p.h)
description: Obtains application-specific registration information.
helpviewer_keywords: ["PeerCollabGetApplicationRegistrationInfo","PeerCollabGetApplicationRegistrationInfo function [Peer Networking]","p2p.peercollabgetapplicationregistrationinfo","p2p/PeerCollabGetApplicationRegistrationInfo"]
old-location: p2p\peercollabgetapplicationregistrationinfo.htm
tech.root: p2p
ms.assetid: d1a8888e-4153-4486-9384-615ae7ed7031
ms.date: 12/05/2018
ms.keywords: PeerCollabGetApplicationRegistrationInfo, PeerCollabGetApplicationRegistrationInfo function [Peer Networking], p2p.peercollabgetapplicationregistrationinfo, p2p/PeerCollabGetApplicationRegistrationInfo
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
 - PeerCollabGetApplicationRegistrationInfo
 - p2p/PeerCollabGetApplicationRegistrationInfo
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
 - PeerCollabGetApplicationRegistrationInfo
---

# PeerCollabGetApplicationRegistrationInfo function


## -description

The <b>PeerCollabGetApplicationRegistrationInfo</b> function obtains application-specific registration information.

## -parameters

### -param pApplicationId [in]

Pointer to the GUID value that represents a particular peer's application registration flags.

### -param registrationType [in]

A <a href="/windows/desktop/api/p2p/ne-p2p-peer_application_registration_type">PEER_APPLICATION_REGISTRATION_TYPE</a> enumeration value that describes whether the peer's application is registered to the current user or all users of the local machine.

### -param ppApplication [out]

Pointer to the address of a <a href="/windows/desktop/api/p2p/ns-p2p-peer_application_registration_info">PEER_APPLICATION_REGISTRATION_INFO</a> structure that contains the information about a peer's specific registered application. The data returned in this parameter can be freed by calling <a href="/windows/desktop/api/p2p/nf-p2p-peerfreedata">PeerFreeData</a>.

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
The requested application is not registered for the given <i>registrationType</i>.

</td>
</tr>
</table>

## -remarks

An <i>application</i> is a set of software or software  features available on the peer's endpoint. Commonly, this refers to software packages that support peer networking activities, like games or other collaborative applications.

A peer's application has a GUID representing a single application. When an application is registered for a peer, this GUID and the corresponding application can be made available to all trusted contacts of the peer, indicating the activities the peer can participate in. To unregister a peer's application, call <a href="/windows/desktop/api/p2p/nf-p2p-peercollabunregisterapplication">PeerCollabUnregisterApplication</a> with this GUID.

## -see-also

<a href="/windows/desktop/api/p2p/ns-p2p-peer_application_registration_info">PEER_APPLICATION_REGISTRATION_INFO</a>



<a href="/windows/desktop/api/p2p/ne-p2p-peer_application_registration_type">PEER_APPLICATION_REGISTRATION_TYPE</a>



<a href="/windows/desktop/P2PSdk/collaboration-api-functions">Peer Collaboration API Functions</a>



<a href="/windows/desktop/api/p2p/nf-p2p-peercollabregisterapplication">PeerCollabRegisterApplication</a>



<a href="/windows/desktop/api/p2p/nf-p2p-peercollabunregisterapplication">PeerCollabUnregisterApplication</a>