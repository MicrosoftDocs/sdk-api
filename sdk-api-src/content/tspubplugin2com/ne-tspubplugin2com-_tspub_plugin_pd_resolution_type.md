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

# _TSPUB_PLUGIN_PD_RESOLUTION_TYPE enumeration


## -description


Specifies the type of personal desktop resolution being requested.


## -enum-fields




### -field TSPUB_PLUGIN_PD_QUERY_OR_CREATE

Resolve an existing personal desktop for the user. If no personal desktop exists, the <a href="https://msdn.microsoft.com/1f88d7a6-c662-4a14-a288-9c346c8fb7f1">ResolvePersonalDesktop</a> method should create a new one.


### -field TSPUB_PLUGIN_PD_QUERY_EXISTING

Resolve an existing personal desktop for the user. If no personal desktop exists, the <a href="https://msdn.microsoft.com/1f88d7a6-c662-4a14-a288-9c346c8fb7f1">ResolvePersonalDesktop</a> method should return an error code.


## -see-also




<a href="https://msdn.microsoft.com/1f88d7a6-c662-4a14-a288-9c346c8fb7f1">ResolvePersonalDesktop</a>
 

 

