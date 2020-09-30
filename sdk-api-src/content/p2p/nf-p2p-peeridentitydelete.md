---
UID: NF:p2p.PeerIdentityDelete
title: PeerIdentityDelete function (p2p.h)
description: The PeerIdentityDelete function permanently deletes a peer identity. This includes removing all certificates, private keys, and all group information associated with a specified peer identity.
helpviewer_keywords: ["PeerIdentityDelete","PeerIdentityDelete function [Peer Networking]","p2p.peeridentitydelete","p2p/PeerIdentityDelete"]
old-location: p2p\peeridentitydelete.htm
tech.root: p2p
ms.assetid: 9738f6b1-cd88-4950-bab1-f97613a49e03
ms.date: 12/05/2018
ms.keywords: PeerIdentityDelete, PeerIdentityDelete function [Peer Networking], p2p.peeridentitydelete, p2p/PeerIdentityDelete
req.header: p2p.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2 [desktop apps only],Windows XP with SP1 with the Advanced Networking Pack for Windows XP
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
 - PeerIdentityDelete
 - p2p/PeerIdentityDelete
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
 - PeerIdentityDelete
---

# PeerIdentityDelete function


## -description

The <b>PeerIdentityDelete</b> function permanently deletes a peer identity. This includes removing all certificates, private keys, and all group information associated with a specified peer identity.

## -parameters

### -param pwzIdentity [in]

Specifies a peer identity to delete.

## -returns

If the function call succeeds, the return value is <b>S_OK</b>. Otherwise, it  returns one of the following values.

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
The parameter is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PEER_E_GROUPS_EXIST</b></dt>
</dl>
</td>
<td width="60%">
The peer identity cannot be deleted because it has  peer groups associated with it.   All peer groups associated with the specified identity must be deleted by using   <a href="/windows/desktop/api/p2p/nf-p2p-peergroupdelete">PeerGroupDelete</a> before a call to <a href="/windows/desktop/api/p2p/nf-p2p-peeridentitydelete">PeerIdentityDelete</a> can succeed.


</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PEER_E_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
A peer identity that matches the specified name cannot be found.

</td>
</tr>
</table>