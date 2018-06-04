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

# peer_graph_event_type_tag enumeration


## -description



      The <b>PEER_GRAPH_EVENT_TYPE</b> enumeration specifies peer event types the application is to be notified for.


## -enum-fields




### -field PEER_GRAPH_EVENT_STATUS_CHANGED

The peer graph   status has changed in some manner. For example, the node has synchronized with the peer graph.


### -field PEER_GRAPH_EVENT_PROPERTY_CHANGED

A field in the peer graph property structure has changed. This peer event does not generate  a specific piece of data for an application to retrieve. The application must use <a href="https://msdn.microsoft.com/f62fadf8-8cc2-4597-93b0-e076258ccd6a">PeerGraphGetProperties</a> to obtain the updated structure.


### -field PEER_GRAPH_EVENT_RECORD_CHANGED

A record type or specific record has changed in some manner.


### -field PEER_GRAPH_EVENT_DIRECT_CONNECTION

A peer's direct connection has changed.


### -field PEER_GRAPH_EVENT_NEIGHBOR_CONNECTION

A connection to a peer neighbor has changed.


### -field PEER_GRAPH_EVENT_INCOMING_DATA

Data has been received from a direct or neighbor connection.


### -field PEER_GRAPH_EVENT_CONNECTION_REQUIRED

The peer graph has become unstable.  The client should call <a href="https://msdn.microsoft.com/76a2c54d-4424-4aa3-9b62-3ebe88b63c9f">PeerGraphConnect</a> on a new node. This peer event does not generate  a specific piece of data for an application to retrieve.


### -field PEER_GRAPH_EVENT_NODE_CHANGED

A node's presence status has changed in the peer graph.


### -field PEER_GRAPH_EVENT_SYNCHRONIZED

A specific  record type has been synchronized.


## -see-also




<a href="https://msdn.microsoft.com/a052bff8-e90c-4ff7-8362-edb94b130f38">
        PEER_GRAPH_EVENT_DATA</a>



<a href="https://msdn.microsoft.com/6725eba9-af61-4088-96e0-d0bf943902ea">
        PEER_GRAPH_EVENT_REGISTRATION</a>



<a href="https://msdn.microsoft.com/76a2c54d-4424-4aa3-9b62-3ebe88b63c9f">PeerGraphConnect</a>



<a href="https://msdn.microsoft.com/f62fadf8-8cc2-4597-93b0-e076258ccd6a">PeerGraphGetProperties</a>
 

 

