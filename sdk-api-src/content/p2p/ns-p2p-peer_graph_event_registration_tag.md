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

# peer_graph_event_registration_tag structure


## -description


The <b>PEER_GRAPH_EVENT_REGISTRATION</b> structure is used during registration for peer event notification. During registration it specifies which peer events an application requires notifications for.


## -struct-fields




### -field eventType

Specifies the type of peer event the application requires notifications for. The per events that can be registered for are specified by the <a href="https://msdn.microsoft.com/0fb9443f-bf95-45e2-b105-400203f286b6">PEER_GRAPH_EVENT_TYPE</a> enumeration.


### -field pType

If the peer event specified by  <b>eventType</b>  relates to records, use this member to specify which types of records the application requires notifications for.  Specify <b>NULL</b> to receive notifications for all record types.   This member is ignored if the  event specified by <b>eventType</b> does not relate to  records.


## -see-also




<a href="https://msdn.microsoft.com/0fb9443f-bf95-45e2-b105-400203f286b6">PEER_GRAPH_EVENT_TYPE</a>



<a href="https://msdn.microsoft.com/3ed963ba-0b9d-4de8-a610-b07cf49ed27f">PeerGraphRegisterEvent</a>
 

 

