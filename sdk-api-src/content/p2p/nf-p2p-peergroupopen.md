---
UID: NF:p2p.PeerGroupOpen
title: PeerGroupOpen function
author: windows-driver-content
description: The PeerGroupOpen function opens a peer group that a peer has created or joined. After a peer group is opened, the peer can register for event notifications.
old-location: p2p\peergroupopen.htm
old-project: P2PSdk
ms.assetid: cfaf244f-8786-4801-926d-f6c79bfa4275
ms.author: windowsdriverdev
ms.date: 4/23/2018
ms.keywords: PeerGroupOpen, PeerGroupOpen function [Peer Networking], p2p.peergroupopen, p2p/PeerGroupOpen
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
-	PeerGroupOpen
product: Windows
targetos: Windows
req.lib: P2P.lib
req.dll: P2P.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# PeerGroupOpen function


## -description



      The <b>PeerGroupOpen</b> function opens a peer group that a peer has created or joined. After a peer group is opened, the peer  can register for event notifications.


## -parameters




### -param pwzIdentity [in]

Pointer to a Unicode string that contains the identity  a peer  uses to open a group.  This parameter is required.


### -param pwzGroupPeerName [in]

Pointer to a Unicode string that contains the peer name of the peer group. This parameter is required.


### -param pwzCloud [in]

Pointer to a Unicode string that contains the name of the PNRP cloud in which the peer group is located. If the value is <b>NULL</b>,  the cloud specified in the peer group properties is used.


### -param phGroup [out]

Pointer to a handle for a  peer group. If this value is <b>NULL</b>, the open operation is unsuccessful. This parameter is required.


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
<dt><b>PEER_E_CLOUD_NAME_AMBIGUOUS</b></dt>
</dl>
</td>
<td width="60%">
The cloud specified in <i>pwzCloud</i>  cannot be uniquely discovered,  for example, more than one cloud matches the provided name.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PEER_E_NO_CLOUD</b></dt>
</dl>
</td>
<td width="60%">
The cloud specified in <i>pwzCloud</i>  cannot be located.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PEER_E_NO_KEY_ACCESS</b></dt>
</dl>
</td>
<td width="60%">
Access to the peer identity or peer group keys is denied. Typically, this is  caused by an incorrect access control list (ACL) for the folder that contains the user or computer keys. This can happen when the ACL has been  reset manually. 


</td>
</tr>
</table>
 

Cryptography-specific errors can be returned from the <a href="https://msdn.microsoft.com/c36025c5-a407-4a05-8780-23f8107730df">Microsoft RSA Base Provider</a>. These errors are prefixed with CRYPT_* and defined in Winerror.h.




## -remarks



Multiple applications can open the same group simultaneously. Any application can choose to open a group without subsequently calling <a href="https://msdn.microsoft.com/240bcba7-29f9-4043-8203-e71175bee69a">PeerGroupConnect</a>. These applications are considered to be offline. However, a second application can open and connect the peer to the group, which means that an application must be ready to connect at any time.




## -see-also




<a href="https://msdn.microsoft.com/4438e6c1-8c25-4656-bac5-dda43421ee43">PeerGroupClose</a>



<a href="https://msdn.microsoft.com/240bcba7-29f9-4043-8203-e71175bee69a">PeerGroupConnect</a>



<a href="https://msdn.microsoft.com/b85d87c6-28b7-49f8-865c-9d246f89367e">PeerGroupCreate</a>



<a href="https://msdn.microsoft.com/a7f5689d-4849-4363-bc61-3fed63f4287b">PeerGroupJoin</a>
 

 

