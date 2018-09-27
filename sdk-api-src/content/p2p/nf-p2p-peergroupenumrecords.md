---
UID: NF:p2p.PeerGroupEnumRecords
title: PeerGroupEnumRecords function
author: windows-sdk-content
description: The PeerGroupEnumRecords function creates an enumeration of peer group records.
old-location: p2p\peergroupenumrecords.htm
tech.root: p2psdk
ms.assetid: d9a0654a-850a-40bb-9112-03ec9bf47370
ms.author: windowssdkdev
ms.date: 08/31/2018
ms.keywords: PeerGroupEnumRecords, PeerGroupEnumRecords function [Peer Networking], p2p.peergroupenumrecords, p2p/PeerGroupEnumRecords
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
req.lib: P2P.lib
req.dll: P2P.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - P2P.dll
api_name:
 - PeerGroupEnumRecords
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PeerGroupEnumRecords function


## -description


The <b>PeerGroupEnumRecords</b> function creates an enumeration of peer group records.


## -parameters




### -param hGroup [in]

Handle to the peer group whose records are enumerated. This handle is returned by the <a href="https://msdn.microsoft.com/b85d87c6-28b7-49f8-865c-9d246f89367e">PeerGroupCreate</a>, <a href="https://msdn.microsoft.com/cfaf244f-8786-4801-926d-f6c79bfa4275">PeerGroupOpen</a>, or <a href="https://msdn.microsoft.com/a7f5689d-4849-4363-bc61-3fed63f4287b">PeerGroupJoin</a> function. This parameter is required.


### -param pRecordType [in]

Pointer to  a <b>GUID</b> value that uniquely identifies a specific record type. If this parameter is <b>NULL</b>, all records are returned.


### -param phPeerEnum [out]

Pointer to the enumeration that contains the returned list of records. This handle is passed to  
	 <a href="https://msdn.microsoft.com/015faeb3-82d9-49e5-a451-7394bf83240f">PeerGetNextItem</a> to retrieve the items, with each item represented as a pointer to a <a href="https://msdn.microsoft.com/4e0a1c44-e5a4-42d6-bb56-9bdcf7f9e6f1">PEER_RECORD</a> structure. When finished, <a href="https://msdn.microsoft.com/cc9484fb-57b9-4970-91b8-c74db6bf2248">PeerEndEnumeration</a> is called to return the memory used by the enumeration. This parameter is required.


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
 

Cryptography-specific errors can be returned from the <a href="https://msdn.microsoft.com/c36025c5-a407-4a05-8780-23f8107730df">Microsoft RSA Base Provider</a>. These errors are prefixed with CRYPT_* and defined in Winerror.h.




## -see-also




<a href="https://msdn.microsoft.com/cc9484fb-57b9-4970-91b8-c74db6bf2248">PeerEndEnumeration</a>



<a href="https://msdn.microsoft.com/8f6fec31-8867-4d65-b5b0-e6506be9c991">PeerGetItemCount</a>



<a href="https://msdn.microsoft.com/015faeb3-82d9-49e5-a451-7394bf83240f">PeerGetNextItem</a>



<a href="https://msdn.microsoft.com/cf24bf5f-8ffc-4b86-80f7-dcb7621f49d2">PeerGroupGetRecord</a>
 

 

