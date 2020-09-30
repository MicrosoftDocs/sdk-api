---
UID: NF:p2p.PeerGroupSearchRecords
title: PeerGroupSearchRecords function (p2p.h)
description: The PeerGroupSearchRecords function searches the local peer group database for records that match the supplied criteria.
helpviewer_keywords: ["PeerGroupSearchRecords","PeerGroupSearchRecords function [Peer Networking]","p2p.peergroupsearchrecords","p2p/PeerGroupSearchRecords"]
old-location: p2p\peergroupsearchrecords.htm
tech.root: p2p
ms.assetid: 7df13041-e802-47b6-8b44-14837c513936
ms.date: 12/05/2018
ms.keywords: PeerGroupSearchRecords, PeerGroupSearchRecords function [Peer Networking], p2p.peergroupsearchrecords, p2p/PeerGroupSearchRecords
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
 - PeerGroupSearchRecords
 - p2p/PeerGroupSearchRecords
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
 - PeerGroupSearchRecords
---

# PeerGroupSearchRecords function


## -description

The <b>PeerGroupSearchRecords</b> function searches the local peer group database for records that match the supplied criteria.

## -parameters

### -param hGroup [in]

Handle to the peer group whose local database is searched. This handle is returned by the <a href="/windows/desktop/api/p2p/nf-p2p-peergroupcreate">PeerGroupCreate</a>, <a href="/windows/desktop/api/p2p/nf-p2p-peergroupopen">PeerGroupOpen</a>, or <a href="/windows/desktop/api/p2p/nf-p2p-peergroupjoin">PeerGroupJoin</a> function. This parameter is required.

### -param pwzCriteria [in]

Pointer to a Unicode XML string that contains the record search query. For information about formulating an XML query string to search the peer group records database, see the <a href="/windows/desktop/P2PSdk/record-search-query-format">Record Search Query Format</a> documentation. This parameter is required.

### -param phPeerEnum [out]

Pointer to the enumeration that contains the returned list of records. This handle is passed to  
	 <a href="/windows/desktop/api/p2p/nf-p2p-peergetnextitem">PeerGetNextItem</a> to retrieve the items with each item represented as a pointer to a <a href="/windows/desktop/api/p2p/ns-p2p-peer_record">PEER_RECORD</a> structure. When finished, <a href="/windows/desktop/api/p2p/nf-p2p-peerendenumeration">PeerEndEnumeration</a> is called to return the memory used by the enumeration. This parameter is required.

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
There is not enough memory available to complete the operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PEER_E_INVALID_SEARCH</b></dt>
</dl>
</td>
<td width="60%">
The XML search query does not adhere to the <a href="/windows/desktop/P2PSdk/record-search-query-format">search query schema specification</a>.

</td>
</tr>
</table>
 

Cryptography-specific errors can be returned from the <a href="/windows/desktop/SecCrypto/microsoft-base-cryptographic-provider">Microsoft RSA Base Provider</a>. These errors are prefixed with CRYPT_* and defined in Winerror.h.

## -see-also

<a href="/windows/desktop/api/p2p/nf-p2p-peerendenumeration">PeerEndEnumeration</a>



<a href="/windows/desktop/api/p2p/nf-p2p-peergetnextitem">PeerGetNextItem</a>



<a href="/windows/desktop/api/p2p/nf-p2p-peergroupcreate">PeerGroupCreate</a>



<a href="/windows/desktop/api/p2p/nf-p2p-peergroupjoin">PeerGroupJoin</a>



<a href="/windows/desktop/api/p2p/nf-p2p-peergroupopen">PeerGroupOpen</a>



<a href="/windows/desktop/P2PSdk/record-search-query-format">Record Search Query Format</a>