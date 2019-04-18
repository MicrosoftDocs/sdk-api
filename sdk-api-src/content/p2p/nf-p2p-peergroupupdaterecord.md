---
UID: NF:p2p.PeerGroupUpdateRecord
title: PeerGroupUpdateRecord function (p2p.h)
author: windows-sdk-content
description: The PeerGroupUpdateRecord function updates a record within a specific peer group.
old-location: p2p\peergroupupdaterecord.htm
tech.root: P2PSdk
ms.assetid: bfff0422-452c-4780-8df7-d3e8d5ad385c
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: PeerGroupUpdateRecord, PeerGroupUpdateRecord function [Peer Networking], p2p.peergroupupdaterecord, p2p/PeerGroupUpdateRecord
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
 - PeerGroupUpdateRecord
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# PeerGroupUpdateRecord function


## -description


The <b>PeerGroupUpdateRecord</b> function updates a record within a specific peer group.


## -parameters




### -param hGroup [in]

Handle to the peer group whose record is updated. This handle is returned by the <a href="https://msdn.microsoft.com/b85d87c6-28b7-49f8-865c-9d246f89367e">PeerGroupCreate</a>, <a href="https://msdn.microsoft.com/cfaf244f-8786-4801-926d-f6c79bfa4275">PeerGroupOpen</a>, or <a href="https://msdn.microsoft.com/a7f5689d-4849-4363-bc61-3fed63f4287b">PeerGroupJoin</a> function. This parameter is required.


### -param pRecord [in]

Pointer to a <a href="https://msdn.microsoft.com/4e0a1c44-e5a4-42d6-bb56-9bdcf7f9e6f1">PEER_RECORD</a> structure that contains the updated record for <i>hGroup</i>.  This parameter is required.

The following members in <a href="https://msdn.microsoft.com/4e0a1c44-e5a4-42d6-bb56-9bdcf7f9e6f1">PEER_RECORD</a> can be updated.

<ul>
<li><b>pwzAttributes</b></li>
<li><b>ftExpiration</b></li>
<li><b>data</b></li>
</ul>
The following members in <a href="https://msdn.microsoft.com/4e0a1c44-e5a4-42d6-bb56-9bdcf7f9e6f1">PEER_RECORD</a> must be present, but cannot be changed.

<ul>
<li><b>dwSize</b></li>
<li><b>id</b></li>
<li><b>type</b></li>
<li><b>dwFlags</b></li>
</ul>
The following members are ignored if populated.

<ul>
<li><b>dwVersion</b></li>
<li><b>pwzCreatorId</b></li>
<li><b>pwzModifiedById</b></li>
<li><b>ftCreation</b></li>
<li><b>ftLastModified</b></li>
<li><b>securityData</b></li>
</ul>
The members that remain are optional.


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
One of the specified parameters is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PEER_E_GROUP_NOT_READY</b></dt>
</dl>
</td>
<td width="60%">
The peer group is not in a state where a record can be updated, for example, <a href="https://msdn.microsoft.com/a7f5689d-4849-4363-bc61-3fed63f4287b">PeerGroupJoin</a> has been called, but synchronization with the peer group database is not complete.

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
The current peer identity does not have the authorization to delete the record. In this case, the peer identity is not the  creator of the record.

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
 

Cryptography-specific errors can be returned from the <a href="https://msdn.microsoft.com/c36025c5-a407-4a05-8780-23f8107730df">Microsoft RSA Base Provider</a>. These errors are prefixed with CRYPT_* and defined in Winerror.h.




## -see-also




<a href="https://msdn.microsoft.com/4e0a1c44-e5a4-42d6-bb56-9bdcf7f9e6f1"> PEER_RECORD</a>



<a href="https://msdn.microsoft.com/d9ca87bc-30da-4a19-b34a-8d8388ccd19a">PeerGroupAddRecord</a>



<a href="https://msdn.microsoft.com/b85d87c6-28b7-49f8-865c-9d246f89367e">PeerGroupCreate</a>



<a href="https://msdn.microsoft.com/e80fbf7f-2193-4a45-8a7f-46707ae4acfe">PeerGroupDeleteRecord</a>



<a href="https://msdn.microsoft.com/a7f5689d-4849-4363-bc61-3fed63f4287b">PeerGroupJoin</a>



<a href="https://msdn.microsoft.com/cfaf244f-8786-4801-926d-f6c79bfa4275">PeerGroupOpen</a>
 

 

