---
UID: NF:p2p.PeerCollabRegisterApplication
title: PeerCollabRegisterApplication function (p2p.h)
description: Registers an application with the local computer so that it can be launched in a peer collaboration activity.
helpviewer_keywords: ["PeerCollabRegisterApplication","PeerCollabRegisterApplication function [Peer Networking]","p2p.peercollabregisterapplication","p2p/PeerCollabRegisterApplication"]
old-location: p2p\peercollabregisterapplication.htm
tech.root: p2p
ms.assetid: 962982a6-171f-4c13-ae03-84698482dea4
ms.date: 12/05/2018
ms.keywords: PeerCollabRegisterApplication, PeerCollabRegisterApplication function [Peer Networking], p2p.peercollabregisterapplication, p2p/PeerCollabRegisterApplication
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
 - PeerCollabRegisterApplication
 - p2p/PeerCollabRegisterApplication
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
 - PeerCollabRegisterApplication
---

# PeerCollabRegisterApplication function


## -description

The <b>PeerCollabRegisterApplication</b> function registers an application with the local computer so that it can be launched in a peer collaboration activity.

## -parameters

### -param pcApplication [in]

Pointer to a <a href="/windows/desktop/api/p2p/ns-p2p-peer_application_registration_info">PEER_APPLICATION_REGISTRATION_INFO</a> structure that contains the UUID of the peer's application feature set as well as any additional peer-specific data.

### -param registrationType [in]

A <a href="/windows/desktop/api/p2p/ne-p2p-peer_application_registration_type">PEER_APPLICATION_REGISTRATION_TYPE</a> value that describes whether the peer's application is registered to the <b>current user</b> or <b>all users</b> of the peer's machine.

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

An <i>application</i> is a set of software or software  features available on the peer's endpoint. Commonly, this refers to software packages that support peer networking activities, like games or other collaborative applications.

The collaboration infrastructure can receive application invites from trusted contacts or from "People Near Me", which are based on the scope the collaboration infrastructure is signed in with using PeerCollabSignin.

A peer's application has a GUID representing a single specific application. When an application is registered for a peer, this GUID and the corresponding application can be made available to all trusted contacts of the peer, indicating the activities the peer can participate in. To unregister a peer's application, call <a href="/windows/desktop/api/p2p/nf-p2p-peercollabunregisterapplication">PeerCollabUnregisterApplication</a> with this GUID.

When registering an application, it is recommended that developers specify a relative path, such as <b>%ProgramFiles%</b>, instead of an absolute path. This prevents application failure due to a change in the location of application files. For example, if the <b>C:\ProgramFiles</b> directory is moved to <b>E:\\</b>. 

Only applications that are local to the machine can be registered. It is not possible to register when an application's executable path is located on a network share like a UNC path or locally-mapped network drive.

Applications can be registered in  the 'ALL_USERS' and 'CURRENT_USER' scopes. In the event an application is registered in both  scopes simultaneously, an application registered in 'CURRENT_USER' scope takes precedence over an application registered in 'ALL_USERS' scope.
It is important to note that to register for the registration type of 'ALL_USERS' the caller must be operating with administrative privileges.

The maximum number of applications that can be registered for a specific <i>registrationType</i> is 64.

## -see-also

<a href="/windows/desktop/api/p2p/ne-p2p-peer_application_registration_type">PEER_APPLICATION_REGISTRATION_TYPE</a>



<a href="/windows/desktop/P2PSdk/collaboration-api-functions">Peer Collaboration API Functions</a>



<a href="/windows/desktop/api/p2p/nf-p2p-peercollabunregisterapplication">PeerCollabUnregisterApplication</a>