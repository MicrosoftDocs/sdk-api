---
UID: NS:p2p.peer_group_properties_tag
title: peer_group_properties_tag
author: windows-sdk-content
description: The PEER_GROUP_PROPERTIES structure contains data about the membership policy of a peer group.
old-location: p2p\peer_group_properties.htm
tech.root: P2PSdk
ms.assetid: a1501343-bd84-4dbe-91d0-c64c59e34abc
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: "*PPEER_GROUP_PROPERTIES, PEER_GROUP_PROPERTIES, PEER_GROUP_PROPERTIES structure [Peer Networking], PPEER_GROUP_PROPERTIES, PPEER_GROUP_PROPERTIES structure pointer [Peer Networking], p2p.peer_group_properties, p2p/PPEER_GROUP_PROPERTIES, p2p/peer_group_properties_tag, peer_group_properties_tag"
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - P2P.h
api_name:
 - PEER_GROUP_PROPERTIES
product: Windows
targetos: Windows
req.typenames: PEER_GROUP_PROPERTIES, *PPEER_GROUP_PROPERTIES
req.redist: 
---

# peer_group_properties_tag structure


## -description


The <b>PEER_GROUP_PROPERTIES</b> structure contains data about the   membership policy of a peer group.


## -struct-fields




### -field dwSize

Size of the structure, in bytes.


### -field dwFlags


<a href="https://msdn.microsoft.com/ce8a4245-391d-4433-8811-8d190d94815c">PEER_GROUP_PROPERTY_FLAGS</a> flags that describe the behavior of a peer group. The default value is zero (0), which indicates that flags are not set.


### -field pwzCloud

Specifies the name of the   Peer Name Resolution Protocol (PNRP) cloud that  a peer group participates in. The default value is "global", if this member is <b>NULL</b>.


### -field pwzClassifier

Specifies the classifier used to  identify the authority of a peer group peer name for registration or resolution within a PNRP cloud. The maximum size of this field is 149 Unicode characters. This member can be <b>NULL</b>.


### -field pwzGroupPeerName

Specifies the name of a peer group that is registered with the PNRP service. The maximum size of this field is 137 Unicode characters.


### -field pwzCreatorPeerName

Specifies the  peer name associated with the Peer group creator. The maximum size of this field is 137 Unicode characters. If this structure member is <b>NULL</b>, the implementation uses the identity obtained from <a href="https://msdn.microsoft.com/195052a2-eaae-4b8c-bc13-0667ce50a967">PeerIdentityGetDefault</a>.


### -field pwzFriendlyName

Specifies the friendly (display) name of a peer group. The maximum size of this field is 255 characters.


### -field pwzComment

Contains a comment used to describe a peer group. The maximum size of this field is 255 characters.


### -field ulMemberDataLifetime

Specifies the lifetime, in seconds, of peer group member data (<a href="https://msdn.microsoft.com/b8bd0e17-6af7-426d-ba38-11ff4948cf67">PEER_MEMBER</a>). The minimum value for this field is 8 hours, and the maximum is 10 years. The default value is 2,419,200 seconds, or 28 days.

If this value is set to zero (0), member data has the maximum allowable lifetime, which is the time remaining in the lifetime of the administrator who issues the credentials for a member.


### -field ulPresenceLifetime

Specifies the lifetime, in seconds, of presence information published to a peer group. The default value is 300 seconds. Do not set the value  of   <b>ulPresenceLifetime</b> to less than 300  seconds. If this member is set to less than the 300–second default value, then undefined behavior can occur.


### -field dwAuthenticationSchemes

<b>Windows Vista or later.</b> Logical OR of <a href="https://msdn.microsoft.com/51bbbfdb-fa64-473b-aa48-2562512a2af3">PEER_GROUP_AUTHENTICATION_SCHEME</a> enumeration values that indicate the types of authentication supported by the peer group.


### -field pwzGroupPassword

<b>Windows Vista or later.</b> Pointer to a Unicode string that contains the password used to authenticate peers attempting to join the peer group.


### -field groupPasswordRole

<b>Windows Vista or later.</b> GUID value that indicates the peer group role for which the password is required for authentication.


## -see-also




<a href="https://msdn.microsoft.com/b85d87c6-28b7-49f8-865c-9d246f89367e">PeerGroupCreate</a>



<a href="https://msdn.microsoft.com/6273817f-9698-4c0b-93a9-9bbee2e5dc78">PeerGroupGetProperties</a>



<a href="https://msdn.microsoft.com/20acf963-de8f-4bcd-a9d6-a513d516b108">PeerGroupSetProperties</a>
 

 

