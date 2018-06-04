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

# D2D1_MORPHOLOGY_PROP enumeration


## -description



          Identifiers for properties of the <a href="https://msdn.microsoft.com/4B3CFC51-D556-4729-B433-7307C80291F4">Morphology effect</a>.
        


## -enum-fields




### -field D2D1_MORPHOLOGY_PROP_MODE


            The morphology mode.
            

The type is D2D1_MORPHOLOGY_MODE.

The default value is D2D1_MORPHOLOGY_MODE_ERODE.


### -field D2D1_MORPHOLOGY_PROP_WIDTH


            Size of the kernel in the X direction. The units are in DIPs. Values must be between 1 and 100 inclusive.
            

The type is UINT.

The default value is 1.


### -field D2D1_MORPHOLOGY_PROP_HEIGHT


            Size of the kernel in the Y direction. The units are in DIPs. Values must be between 1 and 100 inclusive.
            

The type is UINT.

The default value is 1.


### -field D2D1_MORPHOLOGY_PROP_FORCE_DWORD



