---
UID: NS:p2p.peer_graph_event_data_tag
title: PEER_GRAPH_EVENT_DATA (p2p.h)
description: The PEER_GRAPH_EVENT_DATA structure contains data associated with a peer event.
helpviewer_keywords: ["*PPEER_GRAPH_EVENT_DATA","PEER_GRAPH_EVENT_DATA","PEER_GRAPH_EVENT_DATA structure [Peer Networking]","PPEER_GRAPH_EVENT_DATA","PPEER_GRAPH_EVENT_DATA structure pointer [Peer Networking]","p2p.peer_graph_event_data","p2p/PPEER_GRAPH_EVENT_DATA","p2p/peer_graph_event_data_tag"]
old-location: p2p\peer_graph_event_data.htm
tech.root: p2p
ms.assetid: a052bff8-e90c-4ff7-8362-edb94b130f38
ms.date: 12/05/2018
ms.keywords: '*PPEER_GRAPH_EVENT_DATA, PEER_GRAPH_EVENT_DATA, PEER_GRAPH_EVENT_DATA structure [Peer Networking], PPEER_GRAPH_EVENT_DATA, PPEER_GRAPH_EVENT_DATA structure pointer [Peer Networking], p2p.peer_graph_event_data, p2p/PPEER_GRAPH_EVENT_DATA, p2p/peer_graph_event_data_tag'
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: PEER_GRAPH_EVENT_DATA, *PPEER_GRAPH_EVENT_DATA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - peer_graph_event_data_tag
 - p2p/peer_graph_event_data_tag
 - PPEER_GRAPH_EVENT_DATA
 - p2p/PPEER_GRAPH_EVENT_DATA
 - PEER_GRAPH_EVENT_DATA
 - p2p/PEER_GRAPH_EVENT_DATA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - P2P.h
api_name:
 - PEER_GRAPH_EVENT_DATA
---

# PEER_GRAPH_EVENT_DATA structure


## -description

The <b>PEER_GRAPH_EVENT_DATA</b> structure contains data associated with a peer event.

## -struct-fields

### -field eventType

The type of peer event this data corresponds to. Must be one of the <a href="/windows/desktop/api/p2p/ne-p2p-peer_graph_event_type">PEER_GRAPH_EVENT_TYPE</a> values. The members that remain are given values based on the peer event type that has occurred.  Not all members contain data.

### -field dwStatus

This member is given a value  if the <a href="/windows/desktop/api/p2p/ne-p2p-peer_graph_event_type">PEER_GRAPH_EVENT_STATUS_CHANGE</a> peer event is triggered.  A change has been made in relation to a node's connection to the graph.

### -field incomingData

This member is given a value if the <a href="/windows/desktop/api/p2p/ns-p2p-peer_event_incoming_data">PEER_GRAPH_INCOMING_DATA</a> peer event is triggered.  A node has received data from a neighbor or a direct connection.

### -field recordChangeData

This member given a value if the <a href="/windows/desktop/api/p2p/ns-p2p-peer_event_record_change_data">PEER_GRAPH_EVENT_RECORD_CHANGE</a> peer event is triggered.  A record type the application asked for notifications of has changed.

### -field connectionChangeData

This member is given a value if the <a href="/windows/desktop/api/p2p/ns-p2p-peer_event_connection_change_data">PEER_GRAPH_EVENT_NEIGHBOR_CONNECTION</a> or <b>PEER_GRAPH_EVENT_DIRECT_CONNECTION</b> peer event is triggered.  An aspect of a neighbor or direct connection state has changed.

### -field nodeChangeData

This member is given a value if the <a href="/windows/desktop/api/p2p/ns-p2p-peer_event_node_change_data">PEER_GRAPH_EVENT_NODE_CHANGED</a> peer event is triggered.  A node's presence state has changed.

### -field synchronizedData

This member is given a value if the <a href="/windows/desktop/api/p2p/ns-p2p-peer_event_synchronized_data">PEER_GRAPH_EVENT_SYNCHRONIZED</a> peer event is triggered.  A record type has completed its synchronization.

## -see-also

<a href="/windows/desktop/api/p2p/ns-p2p-peer_event_connection_change_data">PEER_EVENT_CONNECTION_CHANGE_DATA</a>



<a href="/windows/desktop/api/p2p/ns-p2p-peer_event_incoming_data">PEER_EVENT_INCOMING_DATA</a>



<a href="/windows/desktop/api/p2p/ns-p2p-peer_event_node_change_data">PEER_EVENT_NODE_CHANGE_DATA</a>



<a href="/windows/desktop/api/p2p/ns-p2p-peer_event_record_change_data">PEER_EVENT_RECORD_CHANGE_DATA</a>



<a href="/windows/desktop/api/p2p/ns-p2p-peer_event_synchronized_data">PEER_EVENT_SYNCHRONIZED_DATA</a>



<a href="/windows/desktop/api/p2p/ne-p2p-peer_graph_event_type">PEER_GRAPH_EVENT_TYPE</a>



<a href="/windows/desktop/api/p2p/ne-p2p-peer_graph_status_flags">PEER_GRAPH_STATUS_FLAGS</a>



<a href="/windows/desktop/api/p2p/nf-p2p-peergraphgeteventdata">PeerGraphGetEventData</a>