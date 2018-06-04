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

# MF_TOPOLOGY_TYPE enumeration


## -description



Defines the type of a topology node.




## -enum-fields




### -field MF_TOPOLOGY_OUTPUT_NODE

Output node. Represents a media sink in the topology.


### -field MF_TOPOLOGY_SOURCESTREAM_NODE

Source node. Represents a media stream in the topology.


### -field MF_TOPOLOGY_TRANSFORM_NODE

Transform node. Represents a Media Foundation Transform (MFT) in the topology.


### -field MF_TOPOLOGY_TEE_NODE

Tee node. A tee node does not hold a pointer to an object. Instead, it represents a fork in the stream. A tee node has one input and multiple outputs, and samples from the upstream node are delivered to all of the downstream nodes.


### -field MF_TOPOLOGY_MAX

Reserved.


## -see-also




<a href="https://msdn.microsoft.com/f26a730f-18c4-4247-acaf-af1dfad19086">Media Foundation Enumerations</a>
 

 

