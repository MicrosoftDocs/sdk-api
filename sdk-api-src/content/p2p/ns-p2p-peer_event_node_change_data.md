---
UID: NS:p2p.peer_event_node_change_data_tag
title: PEER_EVENT_NODE_CHANGE_DATA (p2p.h)
description: The PEER_EVENT_NODE_CHANGE_DATA structure contains a pointer to the data if a PEER_GRAPH_EVENT_NODE_CHANGE event is triggered.
helpviewer_keywords: ["*PPEER_EVENT_NODE_CHANGE_DATA","PEER_EVENT_NODE_CHANGE_DATA","PEER_EVENT_NODE_CHANGE_DATA structure [Peer Networking]","PEER_NODE_CHANGE_CONNECTED","PEER_NODE_CHANGE_DISCONNECTED","PEER_NODE_CHANGE_UPDATED","PPEER_EVENT_NODE_CHANGE_DATA","PPEER_EVENT_NODE_CHANGE_DATA structure pointer [Peer Networking]","p2p.peer_event_node_change_data","p2p/PPEER_EVENT_NODE_CHANGE_DATA","p2p/peer_event_node_change_data_tag"]
old-location: p2p\peer_event_node_change_data.htm
tech.root: p2p
ms.assetid: 656c9155-643d-4c94-9141-3499f7e0adac
ms.date: 12/05/2018
ms.keywords: '*PPEER_EVENT_NODE_CHANGE_DATA, PEER_EVENT_NODE_CHANGE_DATA, PEER_EVENT_NODE_CHANGE_DATA structure [Peer Networking], PEER_NODE_CHANGE_CONNECTED, PEER_NODE_CHANGE_DISCONNECTED, PEER_NODE_CHANGE_UPDATED, PPEER_EVENT_NODE_CHANGE_DATA, PPEER_EVENT_NODE_CHANGE_DATA structure pointer [Peer Networking], p2p.peer_event_node_change_data, p2p/PPEER_EVENT_NODE_CHANGE_DATA, p2p/peer_event_node_change_data_tag'
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
req.typenames: PEER_EVENT_NODE_CHANGE_DATA, *PPEER_EVENT_NODE_CHANGE_DATA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - peer_event_node_change_data_tag
 - p2p/peer_event_node_change_data_tag
 - PPEER_EVENT_NODE_CHANGE_DATA
 - p2p/PPEER_EVENT_NODE_CHANGE_DATA
 - PEER_EVENT_NODE_CHANGE_DATA
 - p2p/PEER_EVENT_NODE_CHANGE_DATA
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
 - PEER_EVENT_NODE_CHANGE_DATA
---

# PEER_EVENT_NODE_CHANGE_DATA structure


## -description

The <b>PEER_EVENT_NODE_CHANGE_DATA</b> structure contains a pointer to the data if a <b>PEER_GRAPH_EVENT_NODE_CHANGE</b> event is triggered.

## -struct-fields

### -field dwSize

Specifies the size of the structure. Should  set to the size of PEER_EVENT_NODE_CHANGE_DATA.

### -field changeType

Specifies the  new  state of the node. Valid values are the following.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="PEER_NODE_CHANGE_CONNECTED"></a><a id="peer_node_change_connected"></a><dl>
<dt><b>PEER_NODE_CHANGE_CONNECTED</b></dt>
</dl>
</td>
<td width="60%">
The node is present in the graph.

</td>
</tr>
<tr>
<td width="40%"><a id="PEER_NODE_CHANGE_DISCONNECTED"></a><a id="peer_node_change_disconnected"></a><dl>
<dt><b>PEER_NODE_CHANGE_DISCONNECTED</b></dt>
</dl>
</td>
<td width="60%">
The node is no longer present in the graph.

</td>
</tr>
<tr>
<td width="40%"><a id="PEER_NODE_CHANGE_UPDATED"></a><a id="peer_node_change_updated"></a><dl>
<dt><b>PEER_NODE_CHANGE_UPDATED</b></dt>
</dl>
</td>
<td width="60%">
The node has new information, for example, the attributes have changed.

</td>
</tr>
</table>

### -field ullNodeId

Specifies the  unique ID of the node that has changed.

### -field pwzPeerId

Specifies the peer ID of the node that has  changed.

## -see-also

[PEER_GRAPH_EVENT_DATA](./ns-p2p-peer_graph_event_data.md)