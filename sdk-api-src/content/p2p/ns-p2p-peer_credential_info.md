---
UID: NS:p2p.peer_credential_info_tag
title: PEER_CREDENTIAL_INFO (p2p.h)
description: The PEER_CREDENTIAL_INFO structure defines information used to obtain and issue a peer's security credentials.
helpviewer_keywords: ["*PPEER_CREDENTIAL_INFO","PEER_CREDENTIAL_INFO","PEER_CREDENTIAL_INFO structure [Peer Networking]","PEER_GROUP_ROLE_ADMIN","PEER_GROUP_ROLE_MEMBER","PPEER_CREDENTIAL_INFO","PPEER_CREDENTIAL_INFO structure pointer [Peer Networking]","p2p.peer_credential_info","p2p/PEER_CREDENTIAL_INFO","p2p/PPEER_CREDENTIAL_INFO"]
old-location: p2p\peer_credential_info.htm
tech.root: p2p
ms.assetid: c47bb38d-eafd-4218-8ac7-1c54ed6948ee
ms.date: 12/05/2018
ms.keywords: '*PPEER_CREDENTIAL_INFO, PEER_CREDENTIAL_INFO, PEER_CREDENTIAL_INFO structure [Peer Networking], PEER_GROUP_ROLE_ADMIN, PEER_GROUP_ROLE_MEMBER, PPEER_CREDENTIAL_INFO, PPEER_CREDENTIAL_INFO structure pointer [Peer Networking], p2p.peer_credential_info, p2p/PEER_CREDENTIAL_INFO, p2p/PPEER_CREDENTIAL_INFO'
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: PEER_CREDENTIAL_INFO, *PPEER_CREDENTIAL_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - peer_credential_info_tag
 - p2p/peer_credential_info_tag
 - PPEER_CREDENTIAL_INFO
 - p2p/PPEER_CREDENTIAL_INFO
 - PEER_CREDENTIAL_INFO
 - p2p/PEER_CREDENTIAL_INFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - P2P.h
api_name:
 - PEER_CREDENTIAL_INFO
---

# PEER_CREDENTIAL_INFO structure


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

Specifies the <a href="/windows/desktop/P2PSdk/graphing-reference-links">FILETIME</a> structure that contains the time when the recipient's membership in the peer group becomes valid. When issuing new credentials this value must be greater than the ValidityStart value for the member's current credentials.

### -field ftValidityEnd

Specifies the <a href="/windows/desktop/P2PSdk/graphing-reference-links">FILETIME</a> structure that contains the time when the recipient's membership in the peer group becomes invalid.

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

<a href="/windows/desktop/api/p2p/ns-p2p-peer_member">PEER_MEMBER</a>



<a href="/windows/desktop/api/p2p/nf-p2p-peergroupissuecredentials">PeerGroupIssueCredentials</a>