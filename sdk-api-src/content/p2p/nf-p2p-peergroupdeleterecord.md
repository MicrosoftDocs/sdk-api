---
UID: NF:p2p.PeerGroupDeleteRecord
title: PeerGroupDeleteRecord function (p2p.h)
description: The PeerGroupDeleteRecord function deletes a record from a peer group. The creator, as well as any other member in an administrative role may delete a specific record.
helpviewer_keywords: ["PeerGroupDeleteRecord","PeerGroupDeleteRecord function [Peer Networking]","p2p.peergroupdeleterecord","p2p/PeerGroupDeleteRecord"]
old-location: p2p\peergroupdeleterecord.htm
tech.root: p2p
ms.assetid: e80fbf7f-2193-4a45-8a7f-46707ae4acfe
ms.date: 12/05/2018
ms.keywords: PeerGroupDeleteRecord, PeerGroupDeleteRecord function [Peer Networking], p2p.peergroupdeleterecord, p2p/PeerGroupDeleteRecord
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
 - PeerGroupDeleteRecord
 - p2p/PeerGroupDeleteRecord
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
 - PeerGroupDeleteRecord
---

# PeerGroupDeleteRecord function


## -description

The <b>PeerGroupDeleteRecord</b> function deletes a record from a peer group. The creator, as well as any other member in an administrative role may delete a specific record.

## -parameters

### -param hGroup [in]

Handle to the peer group that contains the record. This handle is returned by the <a href="/windows/desktop/api/p2p/nf-p2p-peergroupcreate">PeerGroupCreate</a>, <a href="/windows/desktop/api/p2p/nf-p2p-peergroupopen">PeerGroupOpen</a>, or <a href="/windows/desktop/api/p2p/nf-p2p-peergroupjoin">PeerGroupJoin</a> function. This parameter is required.

### -param pRecordId [in]

Specifies the GUID value that uniquely identifies the record to be deleted. This parameter is required.

## -returns

Returns S_OK  if the operation succeeds. Otherwise, the function returns one of the following values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PEER_E_GROUP_NOT_READY</b></dt>
</dl>
</td>
<td width="60%">
The peer group is not in a state where records can be deleted. For example, <a href="/windows/desktop/api/p2p/nf-p2p-peergroupjoin">PeerGroupJoin</a>  is called, but synchronization with the peer group database has not completed.

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
<tr>
<td width="40%">
<dl>
<dt><b>PEER_E_NOT_AUTHORIZED</b></dt>
</dl>
</td>
<td width="60%">
The current identity does not have the authorization to delete the record. In this case, the identity is not the creator or a member in an administrative role may delete a specific record.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PEER_E_RECORD_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The record cannot be located in the data store.

</td>
</tr>
</table>
 

Cryptography-specific errors can be returned from the <a href="/windows/desktop/SecCrypto/microsoft-base-cryptographic-provider">Microsoft RSA Base Provider</a>. These errors are prefixed with CRYPT_* and defined in Winerror.h.

## -see-also

<a href="/windows/desktop/api/p2p/nf-p2p-peergroupaddrecord">PeerGroupAddRecord</a>



<a href="/windows/desktop/api/p2p/nf-p2p-peergroupcreate">PeerGroupCreate</a>



<a href="/windows/desktop/api/p2p/nf-p2p-peergroupjoin">PeerGroupJoin</a>



<a href="/windows/desktop/api/p2p/nf-p2p-peergroupopen">PeerGroupOpen</a>



<a href="/windows/desktop/api/p2p/nf-p2p-peergroupupdaterecord">PeerGroupUpdateRecord</a>