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

# peer_event_node_change_data_tag structure


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




<a href="https://msdn.microsoft.com/a052bff8-e90c-4ff7-8362-edb94b130f38">PEER_GRAPH_EVENT_DATA</a>
 

 

