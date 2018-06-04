---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# peer_credential_info_tag structure


## -description


The <b>PEER_CREDENTIAL_INFO</b> structure defines information used to obtain and issue a peer's security credentials.


## -struct-fields




### -field dwSize

Specifies the size of this structure, in bytes.


### -field dwFlags

Reserved. This field must be set to 0.


### -field pwzFriendlyName

Pointer to a Unicode string that specifies the friendly (display) name of the issuer.


### -field pPublicKey

Pointer to a <b>CERT_PUBLIC_KEY_INFO</b> structure that contains the peer group member's public key and the encryption type it uses.


### -field pwzIssuerPeerName

Pointer to a Unicode string that specifies the membership issuer's PNRP name.


### -field pwzIssuerFriendlyName

Pointer to a Unicode string that specifies the friendly (display) name of the issuer.


### -field ftValidityStart

Specifies the <a href="https://msdn.microsoft.com/2d72b1bc-4687-4672-9644-85ad9b197a72">FILETIME</a> structure that contains the time when the recipient's membership in the peer group becomes valid. When issuing new credentials this value must be greater than the ValidityStart value for the member's current credentials. 


### -field ftValidityEnd

Specifies the <a href="https://msdn.microsoft.com/2d72b1bc-4687-4672-9644-85ad9b197a72">FILETIME</a> structure that contains the time when the recipient's membership in the peer group becomes invalid.


### -field cRoles

Specifies the number of role GUIDs present in <b>pRoles</b>.


### -field pRoles

Pointer to a list of GUIDs that specifies the combined set of available roles. The available roles are as follows.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="PEER_GROUP_ROLE_ADMIN"></a><a id="peer_group_role_admin"></a><dl>
<dt><b>PEER_GROUP_ROLE_ADMIN</b></dt>
</dl>
</td>
<td width="60%">
This role can issue invitations, issue credentials,   and renew the GMC of other administrators, as well as behave as a member of the peer group.

</td>
</tr>
<tr>
<td width="40%"><a id="PEER_GROUP_ROLE_MEMBER"></a><a id="peer_group_role_member"></a><dl>
<dt><b>PEER_GROUP_ROLE_MEMBER</b></dt>
</dl>
</td>
<td width="60%">
The role can add records to the peer group database.

</td>
</tr>
</table>
 


## -see-also




<a href="https://msdn.microsoft.com/b8bd0e17-6af7-426d-ba38-11ff4948cf67">PEER_MEMBER</a>



<a href="https://msdn.microsoft.com/81284e61-fc31-47c3-a296-c9c02a2889ec">PeerGroupIssueCredentials</a>
 

 

