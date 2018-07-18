---
UID: NE:p2p.peer_graph_event_type_tag
title: peer_graph_event_type_tag
author: windows-sdk-content
description: The PEER_GRAPH_EVENT_TYPE enumeration specifies peer event types the application is to be notified for.
old-location: p2p\peer_graph_event_type.htm
old-project: P2PSdk
ms.assetid: 0fb9443f-bf95-45e2-b105-400203f286b6
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: PEER_GRAPH_EVENT_CONNECTION_REQUIRED, PEER_GRAPH_EVENT_DIRECT_CONNECTION, PEER_GRAPH_EVENT_INCOMING_DATA, PEER_GRAPH_EVENT_NEIGHBOR_CONNECTION, PEER_GRAPH_EVENT_NODE_CHANGED, PEER_GRAPH_EVENT_PROPERTY_CHANGED, PEER_GRAPH_EVENT_RECORD_CHANGED, PEER_GRAPH_EVENT_STATUS_CHANGED, PEER_GRAPH_EVENT_SYNCHRONIZED, PEER_GRAPH_EVENT_TYPE, PEER_GRAPH_EVENT_TYPE enumeration [Peer Networking], p2p.peer_graph_event_type, p2p/ PEER_GRAPH_EVENT_TYPE, p2p/PEER_GRAPH_EVENT_CONNECTION_REQUIRED, p2p/PEER_GRAPH_EVENT_DIRECT_CONNECTION, p2p/PEER_GRAPH_EVENT_INCOMING_DATA, p2p/PEER_GRAPH_EVENT_NEIGHBOR_CONNECTION, p2p/PEER_GRAPH_EVENT_NODE_CHANGED, p2p/PEER_GRAPH_EVENT_PROPERTY_CHANGED, p2p/PEER_GRAPH_EVENT_RECORD_CHANGED, p2p/PEER_GRAPH_EVENT_STATUS_CHANGED, p2p/PEER_GRAPH_EVENT_SYNCHRONIZED, peer_graph_event_type_tag
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
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
tech.root: 
req.typenames: PEER_GRAPH_EVENT_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - P2P.h
api_name:
 - PEER_GRAPH_EVENT_TYPE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
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
 

 

