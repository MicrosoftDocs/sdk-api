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

# peer_event_record_change_data_tag structure


## -description


The <a href="https://msdn.microsoft.com/a052bff8-e90c-4ff7-8362-edb94b130f38">PEER_GRAPH_EVENT_DATA</a> or <a href="https://msdn.microsoft.com/5cdae832-e6a7-481c-9784-1c1c07d689dd">PEER_GROUP_EVENT_DATA</a> structure points to the <b>PEER_EVENT_RECORD_CHANGE_DATA</b> structure if one of the following peer events is triggered:
<ul>
<li><b>PEER_GRAPH_EVENT_RECORD_CHANGE</b></li>
<li><b>PEER_GROUP_EVENT_RECORD_CHANGE</b></li>
</ul> The <b>PEER_EVENT_RECORD_CHANGE_DATA</b> structure contains updated information that an application requests for data  changes  to a record or record type. 


## -struct-fields




### -field dwSize

Specifies the size of a structure.


### -field changeType

Specifies the type of change to a record or record type.


### -field recordId

Specifies the unique  ID of a changed record.


### -field recordType

Specifies the unique  record type of a changed record.


## -see-also




<a href="https://msdn.microsoft.com/a052bff8-e90c-4ff7-8362-edb94b130f38">PEER_GRAPH_EVENT_DATA</a>



<a href="https://msdn.microsoft.com/5cdae832-e6a7-481c-9784-1c1c07d689dd">PEER_GROUP_EVENT_DATA</a>



<a href="https://msdn.microsoft.com/d2451b45-eb42-4401-ab1d-505a41e25822">PEER_RECORD_CHANGE_TYPE</a>
 

 

