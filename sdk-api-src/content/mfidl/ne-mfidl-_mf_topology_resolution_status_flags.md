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

# _MF_TOPOLOGY_RESOLUTION_STATUS_FLAGS enumeration


## -description



Defines status flags for the <a href="https://msdn.microsoft.com/7c2410ce-e70b-4303-9dbc-caff4a355d6b">MF_TOPOLOGY_RESOLUTION_STATUS</a> attribute.




## -enum-fields




### -field MF_TOPOLOGY_RESOLUTION_SUCCEEDED

The topology was resolved successfully.


### -field MF_OPTIONAL_NODE_REJECTED_MEDIA_TYPE

An optional topology node was rejected because the topology loader could not find a media type for the connection.


### -field MF_OPTIONAL_NODE_REJECTED_PROTECTED_PROCESS

An optional topology node was rejected because it could not be loaded into a protected process.


## -see-also




<a href="https://msdn.microsoft.com/f26a730f-18c4-4247-acaf-af1dfad19086">Media Foundation Enumerations</a>
 

 

