---
UID: NE:p2p.peer_graph_property_flags_tag
title: PEER_GRAPH_PROPERTY_FLAGS (p2p.h)
description: The PEER_GRAPH_PROPERTY_FLAGS enumeration specifies properties of a peer graph.
helpviewer_keywords: ["PEER_GRAPH_PROPERTY_DEFER_EXPIRATION","PEER_GRAPH_PROPERTY_FLAGS","PEER_GRAPH_PROPERTY_FLAGS enumeration [Peer Networking]","PEER_GRAPH_PROPERTY_HEARTBEATS","p2p.peer_graph_property_flags","p2p/PEER_GRAPH_PROPERTY_DEFER_EXPIRATION","p2p/PEER_GRAPH_PROPERTY_FLAGS","p2p/PEER_GRAPH_PROPERTY_HEARTBEATS"]
old-location: p2p\peer_graph_property_flags.htm
tech.root: p2p
ms.assetid: 0e4f273f-7b6f-4aac-8fee-c0295479ee78
ms.date: 12/05/2018
ms.keywords: PEER_GRAPH_PROPERTY_DEFER_EXPIRATION, PEER_GRAPH_PROPERTY_FLAGS, PEER_GRAPH_PROPERTY_FLAGS enumeration [Peer Networking], PEER_GRAPH_PROPERTY_HEARTBEATS, p2p.peer_graph_property_flags, p2p/PEER_GRAPH_PROPERTY_DEFER_EXPIRATION, p2p/PEER_GRAPH_PROPERTY_FLAGS, p2p/PEER_GRAPH_PROPERTY_HEARTBEATS
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
req.typenames: PEER_GRAPH_PROPERTY_FLAGS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - peer_graph_property_flags_tag
 - p2p/peer_graph_property_flags_tag
 - PEER_GRAPH_PROPERTY_FLAGS
 - p2p/PEER_GRAPH_PROPERTY_FLAGS
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
 - PEER_GRAPH_PROPERTY_FLAGS
---

# PEER_GRAPH_PROPERTY_FLAGS enumeration


## -description

The <b>PEER_GRAPH_PROPERTY_FLAGS</b> enumeration specifies properties of a peer graph.

## -enum-fields

### -field PEER_GRAPH_PROPERTY_HEARTBEATS:0x0001

Reserved.

### -field PEER_GRAPH_PROPERTY_DEFER_EXPIRATION:0x0002

Graph records are not expired until the peer  connects with a graph.

