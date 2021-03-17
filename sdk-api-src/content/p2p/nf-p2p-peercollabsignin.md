---
UID: NF:p2p.PeerCollabSignin
title: PeerCollabSignin function (p2p.h)
description: Signs the peer into a hosted Internet (serverless presence) or subnet (&quot;People Near Me&quot;) peer collaboration network presence provider.
helpviewer_keywords: ["PeerCollabSignin","PeerCollabSignin function [Peer Networking]","p2p.peercollabsignin","p2p/PeerCollabSignin"]
old-location: p2p\peercollabsignin.htm
tech.root: p2p
ms.assetid: 927cccfa-2711-439c-833f-348087927c09
ms.date: 12/05/2018
ms.keywords: PeerCollabSignin, PeerCollabSignin function [Peer Networking], p2p.peercollabsignin, p2p/PeerCollabSignin
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
 - PeerCollabSignin
 - p2p/PeerCollabSignin
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
 - PeerCollabSignin
---

# PeerCollabSignin function


## -description

The <b>PeerCollabSignin</b> function signs the peer into a hosted Internet (serverless presence) or subnet ("People Near Me") peer collaboration network presence provider.

## -parameters

### -param hwndParent [in]

Windows handle to the parent application signing in.

### -param dwSigninOptions [in]

<a href="/windows/desktop/api/p2p/ne-p2p-peer_signin_flags">PEER_SIGNIN_FLAGS</a> enumeration value that contains the presence provider sign-in options for the calling peer.

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
<tr>
<td width="40%">
<dl>
<dt><b>PEER_E_SERVICE_NOT_AVAILABLE</b></dt>
</dl>
</td>
<td width="60%">
An attempt was made to call <a href="/windows/desktop/api/p2p/nf-p2p-peercollabsignin">PeerCollabSignIn</a> from an elevated process.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PEER_S_NO_CONNECTIVITY</b></dt>
</dl>
</td>
<td width="60%">
The sign-in succeeded, but IPv6 addresses are not available at this time.

</td>
</tr>
</table>

## -remarks

If the p2phost.exe service is not running, this function will launch it.

If an attempt is made to launch the p2phost.exe service from an  elevated process, an error is returned. As a result, security cannot be compromised by an application mistakenly granting administrative privileges   to p2phost.exe. It is not possible to launch p2phost.exe in a non-interactive mode, as it needs to display Windows dialog boxes for incoming invites.

Calling <b>PeerCollabSignin</b> displays a sign-in user interface if the user has not authorized automatic sign-in. If <i>hwndParent</i> is specified, the user interface window will use <i>hwndParent</i> as the parent window.

When a user signs in to "People Near Me", the user's display name, machine name, and IP address are published to peers on the  subnet. The user can optionally specify a display picture for publishing. This information is not published if <b>PeerCollabSignin</b> is not called or the user signs out. 

Once signed in, the user can view a list of peers signed in on the subnet and available for interaction. This list will be empty if nobody else has signed in to "People Near Me" on the subnet.

 Multiple applications can  use the infrastructure at any given moment. It is not recommended for a single application to call <a href="/windows/desktop/api/p2p/nf-p2p-peercollabsignout">PeerCollabSignout</a>, as other applications will not be able to use the infrastructure.
Applications must also be prepared to handle the user signing in and signing out, or situations where a machine goes to sleep or hibernation.


The <b>PeerCollabSignin</b> function currently requires up to two seconds to complete.

Display names are not necessarily unique. Users should verify the identity of the person using a display name by e-mail, phone, or in person before accepting an invitation to interact.

To sign out of a peer collaborative network, call <a href="/windows/desktop/api/p2p/nf-p2p-peercollabsignout">PeerCollabSignout</a> with the same set of sign-in options. A user can also sign out through the user interface.

## -see-also

<a href="/windows/desktop/api/p2p/ne-p2p-peer_signin_flags">PEER_SIGNIN_FLAGS</a>



<a href="/windows/desktop/P2PSdk/collaboration-api-functions">Peer Collaboration API Functions</a>



<a href="/windows/desktop/api/p2p/nf-p2p-peercollabgetsigninoptions">PeerCollabGetSigninOptions</a>



<a href="/windows/desktop/api/p2p/nf-p2p-peercollabsignout">PeerCollabSignOut</a>