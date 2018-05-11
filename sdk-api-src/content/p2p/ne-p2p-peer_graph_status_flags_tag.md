---
UID: NE:p2p.peer_graph_status_flags_tag
title: peer_graph_status_flags_tag
author: windows-driver-content
description: The PEER_GRAPH_STATUS_FLAGS enumeration is a set of flags that show the current status of a node within the peer graph.
old-location: p2p\peer_graph_status_flags.htm
old-project: P2PSdk
ms.assetid: 71910437-4ebd-4fcc-977c-0a56c5f26d61
ms.author: windowsdriverdev
ms.date: 5/8/2018
ms.keywords: PEER_GRAPH_STATUS_FLAGS, PEER_GRAPH_STATUS_FLAGS enumeration [Peer Networking], PEER_GRAPH_STATUS_HAS_CONNECTIONS, PEER_GRAPH_STATUS_LISTENING, PEER_GRAPH_STATUS_SYNCHRONIZED, p2p.peer_graph_status_flags, p2p/ PEER_GRAPH_STATUS_FLAGS, p2p/PEER_GRAPH_STATUS_HAS_CONNECTIONS, p2p/PEER_GRAPH_STATUS_LISTENING, p2p/PEER_GRAPH_STATUS_SYNCHRONIZED, peer_graph_status_flags_tag
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: PEER_GRAPH_STATUS_FLAGS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	P2P.h
api_name:
-	PEER_GRAPH_STATUS_FLAGS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# peer_graph_status_flags_tag enumeration


## -description



      The <b>PEER_GRAPH_STATUS_FLAGS</b> enumeration is a set of flags that show the current status of a node within the peer graph.


## -enum-fields




### -field PEER_GRAPH_STATUS_LISTENING

Specifies whether or not the node is listening for connections.


### -field PEER_GRAPH_STATUS_HAS_CONNECTIONS

Specifies whether or not the node has connections to other nodes.


### -field PEER_GRAPH_STATUS_SYNCHRONIZED

Specifies whether or not the node's database is synchronized.


## -see-also




<a href="https://msdn.microsoft.com/a052bff8-e90c-4ff7-8362-edb94b130f38">
        PEER_GRAPH_EVENT_DATA</a>



<a href="https://msdn.microsoft.com/a7d23640-4f69-4ce0-996f-562807db7768">PeerGraphGetStatus</a>
 

 

