---
UID: NE:p2p.peer_graph_event_type_tag
title: PEER_GRAPH_EVENT_TYPE (p2p.h)
description: The PEER_GRAPH_EVENT_TYPE enumeration specifies peer event types the application is to be notified for.
helpviewer_keywords: ["PEER_GRAPH_EVENT_CONNECTION_REQUIRED","PEER_GRAPH_EVENT_DIRECT_CONNECTION","PEER_GRAPH_EVENT_INCOMING_DATA","PEER_GRAPH_EVENT_NEIGHBOR_CONNECTION","PEER_GRAPH_EVENT_NODE_CHANGED","PEER_GRAPH_EVENT_PROPERTY_CHANGED","PEER_GRAPH_EVENT_RECORD_CHANGED","PEER_GRAPH_EVENT_STATUS_CHANGED","PEER_GRAPH_EVENT_SYNCHRONIZED","PEER_GRAPH_EVENT_TYPE","PEER_GRAPH_EVENT_TYPE enumeration [Peer Networking]","p2p.peer_graph_event_type","p2p/PEER_GRAPH_EVENT_CONNECTION_REQUIRED","p2p/PEER_GRAPH_EVENT_DIRECT_CONNECTION","p2p/PEER_GRAPH_EVENT_INCOMING_DATA","p2p/PEER_GRAPH_EVENT_NEIGHBOR_CONNECTION","p2p/PEER_GRAPH_EVENT_NODE_CHANGED","p2p/PEER_GRAPH_EVENT_PROPERTY_CHANGED","p2p/PEER_GRAPH_EVENT_RECORD_CHANGED","p2p/PEER_GRAPH_EVENT_STATUS_CHANGED","p2p/PEER_GRAPH_EVENT_SYNCHRONIZED","p2p/PEER_GRAPH_EVENT_TYPE"]
old-location: p2p\peer_graph_event_type.htm
tech.root: p2p
ms.assetid: 0fb9443f-bf95-45e2-b105-400203f286b6
ms.date: 12/05/2018
ms.keywords: PEER_GRAPH_EVENT_CONNECTION_REQUIRED, PEER_GRAPH_EVENT_DIRECT_CONNECTION, PEER_GRAPH_EVENT_INCOMING_DATA, PEER_GRAPH_EVENT_NEIGHBOR_CONNECTION, PEER_GRAPH_EVENT_NODE_CHANGED, PEER_GRAPH_EVENT_PROPERTY_CHANGED, PEER_GRAPH_EVENT_RECORD_CHANGED, PEER_GRAPH_EVENT_STATUS_CHANGED, PEER_GRAPH_EVENT_SYNCHRONIZED, PEER_GRAPH_EVENT_TYPE, PEER_GRAPH_EVENT_TYPE enumeration [Peer Networking], p2p.peer_graph_event_type, p2p/PEER_GRAPH_EVENT_CONNECTION_REQUIRED, p2p/PEER_GRAPH_EVENT_DIRECT_CONNECTION, p2p/PEER_GRAPH_EVENT_INCOMING_DATA, p2p/PEER_GRAPH_EVENT_NEIGHBOR_CONNECTION, p2p/PEER_GRAPH_EVENT_NODE_CHANGED, p2p/PEER_GRAPH_EVENT_PROPERTY_CHANGED, p2p/PEER_GRAPH_EVENT_RECORD_CHANGED, p2p/PEER_GRAPH_EVENT_STATUS_CHANGED, p2p/PEER_GRAPH_EVENT_SYNCHRONIZED, p2p/PEER_GRAPH_EVENT_TYPE
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
req.typenames: PEER_GRAPH_EVENT_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - peer_graph_event_type_tag
 - p2p/peer_graph_event_type_tag
 - PEER_GRAPH_EVENT_TYPE
 - p2p/PEER_GRAPH_EVENT_TYPE
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
 - PEER_GRAPH_EVENT_TYPE
---

# PEER_GRAPH_EVENT_TYPE enumeration


## -description

The <b>PEER_GRAPH_EVENT_TYPE</b> enumeration specifies peer event types the application is to be notified for.

## -enum-fields

### -field PEER_GRAPH_EVENT_STATUS_CHANGED:1

The peer graph   status has changed in some manner. For example, the node has synchronized with the peer graph.

### -field PEER_GRAPH_EVENT_PROPERTY_CHANGED:2

A field in the peer graph property structure has changed. This peer event does not generate  a specific piece of data for an application to retrieve. The application must use <a href="/windows/desktop/api/p2p/nf-p2p-peergraphgetproperties">PeerGraphGetProperties</a> to obtain the updated structure.

### -field PEER_GRAPH_EVENT_RECORD_CHANGED:3

A record type or specific record has changed in some manner.

### -field PEER_GRAPH_EVENT_DIRECT_CONNECTION:4

A peer's direct connection has changed.

### -field PEER_GRAPH_EVENT_NEIGHBOR_CONNECTION:5

A connection to a peer neighbor has changed.

### -field PEER_GRAPH_EVENT_INCOMING_DATA:6

Data has been received from a direct or neighbor connection.

### -field PEER_GRAPH_EVENT_CONNECTION_REQUIRED:7

The peer graph has become unstable.  The client should call <a href="/windows/desktop/api/p2p/nf-p2p-peergraphconnect">PeerGraphConnect</a> on a new node. This peer event does not generate  a specific piece of data for an application to retrieve.

### -field PEER_GRAPH_EVENT_NODE_CHANGED:8

A node's presence status has changed in the peer graph.

### -field PEER_GRAPH_EVENT_SYNCHRONIZED:9

A specific  record type has been synchronized.

## -see-also

<a href="/windows/desktop/api/p2p/ns-p2p-peer_graph_event_data">PEER_GRAPH_EVENT_DATA</a>



<a href="/windows/desktop/api/p2p/ns-p2p-peer_graph_event_registration">PEER_GRAPH_EVENT_REGISTRATION</a>



<a href="/windows/desktop/api/p2p/nf-p2p-peergraphconnect">PeerGraphConnect</a>



<a href="/windows/desktop/api/p2p/nf-p2p-peergraphgetproperties">PeerGraphGetProperties</a>
