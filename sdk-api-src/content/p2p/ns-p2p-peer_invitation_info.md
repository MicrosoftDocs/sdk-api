---
UID: NS:p2p.peer_invitation_info_tag
title: PEER_INVITATION_INFO (p2p.h)
description: The PEER_INVITATION_INFO structure defines information about an invitation to join a peer group.
helpviewer_keywords: ["*PPEER_INVITATION_INFO","PEER_GROUP_ROLE_ADMIN","PEER_GROUP_ROLE_MEMBER","PEER_INVITATION_INFO","PEER_INVITATION_INFO structure [Peer Networking]","PNRP_CLOUD_NAME_LOCAL","PNRP_CLOUD_NO_FLAGS","PNRP_GLOBAL_SCOPE","PNRP_LINK_LOCAL_SCOPE","PNRP_LOCAL_SCOPE","PPEER_INVITATION_INFO","PPEER_INVITATION_INFO structure pointer [Peer Networking]","p2p.peer_invitation_info","p2p/PPEER_INVITATION_INFO","p2p/peer_invitation_info_tag"]
old-location: p2p\peer_invitation_info.htm
tech.root: p2p
ms.assetid: 215df4ed-83e3-40c3-a38e-89d92ce38707
ms.date: 12/05/2018
ms.keywords: '*PPEER_INVITATION_INFO, PEER_GROUP_ROLE_ADMIN, PEER_GROUP_ROLE_MEMBER, PEER_INVITATION_INFO, PEER_INVITATION_INFO structure [Peer Networking], PNRP_CLOUD_NAME_LOCAL, PNRP_CLOUD_NO_FLAGS, PNRP_GLOBAL_SCOPE, PNRP_LINK_LOCAL_SCOPE, PNRP_LOCAL_SCOPE, PPEER_INVITATION_INFO, PPEER_INVITATION_INFO structure pointer [Peer Networking], p2p.peer_invitation_info, p2p/PPEER_INVITATION_INFO, p2p/peer_invitation_info_tag'
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
req.typenames: PEER_INVITATION_INFO, *PPEER_INVITATION_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - peer_invitation_info_tag
 - p2p/peer_invitation_info_tag
 - PPEER_INVITATION_INFO
 - p2p/PPEER_INVITATION_INFO
 - PEER_INVITATION_INFO
 - p2p/PEER_INVITATION_INFO
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
 - PEER_INVITATION_INFO
---

# PEER_INVITATION_INFO structure


## -description

The <b>PEER_INVITATION_INFO</b> structure defines information about an invitation to join a peer group. Invitations are represented as Unicode strings. To obtain this structure, pass the XML invitation string  created by <a href="/windows/desktop/api/p2p/nf-p2p-peergroupcreateinvitation">PeerGroupCreateInvitation</a> to <a href="/windows/desktop/api/p2p/nf-p2p-peergroupparseinvitation">PeerGroupParseInvitation</a>.

## -struct-fields

### -field dwSize

Specifies the size of this structure, in bytes.

### -field dwFlags

Must be set to 0x00000000.

### -field pwzCloudName

Pointer to a Unicode string that specifies the PNRP cloud name.

### -field dwScope

Specifies the scope under which the peer group was registered.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="PNRP_GLOBAL_SCOPE"></a><a id="pnrp_global_scope"></a><dl>
<dt><b>PNRP_GLOBAL_SCOPE</b></dt>
</dl>
</td>
<td width="60%">
Global scope, including the Internet.

</td>
</tr>
<tr>
<td width="40%"><a id="PNRP_LOCAL_SCOPE"></a><a id="pnrp_local_scope"></a><dl>
<dt><b>PNRP_LOCAL_SCOPE</b></dt>
</dl>
</td>
<td width="60%">
Local scope.

</td>
</tr>
<tr>
<td width="40%"><a id="PNRP_LINK_LOCAL_SCOPE"></a><a id="pnrp_link_local_scope"></a><dl>
<dt><b>PNRP_LINK_LOCAL_SCOPE</b></dt>
</dl>
</td>
<td width="60%">
Link-local scope.

</td>
</tr>
</table>

### -field dwCloudFlags

Specifies a set of flags that describe PNRP cloud features.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="PNRP_CLOUD_NO_FLAGS"></a><a id="pnrp_cloud_no_flags"></a><dl>
<dt><b>PNRP_CLOUD_NO_FLAGS</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
No flags are set.

</td>
</tr>
<tr>
<td width="40%"><a id="PNRP_CLOUD_NAME_LOCAL"></a><a id="pnrp_cloud_name_local"></a><dl>
<dt><b>PNRP_CLOUD_NAME_LOCAL</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
The cloud name is not available on other computers; it is locally defined.

</td>
</tr>
</table>

### -field pwzGroupPeerName

Pointer to a Unicode string that specifies the peer name of the peer group.

### -field pwzIssuerPeerName

Pointer to a Unicode string that specifies the PNRP name of the peer issuing the invitation.

### -field pwzSubjectPeerName

Pointer to a Unicode string that specifies the PNRP name of the peer that receives the invitation.

### -field pwzGroupFriendlyName

Pointer to a Unicode string that specifies the friendly (display) name of the peer group.

### -field pwzIssuerFriendlyName

Pointer to a Unicode string that specifies the friendly (display) name of the peer issuing the invitation.

### -field pwzSubjectFriendlyName

Pointer to a Unicode string that specifies the friendly (display) name of the peer that receives the invitation.

### -field ftValidityStart

Specifies a UTC <b>FILETIME</b> value that indicates when the invitation  becomes valid.

### -field ftValidityEnd

Specifies a UTC <b>FILETIME</b> value that indicates when the invitation becomes invalid.

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
This role can issue invitations, renew memberships, modify peer group properties, publish and update records, and renew the GMC of other administrators.

</td>
</tr>
<tr>
<td width="40%"><a id="PEER_GROUP_ROLE_MEMBER"></a><a id="peer_group_role_member"></a><dl>
<dt><b>PEER_GROUP_ROLE_MEMBER</b></dt>
</dl>
</td>
<td width="60%">
The role can publish records to the peer group database.

</td>
</tr>
</table>

### -field cClassifiers

Unsigned integer value that contains the number of string values listed in <b>ppwzClassifiers</b>. This field is reserved for future use.

### -field ppwzClassifiers

List of pointers to Unicode strings. This field is reserved for future use.

### -field pSubjectPublicKey

Pointer to a <b>CERT_PUBLIC_KEY_INFO</b> structure that contains the recipient's returned public key and the encryption algorithm type it uses.

### -field authScheme

<b>Windows Vista or later.</b>           The <a href="/windows/desktop/api/p2p/ne-p2p-peer_group_authentication_scheme">PEER_GROUP_AUTHENTICATION_SCHEME</a> enumeration value that indicates the type of authentication used to validate the peer group invitee.

## -see-also

<a href="/windows/desktop/api/p2p/nf-p2p-peergroupparseinvitation">PeerGroupParseInvitation</a>