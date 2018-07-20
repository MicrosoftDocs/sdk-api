---
UID: NS:p2p.peer_event_incoming_data_tag
title: peer_event_incoming_data_tag
author: windows-sdk-content
description: Points to the PEER_EVENT_INCOMING_DATA structure if one of the following peer events is triggered.
old-location: p2p\peer_event_incoming_data.htm
old-project: p2psdk
ms.assetid: 93104ca5-b3de-492c-965e-3acd12d05ea6
ms.author: windowssdkdev
ms.date: 07/17/2018
ms.keywords: "*PPEER_EVENT_INCOMING_DATA, PEER_EVENT_INCOMING_DATA, PEER_EVENT_INCOMING_DATA structure [Peer Networking], PPEER_EVENT_INCOMING_DATA, PPEER_EVENT_INCOMING_DATA structure pointer [Peer Networking], p2p.peer_event_incoming_data, p2p/PPEER_EVENT_INCOMING_DATA, p2p/peer_event_incoming_data_tag, peer_event_incoming_data_tag"
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
req.typenames: PEER_EVENT_INCOMING_DATA, *PPEER_EVENT_INCOMING_DATA
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - P2P.h
api_name:
 - PEER_EVENT_INCOMING_DATA
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# peer_event_incoming_data_tag structure


## -description


 The <a href="https://msdn.microsoft.com/a052bff8-e90c-4ff7-8362-edb94b130f38">PEER_GRAPH_EVENT_DATA</a> or <a href="https://msdn.microsoft.com/5cdae832-e6a7-481c-9784-1c1c07d689dd">PEER_GROUP_EVENT_DATA</a> structure points to the <b>PEER_EVENT_INCOMING_DATA</b> structure if one of the following peer events is triggered:
<ul>
<li><b>PEER_GRAPH_INCOMING_DATA</b></li>
<li><b>PEER_GROUP_INCOMING_DATA</b></li>
</ul>  The <b>PEER_EVENT_INCOMING_DATA</b> structure contains updated information that includes data  changes  a node receives from a neighbor or direct connection. 


## -struct-fields




### -field dwSize

Specifies the size of a structure.


### -field ullConnectionId

Specifies the unique ID of a data connection.


### -field type

Specifies the application-defined data type of  incoming data.


### -field data

Specifies the actual data received.


## -see-also




<a href="https://msdn.microsoft.com/d8a8b9e3-c455-4813-b812-263efe7f5e3e">PEER_DATA</a>



<a href="https://msdn.microsoft.com/a052bff8-e90c-4ff7-8362-edb94b130f38">PEER_GRAPH_EVENT_DATA</a>



<a href="https://msdn.microsoft.com/5cdae832-e6a7-481c-9784-1c1c07d689dd">PEER_GROUP_EVENT_DATA</a>
 

 

