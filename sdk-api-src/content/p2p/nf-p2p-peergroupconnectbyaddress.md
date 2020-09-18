---
UID: NF:p2p.PeerGroupConnectByAddress
title: PeerGroupConnectByAddress function (p2p.h)
description: Attempts to connect to the peer group that other peers with known IPv6 addresses are participating in.
helpviewer_keywords: ["PeerGroupConnectByAddress","PeerGroupConnectByAddress function [Peer Networking]","p2p.peergroupconnectbyaddress","p2p/PeerGroupConnectByAddress"]
old-location: p2p\peergroupconnectbyaddress.htm
tech.root: p2p
ms.assetid: 44885110-fcb1-402a-86c6-1229b087165b
ms.date: 12/05/2018
ms.keywords: PeerGroupConnectByAddress, PeerGroupConnectByAddress function [Peer Networking], p2p.peergroupconnectbyaddress, p2p/PeerGroupConnectByAddress
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
 - PeerGroupConnectByAddress
 - p2p/PeerGroupConnectByAddress
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
 - PeerGroupConnectByAddress
---

# PeerGroupConnectByAddress function


## -description

The <b>PeerGroupConnectByAddress</b> function  attempts to connect to the peer group that other peers with known IPv6 addresses are participating in. After this function is  called successfully, a peer can communicate with other members of the peer group.

## -parameters

### -param hGroup [in]

Handle to the peer group  to which a peer intends to connect. This handle is returned by the <a href="/windows/desktop/api/p2p/nf-p2p-peergroupcreate">PeerGroupCreate</a>, <a href="/windows/desktop/api/p2p/nf-p2p-peergroupopen">PeerGroupOpen</a>,<a href="/windows/desktop/api/p2p/nf-p2p-peergroupjoin">PeerGroupJoin</a>, or <a href="/windows/desktop/api/p2p/nf-p2p-peergrouppasswordjoin">PeerGroupPasswordJoin</a> function. This parameter is required.

### -param cAddresses [in]

The total number of <a href="/windows/desktop/api/p2p/ns-p2p-peer_address">PEER_ADDRESS</a> structures pointed to by <i>pAddresses</i>.

### -param pAddresses [in]

Pointer to a list of <a href="/windows/desktop/api/p2p/ns-p2p-peer_address">PEER_ADDRESS</a> structures that specify the endpoints of peers participating in the group.

## -returns

Returns S_OK if the operation succeeds. Otherwise, the function returns  the following value.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
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
 

Cryptography-specific errors may be returned from the <a href="/windows/desktop/SecCrypto/microsoft-base-cryptographic-provider">Microsoft RSA Base Provider</a>. These errors are prefixed with CRYPT_* and defined in Winerror.h.

## -remarks

If  a time-out value for PeerGroupConnectByAddress is not provided in the application, encountering a failure will cause the application to hang.  A time-out value  of 30 seconds is recommended.

## -see-also

<a href="/windows/desktop/api/p2p/ns-p2p-peer_address">PEER_ADDRESS</a>



<a href="/windows/desktop/api/p2p/nf-p2p-peergroupconnect">PeerGroupConnect</a>



<a href="/windows/desktop/api/p2p/nf-p2p-peergroupjoin">PeerGroupJoin</a>



<a href="/windows/desktop/api/p2p/nf-p2p-peergrouppasswordjoin">PeerGroupPasswordJoin</a>