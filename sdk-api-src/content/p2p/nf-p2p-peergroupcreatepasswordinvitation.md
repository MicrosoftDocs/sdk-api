---
UID: NF:p2p.PeerGroupCreatePasswordInvitation
title: PeerGroupCreatePasswordInvitation function
author: windows-sdk-content
description: Returns an XML string that can be used by the specified peer to join a group with a matching password.
old-location: p2p\peergroupcreatepasswordinvitation.htm
old-project: p2psdk
ms.assetid: 12d2920d-35b6-41e3-9129-1f11ce4cb5eb
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: PeerGroupCreatePasswordInvitation, PeerGroupCreatePasswordInvitation function [Peer Networking], p2p.peergroupcreatepasswordinvitation, p2p/PeerGroupCreatePasswordInvitation
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: p2p.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: PEER_WATCH_PERMISSION
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - P2P.dll
api_name:
 - PeerGroupCreatePasswordInvitation
product: Windows
targetos: Windows
req.lib: P2P.lib
req.dll: P2P.dll
req.irql: 
req.product: ADAM
---

# PeerGroupCreatePasswordInvitation function


## -description


The <b>PeerGroupCreatePasswordInvitation</b> function returns an XML string that can be used by the specified peer to join a group with a matching password. 


## -parameters




### -param hGroup [in]

Handle to the peer group for which this invitation is issued. This handle is returned by the <a href="https://msdn.microsoft.com/b85d87c6-28b7-49f8-865c-9d246f89367e">PeerGroupCreate</a>, <a href="https://msdn.microsoft.com/cfaf244f-8786-4801-926d-f6c79bfa4275">PeerGroupOpen</a>, or <a href="https://msdn.microsoft.com/a7f5689d-4849-4363-bc61-3fed63f4287b">PeerGroupJoin</a> function. This parameter is required.


### -param ppwzInvitation [out]

Pointer to a Unicode string that contains the invitation from the issuer. This invitation can be passed to <a href="https://msdn.microsoft.com/aff8a462-a4cf-462b-a641-b1573311037b">PeerGroupPasswordJoin</a> by the recipient in order to join the specified peer group. To return the details of the invitation as a <a href="https://msdn.microsoft.com/215df4ed-83e3-40c3-a38e-89d92ce38707">PEER_INVITATION_INFO</a> structure, pass this string to <a href="https://msdn.microsoft.com/ddc1c419-7be3-4115-af21-1108921c7b1d">PeerGroupParseInvitation</a>. To release this data, pass this pointer to <a href="https://msdn.microsoft.com/54288829-c991-42d6-a7c4-874ed28dd106">PeerFreeData</a>.

This function requires that the following fields are set on the <a href="https://msdn.microsoft.com/a1501343-bd84-4dbe-91d0-c64c59e34abc">PEER_GROUP_PROPERTIES</a> structure passed to <a href="https://msdn.microsoft.com/b85d87c6-28b7-49f8-865c-9d246f89367e">PeerGroupCreate</a>.<ul>
<li><b>pwzGroupPassword</b>. This field must contain the password used to validate peers joining the peer group.</li>
<li><b>groupPasswordRole</b>. This field must containing the GUID of the role (administrator or peer) for which the password is required.</li>
<li><b>dwAuthenticationSchemes</b>. This field must have the <b>PEER_GROUP_PASSWORD_AUTHENTICATION</b> flag (0x00000001) set on it.</li>
</ul>



## -returns



Returns S_OK if the operation succeeds; otherwise, the function returns one of the following values.

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
The peer  group is not in a state where records can be added. For example, <a href="https://msdn.microsoft.com/a7f5689d-4849-4363-bc61-3fed63f4287b">PeerGroupJoin</a>  is called, but synchronization with the group database has not completed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PEER_E_CHAIN_TOO_LONG</b></dt>
</dl>
</td>
<td width="60%">
The GMC chain is longer than 24 administrators or members. For more information about GMC chains, please refer to the <a href="https://msdn.microsoft.com/3966d4eb-4504-4b1e-9c9f-6eab7751d7ed">How Group Security Works</a> documentation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PEER_E_IDENTITY_DELETED</b></dt>
</dl>
</td>
<td width="60%">
The data passed as <i>pwzIdentityInfo</i> is for a deleted identity and no longer valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PEER_E_NOT_AUTHORIZED</b></dt>
</dl>
</td>
<td width="60%">
The peer that called this method is not an administrator.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PEER_E_NO_KEY_ACCESS</b></dt>
</dl>
</td>
<td width="60%">
Access to the identity or peer group keys is denied. Typically, this is caused by an incorrect access control list (ACL) for the folder that contains the user or computer keys. This can happen when the ACL is  reset manually. 


</td>
</tr>
</table>
 

Cryptography-specific errors may be returned from the <a href="https://msdn.microsoft.com/c36025c5-a407-4a05-8780-23f8107730df">Microsoft RSA Base Provider</a>. These errors are prefixed with CRYPT_* and defined in Winerror.h.



