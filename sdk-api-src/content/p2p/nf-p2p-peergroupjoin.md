---
UID: NF:p2p.PeerGroupJoin
title: PeerGroupJoin function (p2p.h)
author: windows-sdk-content
description: The PeerGroupJoin function prepares a peer with an invitation to join an existing peer group prior to calling PeerGroupConnect or PeerGroupConnectByAddress.
old-location: p2p\peergroupjoin.htm
tech.root: P2PSdk
ms.assetid: a7f5689d-4849-4363-bc61-3fed63f4287b
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: PeerGroupJoin, PeerGroupJoin function [Peer Networking], p2p.peergroupjoin, p2p/PeerGroupJoin
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
 - PeerGroupJoin
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PeerGroupJoin function


## -description


The <b>PeerGroupJoin</b> function prepares a peer with an invitation to join an existing peer group prior to calling <a href="https://msdn.microsoft.com/240bcba7-29f9-4043-8203-e71175bee69a">PeerGroupConnect</a> or <a href="https://msdn.microsoft.com/44885110-fcb1-402a-86c6-1229b087165b">PeerGroupConnectByAddress</a>.


## -parameters




### -param pwzIdentity [in]

Pointer to a Unicode string that contains the identity opening the specified peer group. If this parameter is <b>NULL</b>, the implementation uses the identity obtained from <a href="https://msdn.microsoft.com/195052a2-eaae-4b8c-bc13-0667ce50a967">PeerIdentityGetDefault</a>.



### -param pwzInvitation [in]

Pointer to a Unicode string that contains the XML invitation granted by another peer. An invitation is created when the inviting peer calls <a href="https://msdn.microsoft.com/1ae5c288-6e9b-452a-8994-7878d713cd6d">PeerGroupCreateInvitation</a> or <a href="https://msdn.microsoft.com/81284e61-fc31-47c3-a296-c9c02a2889ec">PeerGroupIssueCredentials</a>. Specific details regarding this invitation can be obtained as a <a href="https://msdn.microsoft.com/215df4ed-83e3-40c3-a38e-89d92ce38707">PEER_INVITATION_INFO</a> structure by calling <a href="https://msdn.microsoft.com/ddc1c419-7be3-4115-af21-1108921c7b1d">PeerGroupParseInvitation</a>. This parameter is required.


### -param pwzCloud [in]

Pointer to a Unicode string that contains the name of the PNRP cloud where a group is located.  The default value is <b>NULL</b>, which indicates that the cloud specified in the invitation must be used.


### -param phGroup [out]

Pointer to the handle of the peer group. To start communication with a group, call <a href="https://msdn.microsoft.com/240bcba7-29f9-4043-8203-e71175bee69a">PeerGroupConnect</a>. This parameter is required.


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
The cloud cannot be uniquely discovered, for example, more than one cloud matches the provided name.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PEER_E_INVALID_PEER_NAME</b></dt>
</dl>
</td>
<td width="60%">
The peer identity specified in <i>pwzIdentity</i> is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PEER_E_INVALID_TIME_PERIOD</b></dt>
</dl>
</td>
<td width="60%">
The validity period specified in the invitation is invalid.  Either the specified period has expired or the invitation is not yet valid (i.e. the specified ValidityStart date\time has not yet been reached).  One possible reason for the return of this error is that the system clock is incorrectly set on the machine joining the group, or on the machine that issued the invitation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PEER_E_INVITATION_NOT_TRUSTED</b></dt>
</dl>
</td>
<td width="60%">
The invitation is not trusted. This may be due to invitation alteration,  errors, or expiration.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PEER_E_NO_CLOUD</b></dt>
</dl>
</td>
<td width="60%">
The cloud cannot be located.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PEER_E_UNSUPPORTED_VERSION</b></dt>
</dl>
</td>
<td width="60%">
The invitation is not supported by the current version of the Peer Infrastructure.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PEER_E_NO_KEY_ACCESS</b></dt>
</dl>
</td>
<td width="60%">
Access to the peer identity or peer group keys is denied. Typically,  this is  caused by an incorrect access control list (ACL) for the folder that contains the user or computer keys. This can happen when the ACL has been  reset manually. 


</td>
</tr>
</table>
 

Cryptography-specific errors can be returned from the <a href="https://msdn.microsoft.com/c36025c5-a407-4a05-8780-23f8107730df">Microsoft RSA Base Provider</a>. These errors are prefixed with CRYPT_* and defined in Winerror.h.




## -see-also




<a href="https://msdn.microsoft.com/215df4ed-83e3-40c3-a38e-89d92ce38707">PEER_INVITATION_INFO</a>



<a href="https://msdn.microsoft.com/240bcba7-29f9-4043-8203-e71175bee69a">PeerGroupConnect</a>



<a href="https://msdn.microsoft.com/44885110-fcb1-402a-86c6-1229b087165b">PeerGroupConnectByAddress</a>



<a href="https://msdn.microsoft.com/1ae5c288-6e9b-452a-8994-7878d713cd6d">PeerGroupCreateInvitation</a>



<a href="https://msdn.microsoft.com/cfaf244f-8786-4801-926d-f6c79bfa4275">PeerGroupOpen</a>



<a href="https://msdn.microsoft.com/ddc1c419-7be3-4115-af21-1108921c7b1d">PeerGroupParseInvitation</a>
 

 

