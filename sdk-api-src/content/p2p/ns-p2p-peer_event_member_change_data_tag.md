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

# peer_event_member_change_data_tag structure


## -description


The <b>PEER_EVENT_MEMBER_CHANGE_DATA</b> structure contains data that describes a change in the status of a peer group member.


## -struct-fields




### -field dwSize

Contains the size of this structure, in bytes.


### -field changeType

<b>PEER_MEMBER_CHANGE_TYPE</b> enumeration value that specifies the change event that occurred, such as a member joining or leaving.


### -field pwzIdentity

Pointer to a Unicode string that contains the peer name of the peer group member.


## -see-also




<a href="https://msdn.microsoft.com/5cdae832-e6a7-481c-9784-1c1c07d689dd">PEER_GROUP_EVENT_DATA</a>



<a href="https://msdn.microsoft.com/9c9c82c3-b02a-49c2-9a8f-eb355ded8480">PEER_GROUP_EVENT_REGISTRATION</a>



<a href="https://msdn.microsoft.com/ecebec4f-1dc6-481c-a2d4-cf0043729a8c">PEER_MEMBER_CHANGE_TYPE</a>
 

 

