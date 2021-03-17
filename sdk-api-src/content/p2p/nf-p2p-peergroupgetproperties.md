---
UID: NF:p2p.PeerGroupGetProperties
title: PeerGroupGetProperties function (p2p.h)
description: The PeerGroupGetProperties function retrieves information on the properties of a specified group.
helpviewer_keywords: ["PeerGroupGetProperties","PeerGroupGetProperties function [Peer Networking]","p2p.peergroupgetproperties","p2p/PeerGroupGetProperties"]
old-location: p2p\peergroupgetproperties.htm
tech.root: p2p
ms.assetid: 6273817f-9698-4c0b-93a9-9bbee2e5dc78
ms.date: 12/05/2018
ms.keywords: PeerGroupGetProperties, PeerGroupGetProperties function [Peer Networking], p2p.peergroupgetproperties, p2p/PeerGroupGetProperties
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
 - PeerGroupGetProperties
 - p2p/PeerGroupGetProperties
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
 - PeerGroupGetProperties
---

# PeerGroupGetProperties function


## -description

The <b>PeerGroupGetProperties</b> function retrieves information on the properties of a specified group.

## -parameters

### -param hGroup [in]

Handle to a peer group whose properties are retrieved. This handle is returned by the <a href="/windows/desktop/api/p2p/nf-p2p-peergroupcreate">PeerGroupCreate</a>, <a href="/windows/desktop/api/p2p/nf-p2p-peergroupopen">PeerGroupOpen</a>, or <a href="/windows/desktop/api/p2p/nf-p2p-peergroupjoin">PeerGroupJoin</a> function. This parameter is required.

### -param ppProperties [out]

Pointer to a  <a href="/windows/desktop/api/p2p/ns-p2p-peer_group_properties">PEER_GROUP_PROPERTIES</a> structure that contains information about peer   group properties. This data must be freed with <a href="/windows/desktop/api/p2p/nf-p2p-peerfreedata">PeerFreeData</a>. This parameter is required.

## -returns

Returns <b>S_OK</b>  if the operation succeeds. Otherwise, the function returns one of the following values.

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
There is not enough memory to perform a specified operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PEER_E_GROUP_NOT_READY</b></dt>
</dl>
</td>
<td width="60%">
The group is not in a state where peer group properties can be retrieved. For example, <a href="/windows/desktop/api/p2p/nf-p2p-peergroupjoin">PeerGroupJoin</a>  is called, but synchronization with the group database has not completed.

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

## -remarks

Group properties cannot be retrieved if a peer has not synchronized with a peer group database. To synchronize with a peer group database before calling this function, first call <a href="/windows/desktop/api/p2p/nf-p2p-peergroupconnect">PeerGroupConnect</a>.

## -see-also

<a href="/windows/desktop/api/p2p/ns-p2p-peer_group_properties">PEER_GROUP_PROPERTIES</a>



<a href="/windows/desktop/api/p2p/nf-p2p-peergroupcreate">PeerGroupCreate</a>



<a href="/windows/desktop/api/p2p/nf-p2p-peergroupjoin">PeerGroupJoin</a>



<a href="/windows/desktop/api/p2p/nf-p2p-peergroupopen">PeerGroupOpen</a>



<a href="/windows/desktop/api/p2p/nf-p2p-peergroupsetproperties">PeerGroupSetProperties</a>