---
UID: NS:p2p.peer_graph_event_registration_tag
title: peer_graph_event_registration_tag
author: windows-sdk-content
description: The PEER_GRAPH_EVENT_REGISTRATION structure is used during registration for peer event notification. During registration it specifies which peer events an application requires notifications for.
old-location: p2p\peer_graph_event_registration.htm
old-project: P2PSdk
ms.assetid: 6725eba9-af61-4088-96e0-d0bf943902ea
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: "*PPEER_GRAPH_EVENT_REGISTRATION, PEER_GRAPH_EVENT_REGISTRATION, PEER_GRAPH_EVENT_REGISTRATION structure [Peer Networking], PPEER_GRAPH_EVENT_REGISTRATION, PPEER_GRAPH_EVENT_REGISTRATION structure pointer [Peer Networking], p2p.peer_graph_event_registration, p2p/PPEER_GRAPH_EVENT_REGISTRATION, p2p/peer_graph_event_registration_tag, peer_graph_event_registration_tag"
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
req.typenames: PEER_GRAPH_EVENT_REGISTRATION, *PPEER_GRAPH_EVENT_REGISTRATION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	P2P.h
api_name:
-	PEER_GRAPH_EVENT_REGISTRATION
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
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
 

 

