---
UID: NF:p2p.PeerGroupCloseDirectConnection
title: PeerGroupCloseDirectConnection function (p2p.h)
description: The PeerGroupCloseDirectConnection function closes a specific direct connection between two peers.
helpviewer_keywords: ["PeerGroupCloseDirectConnection","PeerGroupCloseDirectConnection function [Peer Networking]","p2p.peergroupclosedirectconnection","p2p/PeerGroupCloseDirectConnection"]
old-location: p2p\peergroupclosedirectconnection.htm
tech.root: p2p
ms.assetid: 56b47743-f205-407b-80f2-03e3c9b78be1
ms.date: 12/05/2018
ms.keywords: PeerGroupCloseDirectConnection, PeerGroupCloseDirectConnection function [Peer Networking], p2p.peergroupclosedirectconnection, p2p/PeerGroupCloseDirectConnection
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
 - PeerGroupCloseDirectConnection
 - p2p/PeerGroupCloseDirectConnection
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
 - PeerGroupCloseDirectConnection
---

# PeerGroupCloseDirectConnection function


## -description

The <b>PeerGroupCloseDirectConnection</b> function closes a specific direct connection between two peers.

## -parameters

### -param hGroup [in]

Handle to the peer group that contains the peers involved in the direct connection. This handle is returned by the <a href="/windows/desktop/api/p2p/nf-p2p-peergroupcreate">PeerGroupCreate</a>, <a href="/windows/desktop/api/p2p/nf-p2p-peergroupopen">PeerGroupOpen</a>, or <a href="/windows/desktop/api/p2p/nf-p2p-peergroupjoin">PeerGroupJoin</a> function. This parameter is required.

### -param ullConnectionId [in]

Specifies the connection ID  to disconnect from. This parameter is required and has no default value.

## -returns

Returns S_OK if the operation succeeds. Otherwise, the function returns one of the following values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PEER_E_CONNECTION_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
A direct connection that matches the supplied connection ID cannot be found.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PEER_E_INVALID_GROUP</b></dt>
</dl>
</td>
<td width="60%">
The handle to the peer group is invalid.

</td>
</tr>
</table>
 

Cryptography-specific errors can be returned from the <a href="/windows/desktop/SecCrypto/microsoft-base-cryptographic-provider">Microsoft RSA Base Provider</a>. These errors are prefixed with CRYPT_* and defined in Winerror.h.

## -see-also

<a href="/windows/desktop/api/p2p/nf-p2p-peergroupcreate">PeerGroupCreate</a>



<a href="/windows/desktop/api/p2p/nf-p2p-peergroupjoin">PeerGroupJoin</a>



<a href="/windows/desktop/api/p2p/nf-p2p-peergroupopen">PeerGroupOpen</a>



<a href="/windows/desktop/api/p2p/nf-p2p-peergroupopendirectconnection">PeerGroupOpenDirectConnection</a>