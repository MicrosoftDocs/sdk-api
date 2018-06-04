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

# D2D1_VIGNETTE_PROP enumeration


## -description


Identifiers for properties of the <a href="https://msdn.microsoft.com/34da221f-44a2-1d01-d88d-d7846b9770b9">Vignette effect</a>.


## -enum-fields




### -field D2D1_VIGNETTE_PROP_COLOR

The D2D1_VIGNETTE_PROP_COLOR property is an RGB tripplet that specifies the color to fade the image's edges to. The default color is black.


### -field D2D1_VIGNETTE_PROP_TRANSITION_SIZE

The D2D1_VIGNETTE_PROP_TRANSITION_SIZE property is a float value that specifies the size of the vignette region as a percentage of the full image region.  
          A size of 0 means the unfaded region is the entire image, while a size of 1 means the faded region is the entire source image.
          The allowed range is 0.0 to 1.0.  The default value is 0.1.


### -field D2D1_VIGNETTE_PROP_STRENGTH

The D2D1_VIGNETTE_PROP_STRENGTH property is a float value that specifies how much the vignette color bleeds in for a given transition size. 
          The allowed range is 0.0 to 1.0.  The default value is 0.5.


### -field D2D1_VIGNETTE_PROP_FORCE_DWORD



