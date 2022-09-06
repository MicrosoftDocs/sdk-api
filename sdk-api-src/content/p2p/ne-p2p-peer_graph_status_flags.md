---
UID: NE:p2p.peer_graph_status_flags_tag
title: PEER_GRAPH_STATUS_FLAGS (p2p.h)
description: The PEER_GRAPH_STATUS_FLAGS enumeration is a set of flags that show the current status of a node within the peer graph.
helpviewer_keywords: ["PEER_GRAPH_STATUS_FLAGS","PEER_GRAPH_STATUS_FLAGS enumeration [Peer Networking]","PEER_GRAPH_STATUS_HAS_CONNECTIONS","PEER_GRAPH_STATUS_LISTENING","PEER_GRAPH_STATUS_SYNCHRONIZED","p2p.peer_graph_status_flags","p2p/PEER_GRAPH_STATUS_FLAGS","p2p/PEER_GRAPH_STATUS_HAS_CONNECTIONS","p2p/PEER_GRAPH_STATUS_LISTENING","p2p/PEER_GRAPH_STATUS_SYNCHRONIZED"]
old-location: p2p\peer_graph_status_flags.htm
tech.root: p2p
ms.assetid: 71910437-4ebd-4fcc-977c-0a56c5f26d61
ms.date: 12/05/2018
ms.keywords: PEER_GRAPH_STATUS_FLAGS, PEER_GRAPH_STATUS_FLAGS enumeration [Peer Networking], PEER_GRAPH_STATUS_HAS_CONNECTIONS, PEER_GRAPH_STATUS_LISTENING, PEER_GRAPH_STATUS_SYNCHRONIZED, p2p.peer_graph_status_flags, p2p/PEER_GRAPH_STATUS_FLAGS, p2p/PEER_GRAPH_STATUS_HAS_CONNECTIONS, p2p/PEER_GRAPH_STATUS_LISTENING, p2p/PEER_GRAPH_STATUS_SYNCHRONIZED
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
req.typenames: PEER_GRAPH_STATUS_FLAGS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - peer_graph_status_flags_tag
 - p2p/peer_graph_status_flags_tag
 - PEER_GRAPH_STATUS_FLAGS
 - p2p/PEER_GRAPH_STATUS_FLAGS
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
 - PEER_GRAPH_STATUS_FLAGS
---

# PEER_GRAPH_STATUS_FLAGS enumeration


## -description

The <b>PEER_GRAPH_STATUS_FLAGS</b> enumeration is a set of flags that show the current status of a node within the peer graph.

## -enum-fields

### -field PEER_GRAPH_STATUS_LISTENING:0x0001

Specifies whether or not the node is listening for connections.

### -field PEER_GRAPH_STATUS_HAS_CONNECTIONS:0x0002

Specifies whether or not the node has connections to other nodes.

### -field PEER_GRAPH_STATUS_SYNCHRONIZED:0x0004

Specifies whether or not the node's database is synchronized.

## -see-also

<a href="/windows/desktop/api/p2p/ns-p2p-peer_graph_event_data">PEER_GRAPH_EVENT_DATA</a>



<a href="/windows/desktop/api/p2p/nf-p2p-peergraphgetstatus">PeerGraphGetStatus</a>
