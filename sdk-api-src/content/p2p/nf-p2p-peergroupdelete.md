---
UID: NF:p2p.PeerGroupDelete
title: PeerGroupDelete function (p2p.h)
description: The PeerGroupDelete function deletes the local data and certificate associated with a peer group.
helpviewer_keywords: ["PeerGroupDelete","PeerGroupDelete function [Peer Networking]","p2p.peergroupdelete","p2p/PeerGroupDelete"]
old-location: p2p\peergroupdelete.htm
tech.root: p2p
ms.assetid: e98df845-71d9-41f9-bf05-b46014e861df
ms.date: 12/05/2018
ms.keywords: PeerGroupDelete, PeerGroupDelete function [Peer Networking], p2p.peergroupdelete, p2p/PeerGroupDelete
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
 - PeerGroupDelete
 - p2p/PeerGroupDelete
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
 - PeerGroupDelete
---

# PeerGroupDelete function


## -description

The <b>PeerGroupDelete</b> function deletes the local data and certificate associated with a peer group.

## -parameters

### -param pwzIdentity [in]

Pointer to a Unicode string that contains the identity opening the specified peer group. If this parameter is <b>NULL</b>, the implementation uses the identity obtained from <a href="/windows/desktop/api/p2p/nf-p2p-peeridentitygetdefault">PeerIdentityGetDefault</a>.

### -param pwzGroupPeerName [in]

Pointer to a Unicode string that contains the peer name of the peer group for which data is deleted. This parameter is required. The group
	name can be obtained by calling <a href="/windows/desktop/api/p2p/nf-p2p-peergroupgetproperties">PeerGroupGetProperties</a>  prior to <a href="/windows/desktop/api/p2p/nf-p2p-peergroupclose">PeerGroupClose</a>, or by parsing the invitation with
	<a href="/windows/desktop/api/p2p/nf-p2p-peergroupparseinvitation">PeerGroupParseInvitation</a>.

## -returns

Returns S_OK  if the operation succeeds. Otherwise, the function returns one of the following values.

<div class="alert"><b>Note</b>  If a delete operation fails due to a file system error, the appropriate file system error is returned.</div>
<div> </div>
<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ACCESSDENIED</b></dt>
</dl>
</td>
<td width="60%">
Access to the peer  group database is denied. Ensure that the peer has permission to perform this operation. In this case, the peer must be the original creator of the peer group.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One of the parameters is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PEER_E_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The peer group cannot be found.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PEER_E_NO_KEY_ACCESS</b></dt>
</dl>
</td>
<td width="60%">
Access to the identity or peer group keys is denied. Typically, this is  caused by an incorrect access control list (ACL) for the folder that contains the user or computer keys. This can happen when the ACL is  reset manually. 


</td>
</tr>
</table>
 

Cryptography-specific errors can be returned from the <a href="/windows/desktop/SecCrypto/microsoft-base-cryptographic-provider">Microsoft RSA Base Provider</a>. These errors are prefixed with CRYPT_* and defined in Winerror.h.

## -remarks

If a peer group is deleted, all handles associated with that group immediately become invalid. As a best practice,  ensure that all handles for this group are closed before calling this function. Otherwise, this data is deleted from  all other running peer applications that use it, which can cause  errors and instability.

## -see-also

<a href="/windows/desktop/api/p2p/nf-p2p-peergroupcreate">PeerGroupCreate</a>