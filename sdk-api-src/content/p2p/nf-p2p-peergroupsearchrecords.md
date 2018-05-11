---
UID: NF:p2p.PeerGroupSearchRecords
title: PeerGroupSearchRecords function
author: windows-driver-content
description: The PeerGroupSearchRecords function searches the local peer group database for records that match the supplied criteria.
old-location: p2p\peergroupsearchrecords.htm
old-project: P2PSdk
ms.assetid: 7df13041-e802-47b6-8b44-14837c513936
ms.author: windowsdriverdev
ms.date: 5/8/2018
ms.keywords: PeerGroupSearchRecords, PeerGroupSearchRecords function [Peer Networking], p2p.peergroupsearchrecords, p2p/PeerGroupSearchRecords
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
req.typenames: PEER_WATCH_PERMISSION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	P2P.dll
api_name:
-	PeerGroupSearchRecords
product: Windows
targetos: Windows
req.lib: P2P.lib
req.dll: P2P.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# PeerGroupSearchRecords function


## -description



      The <b>PeerGroupSearchRecords</b> function searches the local peer group database for records that match the supplied criteria.


## -parameters




### -param hGroup [in]

Handle to the peer group whose local database is searched. This handle is returned by the <a href="https://msdn.microsoft.com/b85d87c6-28b7-49f8-865c-9d246f89367e">PeerGroupCreate</a>, <a href="https://msdn.microsoft.com/cfaf244f-8786-4801-926d-f6c79bfa4275">PeerGroupOpen</a>, or <a href="https://msdn.microsoft.com/a7f5689d-4849-4363-bc61-3fed63f4287b">PeerGroupJoin</a> function. This parameter is required.


### -param pwzCriteria [in]

Pointer to a Unicode XML string that contains the record search query. For information about formulating an XML query string to search the peer group records database, see the <a href="https://msdn.microsoft.com/2c5ab425-6959-418a-8d9a-c8155257fc7e">Record Search Query Format</a> documentation. This parameter is required.


### -param phPeerEnum [out]

Pointer to the enumeration that contains the returned list of records. This handle is passed to  
	 <a href="https://msdn.microsoft.com/015faeb3-82d9-49e5-a451-7394bf83240f">PeerGetNextItem</a> to retrieve the items with each item represented as a pointer to a <a href="https://msdn.microsoft.com/4e0a1c44-e5a4-42d6-bb56-9bdcf7f9e6f1">PEER_RECORD</a> structure. When finished, <a href="https://msdn.microsoft.com/cc9484fb-57b9-4970-91b8-c74db6bf2248">PeerEndEnumeration</a> is called to return the memory used by the enumeration. This parameter is required.


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
The XML search query does not adhere to the <a href="https://msdn.microsoft.com/2c5ab425-6959-418a-8d9a-c8155257fc7e">search query schema specification</a>.

</td>
</tr>
</table>
 

Cryptography-specific errors can be returned from the <a href="https://msdn.microsoft.com/c36025c5-a407-4a05-8780-23f8107730df">Microsoft RSA Base Provider</a>. These errors are prefixed with CRYPT_* and defined in Winerror.h.




## -see-also




<a href="https://msdn.microsoft.com/cc9484fb-57b9-4970-91b8-c74db6bf2248">PeerEndEnumeration</a>



<a href="https://msdn.microsoft.com/015faeb3-82d9-49e5-a451-7394bf83240f">PeerGetNextItem</a>



<a href="https://msdn.microsoft.com/b85d87c6-28b7-49f8-865c-9d246f89367e">PeerGroupCreate</a>



<a href="https://msdn.microsoft.com/a7f5689d-4849-4363-bc61-3fed63f4287b">PeerGroupJoin</a>



<a href="https://msdn.microsoft.com/cfaf244f-8786-4801-926d-f6c79bfa4275">PeerGroupOpen</a>



<a href="https://msdn.microsoft.com/2c5ab425-6959-418a-8d9a-c8155257fc7e">Record Search Query Format</a>
 

 

