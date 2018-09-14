---
UID: NE:p2p.peer_group_property_flags_tag
title: peer_group_property_flags_tag
author: windows-sdk-content
description: The PEER_GROUP_PROPERTY_FLAGS flags are used to specify various peer group membership settings.
old-location: p2p\peer_group_property_flags.htm
tech.root: p2psdk
ms.assetid: ce8a4245-391d-4433-8811-8d190d94815c
ms.author: windowssdkdev
ms.date: 08/31/2018
ms.keywords: PEER_DEFER_EXPIRATION, PEER_DISABLE_PRESENCE, PEER_GROUP_PROPERTY_FLAGS, PEER_GROUP_PROPERTY_FLAGS enumeration [Peer Networking], PEER_MEMBER_DATA_OPTIONAL, p2p.peer_group_property_flags, p2p/PEER_DEFER_EXPIRATION, p2p/PEER_DISABLE_PRESENCE, p2p/PEER_GROUP_PROPERTY_FLAGS, p2p/PEER_MEMBER_DATA_OPTIONAL, peer_group_property_flags_tag
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: p2p.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2 [desktop apps only],Windows XP with SP1with the Advanced Networking Pack forWindows XP
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
 - PEER_GROUP_PROPERTY_FLAGS
product: Windows
targetos: Windows
req.typenames: PEER_GROUP_PROPERTY_FLAGS
req.redist: 
---

# peer_group_property_flags_tag enumeration


## -description


The <b>PEER_GROUP_PROPERTY_FLAGS</b>  flags are used to specify various peer group membership settings.


## -enum-fields




### -field PEER_MEMBER_DATA_OPTIONAL

A peer's member data (<a href="https://msdn.microsoft.com/b8bd0e17-6af7-426d-ba38-11ff4948cf67">PEER_MEMBER</a>) is only published  when an action if performed, such as publishing a record  or issuing a GMC. If the peer has not performed one of these actions, the membership data will not be available.


### -field PEER_DISABLE_PRESENCE

The peer presence system is prevented from automatically publishing presence information.


### -field PEER_DEFER_EXPIRATION

Group records are not expired until the peer  connects with a group.


## -remarks



These flags can only be set by the peer group creator.




## -see-also




<a href="https://msdn.microsoft.com/b8bd0e17-6af7-426d-ba38-11ff4948cf67">PEER_MEMBER</a>
 

 

