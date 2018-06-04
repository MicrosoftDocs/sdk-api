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

# D2D1_DISPLACEMENTMAP_PROP enumeration


## -description



          Identifiers for properties of the <a href="https://msdn.microsoft.com/07AA64B1-B570-428E-924F-D7DF3E4DB3F8">Displacement map effect</a>.
        


## -enum-fields




### -field D2D1_DISPLACEMENTMAP_PROP_SCALE

Multiplies the intensity of the selected channel from the displacement image. The higher you set this property, the more the effect displaces the pixels.
            

The type is FLOAT.

The default value is 0.0f.


### -field D2D1_DISPLACEMENTMAP_PROP_X_CHANNEL_SELECT

The effect extracts the intensity from this color channel and uses it to spatially displace the image in the X direction.
          

The type is <a href="https://msdn.microsoft.com/92BC07F7-4CB5-487E-9AFB-255C8EF1C6BA">D2D1_CHANNEL_SELECTOR</a>.

The default value is D2D1_CHANNEL_SELECTOR_A


### -field D2D1_DISPLACEMENTMAP_PROP_Y_CHANNEL_SELECT

The effect extracts the intensity from this color channel and uses it to spatially displace the image in the Y direction.
          

The type is <a href="https://msdn.microsoft.com/92BC07F7-4CB5-487E-9AFB-255C8EF1C6BA">D2D1_CHANNEL_SELECTOR</a>.

The default value is D2D1_CHANNEL_SELECTOR_A


### -field D2D1_DISPLACEMENTMAP_PROP_FORCE_DWORD



