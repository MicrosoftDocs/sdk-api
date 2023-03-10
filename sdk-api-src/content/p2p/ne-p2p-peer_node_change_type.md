---
UID: NE:p2p.peer_node_change_type_tag
title: PEER_NODE_CHANGE_TYPE (p2p.h)
description: The PEER_NODE_CHANGE_TYPE enumeration specifies the types of peer node graph status changes.
helpviewer_keywords: ["PEER_NODE_CHANGE_CONNECTED","PEER_NODE_CHANGE_DISCONNECTED","PEER_NODE_CHANGE_TYPE","PEER_NODE_CHANGE_TYPE enumeration [Peer Networking]","PEER_NODE_CHANGE_UPDATED","p2p.peer_node_change_type","p2p/PEER_NODE_CHANGE_CONNECTED","p2p/PEER_NODE_CHANGE_DISCONNECTED","p2p/PEER_NODE_CHANGE_TYPE","p2p/PEER_NODE_CHANGE_UPDATED"]
old-location: p2p\peer_node_change_type.htm
tech.root: p2p
ms.assetid: e14e432a-5edb-4bf1-9c64-e5ece5b9254e
ms.date: 12/05/2018
ms.keywords: PEER_NODE_CHANGE_CONNECTED, PEER_NODE_CHANGE_DISCONNECTED, PEER_NODE_CHANGE_TYPE, PEER_NODE_CHANGE_TYPE enumeration [Peer Networking], PEER_NODE_CHANGE_UPDATED, p2p.peer_node_change_type, p2p/PEER_NODE_CHANGE_CONNECTED, p2p/PEER_NODE_CHANGE_DISCONNECTED, p2p/PEER_NODE_CHANGE_TYPE, p2p/PEER_NODE_CHANGE_UPDATED
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
req.typenames: PEER_NODE_CHANGE_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - peer_node_change_type_tag
 - p2p/peer_node_change_type_tag
 - PEER_NODE_CHANGE_TYPE
 - p2p/PEER_NODE_CHANGE_TYPE
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
 - PEER_NODE_CHANGE_TYPE
---

# PEER_NODE_CHANGE_TYPE enumeration


## -description

The <b>PEER_NODE_CHANGE_TYPE</b> enumeration specifies the types of peer node graph status changes.

## -enum-fields

### -field PEER_NODE_CHANGE_CONNECTED:1

The peer node has connected to the graph.

### -field PEER_NODE_CHANGE_DISCONNECTED:2

The peer node has disconnected from the graph.

### -field PEER_NODE_CHANGE_UPDATED:3

The peer node's status within the graph has changed.

