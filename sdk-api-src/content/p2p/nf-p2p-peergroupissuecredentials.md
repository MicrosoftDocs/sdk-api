---
UID: NF:p2p.PeerGroupIssueCredentials
title: PeerGroupIssueCredentials function
author: windows-sdk-content
description: The PeerGroupIssueCredentials function issues credentials, including a GMC, to a specific identity, and optionally returns an invitation XML string the invited peer can use to join a peer group.
old-location: p2p\peergroupissuecredentials.htm
tech.root: P2PSdk
ms.assetid: 81284e61-fc31-47c3-a296-c9c02a2889ec
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: PEER_GROUP_STORE_CREDENTIALS, PeerGroupIssueCredentials, PeerGroupIssueCredentials function [Peer Networking], p2p.peergroupissuecredentials, p2p/PeerGroupIssueCredentials
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
 - PeerGroupIssueCredentials
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PeerGroupIssueCredentials function


## -description


The <b>PeerGroupIssueCredentials</b> function issues credentials, including a GMC,  to a specific identity, and optionally returns an invitation XML string the invited peer can use to join a peer group.


## -parameters




### -param hGroup [in]

Handle to a peer group  for which a peer will issue credentials to potential invited peers. This handle is returned by the <a href="https://msdn.microsoft.com/b85d87c6-28b7-49f8-865c-9d246f89367e">PeerGroupCreate</a>, <a href="https://msdn.microsoft.com/cfaf244f-8786-4801-926d-f6c79bfa4275">PeerGroupOpen</a>, or <a href="https://msdn.microsoft.com/a7f5689d-4849-4363-bc61-3fed63f4287b">PeerGroupJoin</a> function. This parameter is required.


### -param pwzSubjectIdentity [in]

Specifies the identity of a peer to whom credentials will be issued. This parameter is required.


### -param pCredentialInfo [in]


<a href="https://msdn.microsoft.com/c47bb38d-eafd-4218-8ac7-1c54ed6948ee">PEER_CREDENTIAL_INFO</a> structure that contains information about the credentials  of a peer whose identity is specified in <i>pwzSubjectIdentity</i>. If this parameter is <b>NULL</b>, the information stored in the peer database is used, instead. This parameter is optional.

If this parameter is provided, the following fields in <a href="https://msdn.microsoft.com/c47bb38d-eafd-4218-8ac7-1c54ed6948ee">PEER_CREDENTIAL_INFO</a> are ignored:<ul>
<li><b>pwzIssuerPeerName</b></li>
<li><b>pwzIssuerFriendlyName</b></li>
</ul>



### -param dwFlags [in]

Specifies a set of flags used to describe actions taken when credentials are issued. If this parameter is set to 0 (zero), the credentials are returned in <i>ppwzInvitation</i>. This parameter is optional.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="PEER_GROUP_STORE_CREDENTIALS"></a><a id="peer_group_store_credentials"></a><dl>
<dt><b>PEER_GROUP_STORE_CREDENTIALS</b></dt>
</dl>
</td>
<td width="60%">
Publish the subject identity's newly-created GMC in the group database.  The GMC is picked up automatically by the subject. If this flag is not set, the credentials must be obtained by a different application such as email.

</td>
</tr>
</table>
 


### -param ppwzInvitation [out]

Pointer to an invitation XML string returned by the function call. This invitation is passed out-of-band to the invited peer who uses it in a call to <a href="https://msdn.microsoft.com/a7f5689d-4849-4363-bc61-3fed63f4287b">PeerGroupJoin</a>. This parameter is optional.


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
<dt><b>PEER_E_IDENTITY_DELETED</b></dt>
</dl>
</td>
<td width="60%">
The identity creating the credentials has been deleted.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PEER_E_IDENTITY_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The identity cannot be found in the group database, and <i>pCredentialInfo</i> is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PEER_E_NO_KEY_ACCESS</b></dt>
</dl>
</td>
<td width="60%">
Access to the identity or group keys is denied. Typically, this is  caused by an incorrect access control list (ACL) for the folder that contains the user or computer keys. This can happen when the ACL has been  reset manually. 


</td>
</tr>
</table>
 

Cryptography-specific errors can be returned from the <a href="https://msdn.microsoft.com/c36025c5-a407-4a05-8780-23f8107730df">Microsoft RSA Base Provider</a>. These errors are prefixed with CRYPT_* and defined in Winerror.h.




## -remarks



This function can only be called successfully by an administrator.

The credentials for a member (<a href="https://msdn.microsoft.com/c47bb38d-eafd-4218-8ac7-1c54ed6948ee">PEER_CREDENTIAL_INFO</a>) are obtained  by calling <a href="https://msdn.microsoft.com/1201ce0b-961a-4848-9b9c-ad6491e3ff4a">PeerGroupEnumMembers</a>. The credentials are located in  the <b>pCredentialInfo</b> field of the <a href="https://msdn.microsoft.com/b8bd0e17-6af7-426d-ba38-11ff4948cf67">PEER_MEMBER</a> structure for a specific member.



