---
UID: NE:d2d1effects_2.D2D1_VIGNETTE_PROP
title: D2D1_VIGNETTE_PROP
author: windows-sdk-content
description: Identifiers for properties of the Vignette effect.
old-location: direct2d\d2d1_vignette_prop.htm
tech.root: direct2d
ms.assetid: B45EFED7-97CA-41AF-9C36-4ECDCC153183
ms.author: windowssdkdev
ms.date: 10/17/2018
ms.keywords: D2D1_VIGNETTE_PROP, D2D1_VIGNETTE_PROP enumeration [Direct2D], D2D1_VIGNETTE_PROP_COLOR, D2D1_VIGNETTE_PROP_STRENGTH, D2D1_VIGNETTE_PROP_TRANSITION_SIZE, d2d1effects_2/D2D1_VIGNETTE_PROP, d2d1effects_2/D2D1_VIGNETTE_PROP_COLOR, d2d1effects_2/D2D1_VIGNETTE_PROP_STRENGTH, d2d1effects_2/D2D1_VIGNETTE_PROP_TRANSITION_SIZE, direct2d.d2d1_vignette_prop
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: d2d1effects_2.h
req.include-header: 
req.target-type: Windows
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d2d1effects_2.h
api_name:
 - D2D1_VIGNETTE_PROP
product: Windows
targetos: Windows
req.typenames: D2D1_VIGNETTE_PROP
req.redist: 
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



