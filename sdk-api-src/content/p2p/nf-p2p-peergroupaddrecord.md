---
UID: NF:p2p.PeerGroupAddRecord
title: PeerGroupAddRecord function
author: windows-sdk-content
description: The PeerGroupAddRecord function adds a new record to the peer group, which is propagated to all participating peers.
old-location: p2p\peergroupaddrecord.htm
tech.root: P2PSdk
ms.assetid: d9ca87bc-30da-4a19-b34a-8d8388ccd19a
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: PeerGroupAddRecord, PeerGroupAddRecord function [Peer Networking], p2p.peergroupaddrecord, p2p/PeerGroupAddRecord
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
 - PeerGroupAddRecord
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PeerGroupAddRecord function


## -description


The <b>PeerGroupAddRecord</b> function adds a new record to the peer group, which is propagated to all participating peers.


## -parameters




### -param hGroup [in]

Handle to the peer group. This handle is returned by the <a href="https://msdn.microsoft.com/b85d87c6-28b7-49f8-865c-9d246f89367e">PeerGroupCreate</a>, <a href="https://msdn.microsoft.com/cfaf244f-8786-4801-926d-f6c79bfa4275">PeerGroupOpen</a>, or <a href="https://msdn.microsoft.com/a7f5689d-4849-4363-bc61-3fed63f4287b">PeerGroupJoin</a> function. This parameter is required.


### -param pRecord [in]

Pointer to a <a href="https://msdn.microsoft.com/4e0a1c44-e5a4-42d6-bb56-9bdcf7f9e6f1">PEER_RECORD</a> structure that is added to the peer group specified in <i>hGroup</i>. This parameter is required.

The following members in <a href="https://msdn.microsoft.com/4e0a1c44-e5a4-42d6-bb56-9bdcf7f9e6f1">PEER_RECORD</a> must be populated.

<ul>
<li><b>dwSize</b></li>
<li><b>type</b></li>
<li><b>ftExpiration</b></li>
</ul>
<b>ftExpiration</b>   must be expressed as peer time (see <a href="https://msdn.microsoft.com/8d64c66a-96c3-48c4-82fa-c57554074729">PeerGroupUniversalTimeToPeerTime</a>).

The following members  are ignored and overwritten if populated.

<ul>
<li><b>id</b></li>
<li><b>pwzCreatorId</b></li>
<li><b>pwzLastModifiedById</b></li>
<li><b>ftCreation</b></li>
<li><b>ftLastModified</b></li>
<li><b>securityData</b></li>
</ul>
The remaining fields are optional. 


### -param pRecordId [out]

Pointer to a GUID that identifies the  record. This parameter is required.


## -returns



Returns S_OK if the function succeeds. Otherwise, the function returns one of the following values.

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
The peer group is not in a state where records can be added. For example, <a href="https://msdn.microsoft.com/a7f5689d-4849-4363-bc61-3fed63f4287b">PeerGroupJoin</a>  is called, but synchronization with the peer group database has not completed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PEER_E_INVALID_ATTRIBUTES</b></dt>
</dl>
</td>
<td width="60%">
The XML string that contains the record attributes in the <b>pwzAttributes</b>  member of the <a href="https://msdn.microsoft.com/4e0a1c44-e5a4-42d6-bb56-9bdcf7f9e6f1">PEER_RECORD</a> structure does not comply with the <a href="https://msdn.microsoft.com/2991af9b-da32-4915-b4d6-575e3faac04e">schema specification</a>.

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
<dt><b>PEER_E_INVALID_PEER_NAME</b></dt>
</dl>
</td>
<td width="60%">
The supplied peer name is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PEER_E_INVALID_RECORD</b></dt>
</dl>
</td>
<td width="60%">
One or more fields in <a href="https://msdn.microsoft.com/4e0a1c44-e5a4-42d6-bb56-9bdcf7f9e6f1">PEER_RECORD</a> are invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PEER_E_MAX_RECORD_SIZE_EXCEEDED</b></dt>
</dl>
</td>
<td width="60%">
The record has exceeded the maximum size allowed by the peer group properties.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PEER_E_NOT_AUTHORIZED</b></dt>
</dl>
</td>
<td width="60%">
The identity is not authorized to publish a record of that type.

</td>
</tr>
</table>
 

Cryptography-specific errors can be returned from the <a href="https://msdn.microsoft.com/c36025c5-a407-4a05-8780-23f8107730df">Microsoft RSA Base Provider</a>. These errors are prefixed with CRYPT_* and defined in Winerror.h.




## -see-also




<a href="https://msdn.microsoft.com/4e0a1c44-e5a4-42d6-bb56-9bdcf7f9e6f1"> PEER_RECORD</a>



<a href="https://msdn.microsoft.com/e80fbf7f-2193-4a45-8a7f-46707ae4acfe">PeerGroupDeleteRecord</a>



<a href="https://msdn.microsoft.com/d9a0654a-850a-40bb-9112-03ec9bf47370">PeerGroupEnumRecords</a>



<a href="https://msdn.microsoft.com/bfff0422-452c-4780-8df7-d3e8d5ad385c">PeerGroupUpdateRecord</a>
 

 

