---
UID: NF:p2p.PeerGroupCreate
title: PeerGroupCreate function (p2p.h)
description: The PeerGroupCreate function creates a new peer group.
helpviewer_keywords: ["PeerGroupCreate","PeerGroupCreate function [Peer Networking]","p2p.peergroupcreate","p2p/PeerGroupCreate"]
old-location: p2p\peergroupcreate.htm
tech.root: p2p
ms.assetid: b85d87c6-28b7-49f8-865c-9d246f89367e
ms.date: 12/05/2018
ms.keywords: PeerGroupCreate, PeerGroupCreate function [Peer Networking], p2p.peergroupcreate, p2p/PeerGroupCreate
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
 - PeerGroupCreate
 - p2p/PeerGroupCreate
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
 - PeerGroupCreate
---

# PeerGroupCreate function


## -description

The <b>PeerGroupCreate</b> function creates a new peer group.

## -parameters

### -param pProperties [in]

Pointer to a <a href="/windows/desktop/api/p2p/ns-p2p-peer_group_properties">PEER_GROUP_PROPERTIES</a> structure that specifies the specific details of the group, such as the peer group names, invitation lifetimes, and presence lifetimes. This parameter is required.

The following members must be set:<ul>
<li><b>pwzCreatorPeerName</b></li>
</ul>


The following members cannot be set:<ul>
<li><b>pwzGroupPeerName</b></li>
</ul>The remaining members are optional.

### -param phGroup [out]

Returns the  handle pointer to the  peer group. Any function called with this handle as a parameter  has the corresponding action performed on that peer group.  This parameter is required.

## -returns

Returns S_OK if the operation succeeds. Otherwise, the function returns one of the following values.

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
<dt><b>PEER_E_CLOUD_NAME_AMBIGUOUS</b></dt>
</dl>
</td>
<td width="60%">
The cloud specified in <i>pProperties</i>  cannot be uniquely discovered (more than one cloud matches the provided name).

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PEER_E_INVALID_CLASSIFIER</b></dt>
</dl>
</td>
<td width="60%">
The peer group classifier specified in <i>pProperties</i> is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PEER_E_INVALID_PEER_NAME</b></dt>
</dl>
</td>
<td width="60%">
The peer name specified for the group in <i>pProperties</i> is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PEER_E_INVALID_PROPERTIES</b></dt>
</dl>
</td>
<td width="60%">
One or more of the peer group properties supplied in <i>pProperties</i> is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PEER_E_NO_CLOUD</b></dt>
</dl>
</td>
<td width="60%">
The cloud specified in <i>pProperties</i>  cannot be located.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PEER_E_NO_KEY_ACCESS</b></dt>
</dl>
</td>
<td width="60%">
Access to the identity or group keys is denied. Typically, this is  caused by an incorrect access control list (ACL) for the folder that contains the user or computer keys. This can happen when the ACL is  reset manually. 


</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b> PEER_E_PASSWORD_DOES_NOT_MEET_POLICY</b></dt>
</dl>
</td>
<td width="60%">
Password specified does not meet system password requirements.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_DELETE_PENDING</b></dt>
</dl>
</td>
<td width="60%">
The peer identity specified as the Group Creator has been deleted or is in the process of being deleted.

</td>
</tr>
</table>
 

Cryptography-specific errors can be returned from the <a href="/windows/desktop/SecCrypto/microsoft-base-cryptographic-provider">Microsoft RSA Base Provider</a>. These errors are prefixed with CRYPT_* and defined in Winerror.h.

## -remarks

<a href="/windows/desktop/api/p2p/nf-p2p-peergroupconnect">PeerGroupConnect</a> must be called by the group creator immediately after creation. If this does not take place, users given an invitation will call PeerGroupConnect successfully but they will not be able to listen and will eventually receive the connection failed event. 

An application  obtains an identity by calling <a href="/windows/desktop/api/p2p/nf-p2p-peeridentitycreate">PeerIdentityCreate</a>, or any other method that returns an identity name string. This identity  serves as the owner of the group, and is the initial member of the peer group when created.

For applications that utilize passwords, it is recommended the passwords are handled securely  by calling the <a href="/windows/desktop/api/dpapi/nf-dpapi-cryptprotectmemory">CryptoProtectMemory</a> and <a href="/previous-versions/windows/desktop/legacy/aa366877(v=vs.85)">SecureZeroMemory</a> functions.

## -see-also

<a href="/windows/desktop/api/p2p/ns-p2p-peer_group_properties"> PEER_GROUP_PROPERTIES</a>



<a href="/windows/desktop/api/p2p/nf-p2p-peergroupclose">PeerGroupClose</a>



<a href="/windows/desktop/api/p2p/nf-p2p-peergroupconnect">PeerGroupConnect</a>



<a href="/windows/desktop/api/p2p/nf-p2p-peergroupopen">PeerGroupOpen</a>