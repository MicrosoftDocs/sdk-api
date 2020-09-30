---
UID: NF:p2p.PeerIdentityGetFriendlyName
title: PeerIdentityGetFriendlyName function (p2p.h)
description: The PeerIdentityGetFriendlyName function returns the friendly name of the peer identity.
helpviewer_keywords: ["PeerIdentityGetFriendlyName","PeerIdentityGetFriendlyName function [Peer Networking]","p2p.peeridentitygetfriendlyname","p2p/PeerIdentityGetFriendlyName"]
old-location: p2p\peeridentitygetfriendlyname.htm
tech.root: p2p
ms.assetid: c0d823db-9c2c-46c1-99b8-87fe7fdc9343
ms.date: 12/05/2018
ms.keywords: PeerIdentityGetFriendlyName, PeerIdentityGetFriendlyName function [Peer Networking], p2p.peeridentitygetfriendlyname, p2p/PeerIdentityGetFriendlyName
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
 - PeerIdentityGetFriendlyName
 - p2p/PeerIdentityGetFriendlyName
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
 - PeerIdentityGetFriendlyName
---

# PeerIdentityGetFriendlyName function


## -description

The <b>PeerIdentityGetFriendlyName</b> function returns the friendly name of the peer identity.

## -parameters

### -param pwzIdentity [in]

Specifies the peer identity to obtain a friendly name.

### -param ppwzFriendlyName [out]

Receives a pointer to the friendly name. When <i>ppwzFriendlyName</i> is not required anymore, the application is responsible for freeing this string by calling  <a href="/windows/desktop/api/p2p/nf-p2p-peerfreedata">PeerFreeData</a>.

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
One of the parameters is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
There is not enough memory to perform the specified operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PEER_E_NO_KEY_ACCESS</b></dt>
</dl>
</td>
<td width="60%">
Access to the peer identity or peer group keys is denied. Typically, this is caused by an incorrect access control list (ACL) for the folder that contains the user or computer keys. This can happen when the ACL has been  reset manually. 

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

## -see-also

<a href="/windows/desktop/api/p2p/nf-p2p-peerfreedata">PeerFreeData</a>



<a href="/windows/desktop/api/p2p/nf-p2p-peeridentitysetfriendlyname">PeerIdentitySetFriendlyName</a>