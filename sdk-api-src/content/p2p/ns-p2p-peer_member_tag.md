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
 

 

