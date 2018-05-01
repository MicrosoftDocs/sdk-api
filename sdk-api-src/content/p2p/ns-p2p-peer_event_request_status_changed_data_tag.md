---
UID: NS:p2p.peer_event_request_status_changed_data_tag
title: peer_event_request_status_changed_data_tag
author: windows-driver-content
description: The PEER_EVENT_REQUEST_STATUS_CHANGED_DATA structure contains information returned when a PEER_EVENT_REQUEST_STATUS_CHANGED event is raised on a peer participating in a peer collaboration network.
old-location: p2p\peer_event_request_status_changed_data.htm
old-project: P2PSdk
ms.assetid: 88bcf892-5591-49a0-bb00-090f4d5f2f79
ms.author: windowsdriverdev
ms.date: 4/23/2018
ms.keywords: "*PPEER_EVENT_REQUEST_STATUS_CHANGED_DATA, PEER_EVENT_REQUEST_STATUS_CHANGED_DATA, PEER_EVENT_REQUEST_STATUS_CHANGED_DATA structure [Peer Networking], PPEER_EVENT_REQUEST_STATUS_CHANGED_DATA, PPEER_EVENT_REQUEST_STATUS_CHANGED_DATA structure pointer [Peer Networking], p2p.peer_event_request_status_changed_data, p2p/PEER_EVENT_REQUEST_STATUS_CHANGED_DATA, p2p/PPEER_EVENT_REQUEST_STATUS_CHANGED_DATA, peer_event_request_status_changed_data_tag"
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
req.typenames: PEER_EVENT_REQUEST_STATUS_CHANGED_DATA, *PPEER_EVENT_REQUEST_STATUS_CHANGED_DATA
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	P2P.h
api_name:
-	PEER_EVENT_REQUEST_STATUS_CHANGED_DATA
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# peer_event_request_status_changed_data_tag structure


## -description


The <b>PEER_EVENT_REQUEST_STATUS_CHANGED_DATA</b> structure contains information returned when a PEER_EVENT_REQUEST_STATUS_CHANGED event is raised on a peer participating in a peer collaboration network.


## -struct-fields




### -field pEndpoint

Pointer to a <a href="https://msdn.microsoft.com/9687b332-14ed-4023-b8c2-437d75fd0298">PEER_ENDPOINT</a> structure that contains the peer endpoint information for the contact whose change in request status raised the event.


### -field hrChange

HRESULT value that indicates the change in request status that occurred.


## -remarks



This event is raised when the infrastructure  finishes processing the request for <a href="https://msdn.microsoft.com/ba841da4-de7f-4288-84b7-a06370b55e3c">PeerCollabRefreshEndpointData</a> or <a href="https://msdn.microsoft.com/dfe17235-34dd-4694-9ee5-4268b4406731">PeerCollabSubscribeEndpointData</a>. If the  process fails <b>hrChange</b> value will most typically be PEER_E_CONNECTION_FAILED.




## -see-also




<a href="https://msdn.microsoft.com/ef8f1cc7-e1db-4d6d-9ff6-141746d0787a">PEER_CHANGE_TYPE</a>



<a href="https://msdn.microsoft.com/9687b332-14ed-4023-b8c2-437d75fd0298">PEER_ENDPOINT</a>



<a href="https://msdn.microsoft.com/2634899c-3263-45ce-9fac-407e11e42cd4">Peer Collaboration API Structures</a>
 

 

