---
UID: NF:p2p.PeerGroupDeleteRecord
title: PeerGroupDeleteRecord function
author: windows-sdk-content
description: The PeerGroupDeleteRecord function deletes a record from a peer group. The creator, as well as any other member in an administrative role may delete a specific record.
old-location: p2p\peergroupdeleterecord.htm
old-project: P2PSdk
ms.assetid: e80fbf7f-2193-4a45-8a7f-46707ae4acfe
ms.author: windowssdkdev
ms.date: 05/08/2018
ms.keywords: PeerGroupDeleteRecord, PeerGroupDeleteRecord function [Peer Networking], p2p.peergroupdeleterecord, p2p/PeerGroupDeleteRecord
ms.prod: windows
ms.technology: windows-sdk
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
-	PeerGroupDeleteRecord
product: Windows
targetos: Windows
req.lib: P2P.lib
req.dll: P2P.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# PeerGroupDeleteRecord function


## -description



      The <b>PeerGroupDeleteRecord</b> function deletes a record from a peer group. The creator, as well as any other member in an administrative role may delete a specific record.


## -parameters




### -param hGroup [in]

Handle to the peer group that contains the record. This handle is returned by the <a href="https://msdn.microsoft.com/b85d87c6-28b7-49f8-865c-9d246f89367e">PeerGroupCreate</a>, <a href="https://msdn.microsoft.com/cfaf244f-8786-4801-926d-f6c79bfa4275">PeerGroupOpen</a>, or <a href="https://msdn.microsoft.com/a7f5689d-4849-4363-bc61-3fed63f4287b">PeerGroupJoin</a> function. This parameter is required.


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
The peer group is not in a state where records can be deleted. For example, <a href="https://msdn.microsoft.com/a7f5689d-4849-4363-bc61-3fed63f4287b">PeerGroupJoin</a>  is called, but synchronization with the peer group database has not completed.

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
 

Cryptography-specific errors can be returned from the <a href="https://msdn.microsoft.com/c36025c5-a407-4a05-8780-23f8107730df">Microsoft RSA Base Provider</a>. These errors are prefixed with CRYPT_* and defined in Winerror.h.




## -see-also




<a href="https://msdn.microsoft.com/d9ca87bc-30da-4a19-b34a-8d8388ccd19a">PeerGroupAddRecord</a>



<a href="https://msdn.microsoft.com/b85d87c6-28b7-49f8-865c-9d246f89367e">PeerGroupCreate</a>



<a href="https://msdn.microsoft.com/a7f5689d-4849-4363-bc61-3fed63f4287b">PeerGroupJoin</a>



<a href="https://msdn.microsoft.com/cfaf244f-8786-4801-926d-f6c79bfa4275">PeerGroupOpen</a>



<a href="https://msdn.microsoft.com/bfff0422-452c-4780-8df7-d3e8d5ad385c">PeerGroupUpdateRecord</a>
 

 

