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

# peer_event_synchronized_data_tag structure


## -description


The <b>PEER_EVENT_SYNCHRONIZED_DATA</b> is pointed to by a <a href="https://msdn.microsoft.com/a052bff8-e90c-4ff7-8362-edb94b130f38">PEER_GRAPH_EVENT_DATA</a> structure's union if a PEER_GRAPH_EVENT_RECORD_CHANGE or  PEER_GROUP_EVENT_RECORD_CHANGE event is triggered. The <b>PEER_EVENT_SYNCHRONIZED_DATA</b> structure indicates the type of record that has been synchronized.


## -struct-fields




### -field dwSize

Specifies the size of the structure.


### -field recordType

Specifies the type of record that is being synchronized.


## -remarks



This event only occurs if an application has specified a record synchronization precedence in a previous call to <a href="https://msdn.microsoft.com/a34656f1-3e29-4bcb-a8a7-0eed19368184">PeerGraphOpen</a>.




## -see-also




<a href="https://msdn.microsoft.com/a052bff8-e90c-4ff7-8362-edb94b130f38">PEER_GRAPH_EVENT_DATA</a>
 

 

