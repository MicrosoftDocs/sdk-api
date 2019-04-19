---
UID: NS:p2p.peer_event_presence_changed_data_tag
title: PEER_EVENT_PRESENCE_CHANGED_DATA (p2p.h)
author: windows-sdk-content
description: The PEER_EVENT_PRESENCE_CHANGED_DATA structure contains information returned when a PEER_EVENT_ENDPOINT_PRESENCE_CHANGED or PEER_EVENT_MY_PRESENCE_CHANGED event is raised on a peer participating in a peer collaboration network.
old-location: p2p\peer_event_presence_changed_data.htm
tech.root: P2PSdk
ms.assetid: 31b64adf-f015-404a-aed7-0b9a21d83c9a
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*PPEER_EVENT_PRESENCE_CHANGED_DATA, PEER_EVENT_PRESENCE_CHANGED_DATA, PEER_EVENT_PRESENCE_CHANGED_DATA structure [Peer Networking], PPEER_EVENT_PRESENCE_CHANGED_DATA, PPEER_EVENT_PRESENCE_CHANGED_DATA structure pointer [Peer Networking], p2p.peer_event_presence_changed_data, p2p/PEER_EVENT_PRESENCE_CHANGED_DATA, p2p/PPEER_EVENT_PRESENCE_CHANGED_DATA"
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
 - PEER_EVENT_PRESENCE_CHANGED_DATA
product: Windows
targetos: Windows
req.typenames: PEER_EVENT_PRESENCE_CHANGED_DATA, *PPEER_EVENT_PRESENCE_CHANGED_DATA
req.redist: 
ms.custom: 19H1
---

# PEER_EVENT_PRESENCE_CHANGED_DATA structure


## -description


The <b>PEER_EVENT_PRESENCE_CHANGED_DATA</b> structure contains information returned when a PEER_EVENT_ENDPOINT_PRESENCE_CHANGED or PEER_EVENT_MY_PRESENCE_CHANGED event is raised on a peer participating in a peer collaboration network.


## -struct-fields




### -field pContact

Pointer to a <a href="https://msdn.microsoft.com/b84a17fc-35d6-4098-9bb3-18e708541a80">PEER_CONTACT</a> structure that contains the peer contact information for the contact whose change in presence raised the event.


### -field pEndpoint

Pointer to a <a href="https://msdn.microsoft.com/9687b332-14ed-4023-b8c2-437d75fd0298">PEER_ENDPOINT</a> structure that contains the peer endpoint information for the contact whose change in presence raised the event.


### -field changeType


<a href="https://msdn.microsoft.com/ef8f1cc7-e1db-4d6d-9ff6-141746d0787a">PEER_CHANGE_TYPE</a> enumeration value that specifies the type of presence change that occurred.


### -field pPresenceInfo

Pointer to a <a href="https://msdn.microsoft.com/e8f83ba8-81a3-4083-bc15-e00b2bec1cd4">PEER_PRESENCE_INFO</a> structure that contains the updated presence information for the endpoint of the contact whose change in presence raised the event.


## -see-also




<a href="https://msdn.microsoft.com/ef8f1cc7-e1db-4d6d-9ff6-141746d0787a">PEER_CHANGE_TYPE</a>



<a href="https://msdn.microsoft.com/b84a17fc-35d6-4098-9bb3-18e708541a80">PEER_CONTACT</a>



<a href="https://msdn.microsoft.com/9687b332-14ed-4023-b8c2-437d75fd0298">PEER_ENDPOINT</a>



<a href="https://msdn.microsoft.com/2634899c-3263-45ce-9fac-407e11e42cd4">Peer Collaboration API Structures</a>
 

 

