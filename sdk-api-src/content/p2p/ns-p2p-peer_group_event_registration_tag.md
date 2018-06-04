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

# peer_group_event_registration_tag structure


## -description


The <b>PEER_GROUP_EVENT_REGISTRATION</b> structure defines the particular peer group event a member can register for.


## -struct-fields




### -field eventType


<a href="https://msdn.microsoft.com/9c28eb24-f158-4313-9a7c-0f271013d03a">PEER_GROUP_EVENT_TYPE</a> that specifies the peer group event type to register for.


### -field pType

GUID value that identifies the type of record or data message that  raises an event of the type specified by <b>eventType</b>. For example, if the peer wishes to be notified about all changes to a specific record type,  the GUID that corresponds to this record type must be supplied in this field and PEER_GROUP_RECORD_CHANGED must be in <b>eventType</b>.

This member is only populated (not NULL) when <b>eventType</b> is either PEER_GROUP_EVENT_RECORD_CHANGED or PEER_GROUP_EVENT_INCOMING_DATA.


## -see-also




<a href="https://msdn.microsoft.com/9c28eb24-f158-4313-9a7c-0f271013d03a">PEER_GROUP_EVENT_TYPE</a>



<a href="https://msdn.microsoft.com/a4dc100a-d3dc-408e-a425-bded11d04db5">PeerGroupRegisterEvent</a>
 

 

