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

# D2D1_LAYER_OPTIONS1 enumeration


## -description


Specifies how the layer contents should be prepared.



## -enum-fields




### -field D2D1_LAYER_OPTIONS1_NONE

Default layer behavior. A premultiplied layer target is pushed and its contents are cleared to transparent black. 



### -field D2D1_LAYER_OPTIONS1_INITIALIZE_FROM_BACKGROUND

	The layer is not cleared to transparent black.


### -field D2D1_LAYER_OPTIONS1_IGNORE_ALPHA

	The layer is always created as ignore alpha. All content rendered into the layer will be treated as opaque.


### -field D2D1_LAYER_OPTIONS1_FORCE_DWORD



