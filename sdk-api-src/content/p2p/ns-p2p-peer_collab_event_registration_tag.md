---
UID: NS:p2p.peer_collab_event_registration_tag
title: peer_collab_event_registration_tag
author: windows-driver-content
description: The PEER_COLLAB_EVENT_REGISTRATION structure contains the data used by a peer to register for specific peer collaboration network events.
old-location: p2p\peer_collab_event_registration.htm
old-project: P2PSdk
ms.assetid: dfc55346-99ef-441e-ba49-e7463581ebbb
ms.author: windowsdriverdev
ms.date: 4/23/2018
ms.keywords: "*PPEER_COLLAB_EVENT_REGISTRATION, PCPEER_COLLAB_EVENT_REGISTRATION, PCPEER_COLLAB_EVENT_REGISTRATION structure pointer [Peer Networking], PEER_COLLAB_EVENT_REGISTRATION, PEER_COLLAB_EVENT_REGISTRATION structure [Peer Networking], PPEER_COLLAB_EVENT_REGISTRATION, PPEER_COLLAB_EVENT_REGISTRATION structure pointer [Peer Networking], p2p.peer_collab_event_registration, p2p/PCPEER_COLLAB_EVENT_REGISTRATION, p2p/PEER_COLLAB_EVENT_REGISTRATION, p2p/PPEER_COLLAB_EVENT_REGISTRATION, peer_collab_event_registration_tag"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: p2p.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
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
req.typenames: PEER_COLLAB_EVENT_REGISTRATION, *PPEER_COLLAB_EVENT_REGISTRATION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	P2P.h
api_name:
-	PEER_COLLAB_EVENT_REGISTRATION
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# peer_collab_event_registration_tag structure


## -description


The <b>PEER_COLLAB_EVENT_REGISTRATION</b> structure contains the data used by a peer to register for specific peer collaboration network events.


## -struct-fields




### -field eventType


<a href="https://msdn.microsoft.com/2266c518-d383-4f37-9494-d57a3f780ced">PEER_COLLAB_EVENT_TYPE</a> enumeration value that specifies the type of peer collaboration network event for which to register.


### -field pInstance

GUID value that uniquely identifies the application or object  that registers for the specific event.

This parameter is valid only for PEER_EVENT_ENDPOINT_APPLICATION_CHANGED, PEER_EVENT_ENDPOINT_OBJECT_CHANGED, PEER_EVENT_MY_APPLICATION_CHANGED, and PEER_EVENT_MY_OBJECT_CHANGED. This GUID represents the application ID for application-specific events, and the object ID for object-specific events.  

When <b></b>this member is set, notification will be sent only for the specific application or object.


## -see-also




<a href="https://msdn.microsoft.com/2266c518-d383-4f37-9494-d57a3f780ced">PEER_COLLAB_EVENT_TYPE</a>



<a href="https://msdn.microsoft.com/2634899c-3263-45ce-9fac-407e11e42cd4">Peer Collaboration API Structures</a>
 

 

