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

# D2D1_CHANGE_TYPE enumeration


## -description


Describes flags that influence how the renderer interacts with a custom vertex shader.


## -enum-fields




### -field D2D1_CHANGE_TYPE_NONE

There were no changes.


### -field D2D1_CHANGE_TYPE_PROPERTIES

The properties of the effect changed.


### -field D2D1_CHANGE_TYPE_CONTEXT

The context state changed.


### -field D2D1_CHANGE_TYPE_GRAPH

The effect’s transform graph has changed.  This happens only when an effect supports a variable input count.


### -field D2D1_CHANGE_TYPE_FORCE_DWORD




## -see-also




<a href="https://msdn.microsoft.com/0EBA4FDB-A9EA-4FCF-BF40-3D73ED356CD4">ID2D1EffectImpl::PrepareForRender</a>
 

 

