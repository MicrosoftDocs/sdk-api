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
 

 

