---
UID: NS:p2p.peer_event_endpoint_changed_data_tag
title: peer_event_endpoint_changed_data_tag
author: windows-sdk-content
description: The PEER_EVENT_ENDPOINT_CHANGED_DATA structure contains information returned when a PEER_EVENT_ENDPOINT_CHANGED or PEER_EVENT_MY_ENDPOINT_CHANGED event is raised on a peer participating in a peer collaboration network.
old-location: p2p\peer_event_endpoint_changed_data.htm
tech.root: P2PSdk
ms.assetid: e2ce28c6-6dc0-4ceb-aa3f-7b86a2581425
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: "*PPEER_EVENT_ENDPOINT_CHANGED_DATA, PEER_EVENT_ENDPOINT_CHANGED_DATA, PEER_EVENT_ENDPOINT_CHANGED_DATA structure [Peer Networking], PPEER_EVENT_ENDPOINT_CHANGED_DATA, PPEER_EVENT_ENDPOINT_CHANGED_DATA structure pointer [Peer Networking], p2p.peer_event_endpoint_changed_data, p2p/PEER_EVENT_ENDPOINT_CHANGED_DATA, p2p/PPEER_EVENT_ENDPOINT_CHANGED_DATA, peer_event_endpoint_changed_data_tag"
ms.prod: windows
ms.technology: windows-sdk
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
 - PEER_EVENT_ENDPOINT_CHANGED_DATA
product: Windows
targetos: Windows
req.typenames: PEER_EVENT_ENDPOINT_CHANGED_DATA, *PPEER_EVENT_ENDPOINT_CHANGED_DATA
req.redist: 
---

# peer_event_endpoint_changed_data_tag structure


## -description


The <b>PEER_EVENT_ENDPOINT_CHANGED_DATA</b> structure contains information returned when a PEER_EVENT_ENDPOINT_CHANGED or PEER_EVENT_MY_ENDPOINT_CHANGED event is raised on a peer participating in a peer collaboration network.


## -struct-fields




### -field pContact

Pointer to a <a href="https://msdn.microsoft.com/b84a17fc-35d6-4098-9bb3-18e708541a80">PEER_CONTACT</a> structure that contains the contact information for the contact who changed endpoints.


### -field pEndpoint

Pointer to a <a href="https://msdn.microsoft.com/9687b332-14ed-4023-b8c2-437d75fd0298">PEER_ENDPOINT</a> structure that contains the new active endpoint for  the peer specified in <i>pContact</i>.


## -remarks



This event is raised when information about the endpoint changes. An example of this being the endpoint name in <a href="https://msdn.microsoft.com/9687b332-14ed-4023-b8c2-437d75fd0298">PEER_ENDPOINT</a> structure is changed using <a href="https://msdn.microsoft.com/9b8d0559-c70e-4b05-bd73-1eb3b2e8f9c8">PeerCollabSetEndpointName</a>.




## -see-also




<a href="https://msdn.microsoft.com/b84a17fc-35d6-4098-9bb3-18e708541a80">PEER_CONTACT</a>



<a href="https://msdn.microsoft.com/9687b332-14ed-4023-b8c2-437d75fd0298">PEER_ENDPOINT</a>



<a href="https://msdn.microsoft.com/2634899c-3263-45ce-9fac-407e11e42cd4">Peer Collaboration API Structures</a>
 

 

