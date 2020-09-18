---
UID: NF:p2p.PeerGroupPeerTimeToUniversalTime
title: PeerGroupPeerTimeToUniversalTime function (p2p.h)
description: The PeerGroupPeerTimeToUniversalTime function converts the peer group-maintained reference time value to a localized time value appropriate for display on a peer computer.
helpviewer_keywords: ["PeerGroupPeerTimeToUniversalTime","PeerGroupPeerTimeToUniversalTime function [Peer Networking]","p2p.peergrouppeertimetouniversaltime","p2p/PeerGroupPeerTimeToUniversalTime"]
old-location: p2p\peergrouppeertimetouniversaltime.htm
tech.root: p2p
ms.assetid: 27164da8-b5c7-41c1-bfe1-1c5797aa7ae1
ms.date: 12/05/2018
ms.keywords: PeerGroupPeerTimeToUniversalTime, PeerGroupPeerTimeToUniversalTime function [Peer Networking], p2p.peergrouppeertimetouniversaltime, p2p/PeerGroupPeerTimeToUniversalTime
req.header: p2p.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2 [desktop apps only],Windows XP with SP1 with the Advanced Networking Pack forWindows XP
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
 - PeerGroupPeerTimeToUniversalTime
 - p2p/PeerGroupPeerTimeToUniversalTime
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
 - PeerGroupPeerTimeToUniversalTime
---

# PeerGroupPeerTimeToUniversalTime function


## -description

The <b>PeerGroupPeerTimeToUniversalTime</b> function converts the peer group-maintained reference time value to a localized time value appropriate for display on a peer computer.

## -parameters

### -param hGroup [in]

Handle to the  peer group that a peer participates in. This handle is returned by the <a href="/windows/desktop/api/p2p/nf-p2p-peergroupcreate">PeerGroupCreate</a>, <a href="/windows/desktop/api/p2p/nf-p2p-peergroupopen">PeerGroupOpen</a>, or <a href="/windows/desktop/api/p2p/nf-p2p-peergroupjoin">PeerGroupJoin</a> function. This parameter is required.

### -param pftPeerTime [in]

Pointer to the peer time value—Coordinated Universal Time (UTC)—that is represented as a <a href="/windows/desktop/P2PSdk/graphing-reference-links">FILETIME</a> structure.  This parameter is required.

### -param pftUniversalTime [out]

Pointer to the returned universal time value that is  represented as a <a href="/windows/desktop/P2PSdk/graphing-reference-links">FILETIME</a> structure. This parameter is <b>NULL</b> if an error occurs.

## -returns

Returns <b>S_OK</b> if the function succeeds. Otherwise, the function returns either one of the remote procedure call (RPC) errors or one of the following errors.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One of the parameters is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PEER_E_GROUP_NOT_READY</b></dt>
</dl>
</td>
<td width="60%">
The peer group is not in a state that peer time can be  retrieved accurately, for example, <a href="/windows/desktop/api/p2p/nf-p2p-peergroupjoin">PeerGroupJoin</a> has been called, but synchronization with the group database has not completed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PEER_E_NOT_INITIALIZED</b></dt>
</dl>
</td>
<td width="60%">
The peer group must be  initialized with a call to <a href="/windows/desktop/api/p2p/nf-p2p-peergroupstartup">PeerGroupStartup</a> before using this function.

</td>
</tr>
</table>
 

Cryptography-specific errors can be returned from the <a href="/windows/desktop/SecCrypto/microsoft-base-cryptographic-provider">Microsoft RSA Base Provider</a>. These errors are prefixed with CRYPT_* and defined in Winerror.h.

## -remarks

<i>Universal time</i> is  the universal time value maintained on a peer  computer.

<i>Peer time</i> is a common reference time maintained by a peer group, expressed as UTC. It is often offset from the universal time value, and is used to correct latency issues.

Universal time can be converted to peer time by calling the converse function <a href="/windows/desktop/api/p2p/nf-p2p-peergroupuniversaltimetopeertime">PeerGroupUniversalTimeToPeerTime</a>.

## -see-also

<a href="/windows/desktop/api/p2p/nf-p2p-peergroupuniversaltimetopeertime">PeerGroupUniversalTimeToPeerTime</a>