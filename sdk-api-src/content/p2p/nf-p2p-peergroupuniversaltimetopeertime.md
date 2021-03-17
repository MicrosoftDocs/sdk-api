---
UID: NF:p2p.PeerGroupUniversalTimeToPeerTime
title: PeerGroupUniversalTimeToPeerTime function (p2p.h)
description: The PeerGroupUniversalTimeToPeerTime function converts a local time value from a peer's computer to a common peer group time value.
helpviewer_keywords: ["PeerGroupUniversalTimeToPeerTime","PeerGroupUniversalTimeToPeerTime function [Peer Networking]","p2p.peergroupuniversaltimetopeertime","p2p/PeerGroupUniversalTimeToPeerTime"]
old-location: p2p\peergroupuniversaltimetopeertime.htm
tech.root: p2p
ms.assetid: 8d64c66a-96c3-48c4-82fa-c57554074729
ms.date: 12/05/2018
ms.keywords: PeerGroupUniversalTimeToPeerTime, PeerGroupUniversalTimeToPeerTime function [Peer Networking], p2p.peergroupuniversaltimetopeertime, p2p/PeerGroupUniversalTimeToPeerTime
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
 - PeerGroupUniversalTimeToPeerTime
 - p2p/PeerGroupUniversalTimeToPeerTime
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
 - PeerGroupUniversalTimeToPeerTime
---

# PeerGroupUniversalTimeToPeerTime function


## -description

The <b>PeerGroupUniversalTimeToPeerTime</b> function converts a local time value from a peer's computer to a common peer group time value.

## -parameters

### -param hGroup [in]

Handle to the  peer group a peer participates in. This handle is returned by the <a href="/windows/desktop/api/p2p/nf-p2p-peergroupcreate">PeerGroupCreate</a>, <a href="/windows/desktop/api/p2p/nf-p2p-peergroupopen">PeerGroupOpen</a>, or <a href="/windows/desktop/api/p2p/nf-p2p-peergroupjoin">PeerGroupJoin</a> function. This parameter is required.

### -param pftUniversalTime [in]

Pointer to the universal time value, represented as a <a href="/windows/desktop/P2PSdk/graphing-reference-links">FILETIME</a> structure. This parameter is required.

### -param pftPeerTime [out]

Pointer to the returned peer time—Greenwich Mean Time (GMT) value that is represented as a <a href="/windows/desktop/P2PSdk/graphing-reference-links">FILETIME</a> structure. This parameter is <b>NULL</b> if an error occurs.

## -returns

Returns <b>S_OK</b> if the function succeeds. Otherwise, the function returns either one of the RPC errors or one of the following values.

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
The peer group is not in a state where peer time can be accurately calculated. For example, <a href="/windows/desktop/api/p2p/nf-p2p-peergroupjoin">PeerGroupJoin</a> has been called, but synchronization with the peer group database has not completed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PEER_E_NOT_INITIALIZED</b></dt>
</dl>
</td>
<td width="60%">
The group must be  initialized with a call to <a href="/windows/desktop/api/p2p/nf-p2p-peergroupstartup">PeerGroupStartup</a> before using this function.

</td>
</tr>
</table>
 

Cryptography-specific errors can be returned from the <a href="/windows/desktop/SecCrypto/microsoft-base-cryptographic-provider">Microsoft RSA Base Provider</a>. These errors are prefixed with CRYPT_* and defined in Winerror.h.

## -remarks

<i>Universal time</i> is  the universal time value maintained on a peer's computer.

<i>Peer time</i> is a common reference time maintained by a peer group, expressed as Coordinated Universal Time (UTC). It is often offset from the universal time value, and is used to correct latency issues.

Peer time can be converted to universal time by calling the converse function <a href="/windows/desktop/api/p2p/nf-p2p-peergrouppeertimetouniversaltime">PeerGroupPeerTimeToUniversalTime</a>.

## -see-also

<a href="/windows/desktop/api/p2p/nf-p2p-peergrouppeertimetouniversaltime">PeerGroupPeerTimeToUniversalTime</a>