---
UID: NF:p2p.PeerCollabGetSigninOptions
title: PeerCollabGetSigninOptions function (p2p.h)
description: Obtains the peer's current signed-in peer collaboration network presence options.
helpviewer_keywords: ["PeerCollabGetSigninOptions","PeerCollabGetSigninOptions function [Peer Networking]","p2p.peercollabgetsigninoptions","p2p/PeerCollabGetSigninOptions"]
old-location: p2p\peercollabgetsigninoptions.htm
tech.root: p2p
ms.assetid: 2b1452d3-2474-40c9-a913-de7e148e2d94
ms.date: 12/05/2018
ms.keywords: PeerCollabGetSigninOptions, PeerCollabGetSigninOptions function [Peer Networking], p2p.peercollabgetsigninoptions, p2p/PeerCollabGetSigninOptions
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
 - PeerCollabGetSigninOptions
 - p2p/PeerCollabGetSigninOptions
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
 - PeerCollabGetSigninOptions
---

# PeerCollabGetSigninOptions function


## -description

The <b>PeerCollabGetSigninOptions</b> function obtains the peer's current signed-in peer collaboration network presence options.

## -parameters

### -param pdwSigninOptions [out]

The <a href="/windows/desktop/api/p2p/ne-p2p-peer_signin_flags">PEER_SIGNIN_FLAGS</a> enumeration value is returned by this function.

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
<dt><b>PEER_E_NOT_SIGNED_IN</b></dt>
</dl>
</td>
<td width="60%">
The application has not signed into the peer collaboration network with a previous call to <a href="/windows/desktop/api/p2p/nf-p2p-peercollabsignin">PeerCollabSignIn</a>.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/p2p/ne-p2p-peer_signin_flags">PEER_SIGNIN_FLAGS</a>



<a href="/windows/desktop/P2PSdk/collaboration-api-functions">Peer Collaboration API Functions</a>



<a href="/windows/desktop/api/p2p/nf-p2p-peercollabsignin">PeerCollabSignIn</a>



<a href="/windows/desktop/api/p2p/nf-p2p-peercollabsignout">PeerCollabSignOut</a>