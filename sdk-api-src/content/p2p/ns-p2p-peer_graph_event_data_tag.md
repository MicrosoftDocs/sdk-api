---
UID: NS:p2p.peer_graph_event_data_tag
title: peer_graph_event_data_tag
author: windows-sdk-content
description: The PEER_GRAPH_EVENT_DATA structure contains data associated with a peer event.
old-location: p2p\peer_graph_event_data.htm
old-project: P2PSdk
ms.assetid: a052bff8-e90c-4ff7-8362-edb94b130f38
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: "*PPEER_GRAPH_EVENT_DATA, PEER_GRAPH_EVENT_DATA, PEER_GRAPH_EVENT_DATA structure [Peer Networking], PPEER_GRAPH_EVENT_DATA, PPEER_GRAPH_EVENT_DATA structure pointer [Peer Networking], p2p.peer_graph_event_data, p2p/PPEER_GRAPH_EVENT_DATA, p2p/peer_graph_event_data_tag, peer_graph_event_data_tag"
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
tech.root: 
req.typenames: PEER_GRAPH_EVENT_DATA, *PPEER_GRAPH_EVENT_DATA
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	P2P.h
api_name:
-	PEER_GRAPH_EVENT_DATA
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# peer_graph_event_data_tag structure


## -description


The <b>PEER_GRAPH_EVENT_DATA</b> structure contains data associated with a peer event.


## -struct-fields




### -field eventType

The type of peer event this data corresponds to. Must be one of the <a href="https://msdn.microsoft.com/0fb9443f-bf95-45e2-b105-400203f286b6">PEER_GRAPH_EVENT_TYPE</a> values. The members that remain are given values based on the peer event type that has occurred.  Not all members contain data.


### -field dwStatus

This member is given a value  if the <a href="https://msdn.microsoft.com/0fb9443f-bf95-45e2-b105-400203f286b6">PEER_GRAPH_EVENT_STATUS_CHANGE</a> peer event is triggered.  A change has been made in relation to a node's connection to the graph.


### -field incomingData

This member is given a value if the <a href="https://msdn.microsoft.com/93104ca5-b3de-492c-965e-3acd12d05ea6">PEER_GRAPH_INCOMING_DATA</a> peer event is triggered.  A node has received data from a neighbor or a direct connection.


### -field recordChangeData

This member given a value if the <a href="https://msdn.microsoft.com/01404fff-3488-43aa-bc59-3e08ff925ea5">PEER_GRAPH_EVENT_RECORD_CHANGE</a> peer event is triggered.  A record type the application asked for notifications of has changed.


### -field connectionChangeData

This member is given a value if the <a href="https://msdn.microsoft.com/0d73432c-c1e5-4fa9-a812-377b22a47440">PEER_GRAPH_EVENT_NEIGHBOR_CONNECTION</a> or <b>PEER_GRAPH_EVENT_DIRECT_CONNECTION</b> peer event is triggered.  An aspect of a neighbor or direct connection state has changed.


### -field nodeChangeData

This member is given a value if the <a href="https://msdn.microsoft.com/656c9155-643d-4c94-9141-3499f7e0adac">PEER_GRAPH_EVENT_NODE_CHANGED</a> peer event is triggered.  A node's presence state has changed.


### -field synchronizedData

This member is given a value if the <a href="https://msdn.microsoft.com/ae7dc220-a827-4671-97b3-1ac039ab3e08">PEER_GRAPH_EVENT_SYNCHRONIZED</a> peer event is triggered.  A record type has completed its synchronization.


## -see-also




<a href="https://msdn.microsoft.com/0d73432c-c1e5-4fa9-a812-377b22a47440">PEER_EVENT_CONNECTION_CHANGE_DATA</a>



<a href="https://msdn.microsoft.com/93104ca5-b3de-492c-965e-3acd12d05ea6">PEER_EVENT_INCOMING_DATA</a>



<a href="https://msdn.microsoft.com/656c9155-643d-4c94-9141-3499f7e0adac">PEER_EVENT_NODE_CHANGE_DATA</a>



<a href="https://msdn.microsoft.com/01404fff-3488-43aa-bc59-3e08ff925ea5">PEER_EVENT_RECORD_CHANGE_DATA</a>



<a href="https://msdn.microsoft.com/ae7dc220-a827-4671-97b3-1ac039ab3e08">PEER_EVENT_SYNCHRONIZED_DATA</a>



<a href="https://msdn.microsoft.com/0fb9443f-bf95-45e2-b105-400203f286b6">PEER_GRAPH_EVENT_TYPE</a>



<a href="https://msdn.microsoft.com/71910437-4ebd-4fcc-977c-0a56c5f26d61">PEER_GRAPH_STATUS_FLAGS</a>



<a href="https://msdn.microsoft.com/b64bb920-3fbc-4927-a1b1-39c99850bdd5">PeerGraphGetEventData</a>
 

 

