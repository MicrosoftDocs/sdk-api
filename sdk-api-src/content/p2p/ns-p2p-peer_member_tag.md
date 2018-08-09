---
UID: NS:p2p.peer_member_tag
title: peer_member_tag
author: windows-sdk-content
description: The PEER_MEMBER structure contains information that describes a member of a peer group.
old-location: p2p\peer_member.htm
old-project: p2psdk
ms.assetid: b8bd0e17-6af7-426d-ba38-11ff4948cf67
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: "*PPEER_MEMBER, PEER_MEMBER, PEER_MEMBER structure [Peer Networking], PEER_MEMBER_PRESENT, PPEER_MEMBER, PPEER_MEMBER structure pointer [Peer Networking], p2p.peer_member, p2p/PPEER_MEMBER, p2p/peer_member_tag, peer_member_tag"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
tech.root: 
req.typenames: PEER_MEMBER, *PPEER_MEMBER
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - P2P.h
api_name:
 - PEER_MEMBER
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# peer_member_tag structure


## -description


The <b>PEER_MEMBER</b> structure contains information that describes a member of a peer group.


## -struct-fields




### -field dwSize

Specifies the size of this structure, in bytes.


### -field dwFlags

PEER_MEMBER_FLAGS enumeration value that specifies the state of the member.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="PEER_MEMBER_PRESENT"></a><a id="peer_member_present"></a><dl>
<dt><b>PEER_MEMBER_PRESENT</b></dt>
</dl>
</td>
<td width="60%">
The member is present in the peer group.

</td>
</tr>
</table>
 


### -field pwzIdentity

Pointer to a Unicode string that specifies the peer name of the member.


### -field pwzAttributes

Pointer to a unicode string that specifies the attributes of the member. The format of this string is defined by the application.


### -field ullNodeId

Unsigned 64-bit integer that contains the node ID. The same peer can have several node IDs, each identifying a different node that participates in a different peer group.


### -field cAddresses

Specifies the number of IP addresses listed in <b>pAddress</b>.


### -field pAddresses

Pointer to a list of <a href="https://msdn.microsoft.com/09476d3b-ec65-40a2-90ee-a20be230deca">PEER_ADDRESS</a> structures used by the member.


### -field pCredentialInfo

Pointer to a <a href="https://msdn.microsoft.com/c47bb38d-eafd-4218-8ac7-1c54ed6948ee">PEER_CREDENTIAL_INFO</a> structure that contains information about the security credentials of a member.


## -see-also




<a href="https://msdn.microsoft.com/09476d3b-ec65-40a2-90ee-a20be230deca">PEER_ADDRESS</a>



<a href="https://msdn.microsoft.com/c47bb38d-eafd-4218-8ac7-1c54ed6948ee">PEER_CREDENTIAL_INFO</a>
 

 

