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

# D2D1_HIGHLIGHTSANDSHADOWS_PROP enumeration


## -description


Identifiers for properties of the <a href="https://msdn.microsoft.com/ebbb7d99-9144-ffff-af73-d89e7d269924">Highlights and Shadows effect</a>.


## -enum-fields




### -field D2D1_HIGHLIGHTSANDSHADOWS_PROP_HIGHLIGHTS

The D2D1_HIGHLIGHTSANDSHADOWS_PROP_HIGHLIGHTS property is a float value indicating how much to increase or decrease highlights.  The allowed range is -1.0 to 1.0. The default value is 0.0.


### -field D2D1_HIGHLIGHTSANDSHADOWS_PROP_SHADOWS

The D2D1_HIGHLIGHTSANDSHADOWS_PROP_SHADOWS property is a float value indicating how much to increase or decrease shadows.  The allowed range is -1.0 to 1.0. The default value is 0.0.


### -field D2D1_HIGHLIGHTSANDSHADOWS_PROP_CLARITY

The D2D1_HIGHLIGHTSANDSHADOWS_PROP_CLARITY property is a float value indicating how much to increase or decrease clarity.  The allowed range is -1.0 to 1.0. The default value is 0.0.


### -field D2D1_HIGHLIGHTSANDSHADOWS_PROP_INPUT_GAMMA

The D2D1_HIGHLIGHTSANDSHADOWS_PROP_INPUT_GAMMA property is a <a href="https://msdn.microsoft.com/F56C9933-B340-4E8B-85BE-CE04E90C9ADC">D2D1_HIGHLIGHTSANDSHADOWS_INPUT_GAMMA</a> enumeration value
          indicating the gamma of the input image.  The Highlights and Shadows effect works in linear gamma space, so if the input image is know to be linear, the D2D1_HIGHLIGHTSANDSHADOWS_INPUT_GAMMA_LINEAR value should be used to prevent sRGB to linear conversions from being performed.


### -field D2D1_HIGHLIGHTSANDSHADOWS_PROP_MASK_BLUR_RADIUS

The D2D1_HIGHLIGHTSANDSHADOWS_PROP_MASK_BLUR_RADIUS property is a float value controlling the size of the region used around a pixel to classify the pixel as highlight or shadow. Lower values result in more localized adjustments. 
          The allowed range is 0.0 to 10.0.  The default value is 1.25.


### -field D2D1_HIGHLIGHTSANDSHADOWS_PROP_FORCE_DWORD



