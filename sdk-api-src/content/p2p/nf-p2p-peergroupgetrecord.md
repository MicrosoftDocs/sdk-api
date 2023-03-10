---
UID: NF:p2p.PeerGroupGetRecord
title: PeerGroupGetRecord function (p2p.h)
description: The PeerGroupGetRecord function retrieves a specific group record.
helpviewer_keywords: ["PeerGroupGetRecord","PeerGroupGetRecord function [Peer Networking]","p2p.peergroupgetrecord","p2p/PeerGroupGetRecord"]
old-location: p2p\peergroupgetrecord.htm
tech.root: p2p
ms.assetid: cf24bf5f-8ffc-4b86-80f7-dcb7621f49d2
ms.date: 12/05/2018
ms.keywords: PeerGroupGetRecord, PeerGroupGetRecord function [Peer Networking], p2p.peergroupgetrecord, p2p/PeerGroupGetRecord
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
 - PeerGroupGetRecord
 - p2p/PeerGroupGetRecord
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
 - PeerGroupGetRecord
---

# PeerGroupGetRecord function


## -description

The <b>PeerGroupGetRecord</b> function retrieves a specific group record.

## -parameters

### -param hGroup [in]

Handle to a group that contains a specific record. This handle is returned by the <a href="/windows/desktop/api/p2p/nf-p2p-peergroupcreate">PeerGroupCreate</a>, <a href="/windows/desktop/api/p2p/nf-p2p-peergroupopen">PeerGroupOpen</a>, or <a href="/windows/desktop/api/p2p/nf-p2p-peergroupjoin">PeerGroupJoin</a> function. This parameter is required.

### -param pRecordId [in]

Specifies the GUID value that uniquely identifies a required record within a peer group. This parameter is required.

### -param ppRecord [out]

Pointer to the address of a <a href="/windows/desktop/api/p2p/ns-p2p-peer_record">PEER_RECORD</a> structure that contains a returned record. This structure is freed by passing its pointer to <a href="/windows/desktop/api/p2p/nf-p2p-peerfreedata">PeerFreeData</a>. This parameter is required.

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
There is not enough memory to perform the specified operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PEER_E_GROUP_NOT_READY</b></dt>
</dl>
</td>
<td width="60%">
The peer group is not in a state where group records can be retrieved. For example, <a href="/windows/desktop/api/p2p/nf-p2p-peergroupjoin">PeerGroupJoin</a>  is called, but synchronization with the peer group database has not completed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PEER_E_INVALID_GROUP</b></dt>
</dl>
</td>
<td width="60%">
The handle to a peer group is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PEER_E_RECORD_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
A record that matches the supplied ID cannot be found in a peer group database.

</td>
</tr>
</table>
 

Cryptography-specific errors can be returned from the <a href="/windows/desktop/SecCrypto/microsoft-base-cryptographic-provider">Microsoft RSA Base Provider</a>. These errors are prefixed with CRYPT_* and defined in Winerror.h.

## -see-also

<a href="/windows/desktop/api/p2p/ns-p2p-peer_record"> PEER_RECORD</a>



<a href="/windows/desktop/api/p2p/nf-p2p-peerfreedata">PeerFreeData</a>



<a href="/windows/desktop/api/p2p/nf-p2p-peergroupcreate">PeerGroupCreate</a>



<a href="/windows/desktop/api/p2p/nf-p2p-peergroupdeleterecord">PeerGroupDeleteRecord</a>



<a href="/windows/desktop/api/p2p/nf-p2p-peergroupenumrecords">PeerGroupEnumRecords</a>



<a href="/windows/desktop/api/p2p/nf-p2p-peergroupjoin">PeerGroupJoin</a>



<a href="/windows/desktop/api/p2p/nf-p2p-peergroupopen">PeerGroupOpen</a>