---
UID: NF:p2p.PeerGroupSetProperties
title: PeerGroupSetProperties function
author: windows-sdk-content
description: The PeerGroupSetProperties function sets the current peer group properties. In version 1.0 of this API, only the creator of the peer group can perform this operation.
old-location: p2p\peergroupsetproperties.htm
tech.root: p2psdk
ms.assetid: 20acf963-de8f-4bcd-a9d6-a513d516b108
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: PeerGroupSetProperties, PeerGroupSetProperties function [Peer Networking], p2p.peergroupsetproperties, p2p/PeerGroupSetProperties
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
 - PeerGroupSetProperties
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PeerGroupSetProperties function


## -description


The <b>PeerGroupSetProperties</b> function sets the current peer group properties. In version 1.0 of this API,  only the creator of the peer group can perform this operation.


## -parameters




### -param hGroup [in]

Handle to the peer group whose properties are set by a peer. This handle is returned by the  <a href="https://msdn.microsoft.com/b85d87c6-28b7-49f8-865c-9d246f89367e">PeerGroupCreate</a>, <a href="https://msdn.microsoft.com/cfaf244f-8786-4801-926d-f6c79bfa4275">PeerGroupOpen</a>, or <a href="https://msdn.microsoft.com/a7f5689d-4849-4363-bc61-3fed63f4287b">PeerGroupJoin</a> function. This parameter is required.


### -param pProperties [in]

Pointer to a peer-populated <a href="https://msdn.microsoft.com/a1501343-bd84-4dbe-91d0-c64c59e34abc">PEER_GROUP_PROPERTIES</a> 
	   structure that contains the new properties. To obtain this structure, a peer must first call <a href="https://msdn.microsoft.com/6273817f-9698-4c0b-93a9-9bbee2e5dc78">PeerGroupGetProperties</a>, change the appropriate fields, and then pass it as this parameter. This parameter is required.

The following members of <a href="https://msdn.microsoft.com/a1501343-bd84-4dbe-91d0-c64c59e34abc">PEER_GROUP_PROPERTIES</a> cannot be changed:<ul>
<li><b>dwSize</b></li>
<li><b>pwzCloud</b></li>
<li><b>pwzClassifier</b></li>
<li><b>pwzGroupPeerName</b></li>
<li><b>pwzCreatorPeerName</b></li>
</ul>



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
<dt><b>PEER_E_GROUP_NOT_READY</b></dt>
</dl>
</td>
<td width="60%">
The group is not in a state where peer group properties can be set. For example, <a href="https://msdn.microsoft.com/a7f5689d-4849-4363-bc61-3fed63f4287b">PeerGroupJoin</a> has been called, but synchronization with the peer group database is not complete.

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
<dt><b>PEER_E_INVALID_GROUP_PROPERTIES</b></dt>
</dl>
</td>
<td width="60%">
One or more of the specified properties is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PEER_E_NOT_AUTHORIZED</b></dt>
</dl>
</td>
<td width="60%">
The current identity does not have the authorization to change these properties. In this case, the identity is not the  creator of the peer group.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PEER_E_PASSWORD_DOES_NOT_MEET_POLICY</b></dt>
</dl>
</td>
<td width="60%">
  Password specified does not meet system password requirements.

</td>
</tr>
</table>
 

Cryptography-specific errors can be returned from the <a href="https://msdn.microsoft.com/c36025c5-a407-4a05-8780-23f8107730df">Microsoft RSA Base Provider</a>. These errors are prefixed with CRYPT_* and defined in Winerror.h.




## -remarks



For applications that utilize passwords, it is recommended the passwords are handled securely  by calling the <a href="https://msdn.microsoft.com/6b372552-87d4-4047-afa5-0d1113348289">CryptoProtectMemory</a> and <a href="https://msdn.microsoft.com/2c4090a6-025b-4b7b-8f31-7e744ad51b39">SecureZeroMemory</a> functions.




## -see-also




<a href="https://msdn.microsoft.com/a1501343-bd84-4dbe-91d0-c64c59e34abc">PEER_GROUP_PROPERTIES</a>



<a href="https://msdn.microsoft.com/b85d87c6-28b7-49f8-865c-9d246f89367e">PeerGroupCreate</a>



<a href="https://msdn.microsoft.com/6273817f-9698-4c0b-93a9-9bbee2e5dc78">PeerGroupGetProperties</a>



<a href="https://msdn.microsoft.com/a7f5689d-4849-4363-bc61-3fed63f4287b">PeerGroupJoin</a>



<a href="https://msdn.microsoft.com/cfaf244f-8786-4801-926d-f6c79bfa4275">PeerGroupOpen</a>
 

 

