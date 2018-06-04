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
 

 

