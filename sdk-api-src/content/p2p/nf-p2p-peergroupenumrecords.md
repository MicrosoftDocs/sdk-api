---
UID: NF:p2p.PeerGroupEnumRecords
title: PeerGroupEnumRecords function (p2p.h)
description: The PeerGroupEnumRecords function creates an enumeration of peer group records.
helpviewer_keywords: ["PeerGroupEnumRecords","PeerGroupEnumRecords function [Peer Networking]","p2p.peergroupenumrecords","p2p/PeerGroupEnumRecords"]
old-location: p2p\peergroupenumrecords.htm
tech.root: p2p
ms.assetid: d9a0654a-850a-40bb-9112-03ec9bf47370
ms.date: 12/05/2018
ms.keywords: PeerGroupEnumRecords, PeerGroupEnumRecords function [Peer Networking], p2p.peergroupenumrecords, p2p/PeerGroupEnumRecords
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
 - PeerGroupEnumRecords
 - p2p/PeerGroupEnumRecords
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
 - PeerGroupEnumRecords
---

# PeerGroupEnumRecords function


## -description

The <b>PeerGroupEnumRecords</b> function creates an enumeration of peer group records.

## -parameters

### -param hGroup [in]

Handle to the peer group whose records are enumerated. This handle is returned by the <a href="/windows/desktop/api/p2p/nf-p2p-peergroupcreate">PeerGroupCreate</a>, <a href="/windows/desktop/api/p2p/nf-p2p-peergroupopen">PeerGroupOpen</a>, or <a href="/windows/desktop/api/p2p/nf-p2p-peergroupjoin">PeerGroupJoin</a> function. This parameter is required.

### -param pRecordType [in]

Pointer to  a <b>GUID</b> value that uniquely identifies a specific record type. If this parameter is <b>NULL</b>, all records are returned.

### -param phPeerEnum [out]

Pointer to the enumeration that contains the returned list of records. This handle is passed to  
	 <a href="/windows/desktop/api/p2p/nf-p2p-peergetnextitem">PeerGetNextItem</a> to retrieve the items, with each item represented as a pointer to a <a href="/windows/desktop/api/p2p/ns-p2p-peer_record">PEER_RECORD</a> structure. When finished, <a href="/windows/desktop/api/p2p/nf-p2p-peerendenumeration">PeerEndEnumeration</a> is called to return the memory used by the enumeration. This parameter is required.

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

<a href="/windows/desktop/api/p2p/nf-p2p-peerendenumeration">PeerEndEnumeration</a>



<a href="/windows/desktop/api/p2p/nf-p2p-peergetitemcount">PeerGetItemCount</a>



<a href="/windows/desktop/api/p2p/nf-p2p-peergetnextitem">PeerGetNextItem</a>



<a href="/windows/desktop/api/p2p/nf-p2p-peergroupgetrecord">PeerGroupGetRecord</a>