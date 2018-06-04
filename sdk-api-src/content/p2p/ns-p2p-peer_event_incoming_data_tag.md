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
 

 

