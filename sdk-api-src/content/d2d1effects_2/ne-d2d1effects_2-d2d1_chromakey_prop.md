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

# D2D1_CHROMAKEY_PROP enumeration


## -description


Identifiers for properties of the <a href="https://msdn.microsoft.com/f7bb5c65-f406-f947-c05d-2756cff99d21">Chroma-key effect</a>.


## -enum-fields




### -field D2D1_CHROMAKEY_PROP_COLOR

The D2D1_CHROMAKEY_PROP_COLOR property is a vector4 value indicating the color that should be converted to alpha.  The default color is black.


### -field D2D1_CHROMAKEY_PROP_TOLERANCE

The D2D1_CHROMAKEY_PROP_TOLERANCE property is a float value indicating the tolerance for matching the color specified in the D2D1_CHROMAKEY_PROP_COLOR property.  
          The allowed range is 0.0 to 1.0.  The default value is 0.1.


### -field D2D1_CHROMAKEY_PROP_INVERT_ALPHA

The D2D1_CHROMAKEY_PROP_INVERT_ALPHA property is a boolean value indicating whether the alpha values should be inverted.  The default value if False.


### -field D2D1_CHROMAKEY_PROP_FEATHER

The D2D1_CHROMAKEY_PROP_FEATHER property is a boolean value whether the edges of the output should be softened in the alpha channel.
          When set to False, the alpha output by the effect is 1-bit: either fully opaque or fully transparent. Setting to True results in a softening of edges in the alpha channel of the Chroma Key output.
          The default value is False.


### -field D2D1_CHROMAKEY_PROP_FORCE_DWORD



