---
UID: NF:p2p.PeerCollabSignout
title: PeerCollabSignout function (p2p.h)
description: Signs a peer out of a specific type of peer collaboration network presence provider.
helpviewer_keywords: ["PeerCollabSignout","PeerCollabSignout function [Peer Networking]","p2p.peercollabsignout","p2p/PeerCollabSignout"]
old-location: p2p\peercollabsignout.htm
tech.root: p2p
ms.assetid: aa69a233-6104-47c6-a0b5-378794108623
ms.date: 12/05/2018
ms.keywords: PeerCollabSignout, PeerCollabSignout function [Peer Networking], p2p.peercollabsignout, p2p/PeerCollabSignout
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
 - PeerCollabSignout
 - p2p/PeerCollabSignout
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
 - PeerCollabSignout
---

# PeerCollabSignout function


## -description

The <b>PeerCollabSignout</b> function signs a peer out of a specific type of peer collaboration network presence provider.

## -parameters

### -param dwSigninOptions [in]

<a href="/windows/desktop/api/p2p/ne-p2p-peer_signin_flags">PEER_SIGNIN_FLAGS</a> enumeration value that contains the presence provider sign-in options for the calling peer. This value is obtained by calling <a href="/windows/desktop/api/p2p/nf-p2p-peercollabgetsigninoptions">PeerCollabGetSigninOptions</a> from the peer application.

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
The application did not make a previous call to <a href="/windows/desktop/api/p2p/nf-p2p-peercollabstartup">PeerCollabStartup</a>.

</td>
</tr>
</table>

## -remarks

If the local peer's collaboration infrastructure is signed out of both Internet and People Near Me presence, all transient information like objects and the endpoint ID are deleted. Any application that uses this information must republish the information. A single event that indicates signout is raised, instead of sending multiple individual events for each object or application. 

 Multiple applications can  use the infrastructure at any given moment. It is not recommended for a single application to sign out, as other applications will not be able to use the infrastructure.
Applications must also be prepared to handle user sign in and sign out, or situations where a machine goes to sleep or into hibernation.

## -see-also

<a href="/windows/desktop/api/p2p/ne-p2p-peer_signin_flags">PEER_SIGNIN_FLAGS</a>



<a href="/windows/desktop/P2PSdk/collaboration-api-functions">Peer Collaboration API Functions</a>



<a href="/windows/desktop/api/p2p/nf-p2p-peercollabgetsigninoptions">PeerCollabGetSigninOptions</a>