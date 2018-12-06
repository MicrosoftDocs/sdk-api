---
UID: NE:d2d1effects.D2D1_GAUSSIANBLUR_PROP
title: D2D1_GAUSSIANBLUR_PROP
author: windows-sdk-content
description: Identifiers for properties of the Gaussian blur effect.
old-location: direct2d\d2d1_gaussianblur_prop.htm
tech.root: direct2d
ms.assetid: 0413E97C-1114-4EC4-955E-229BD39E15EA
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: D2D1_GAUSSIANBLUR_PROP, D2D1_GAUSSIANBLUR_PROP enumeration [Direct2D], D2D1_GAUSSIANBLUR_PROP_BORDER_MODE, D2D1_GAUSSIANBLUR_PROP_OPTIMIZATION, D2D1_GAUSSIANBLUR_PROP_STANDARD_DEVIATION, d2d1effects/D2D1_GAUSSIANBLUR_PROP, d2d1effects/D2D1_GAUSSIANBLUR_PROP_BORDER_MODE, d2d1effects/D2D1_GAUSSIANBLUR_PROP_OPTIMIZATION, d2d1effects/D2D1_GAUSSIANBLUR_PROP_STANDARD_DEVIATION, direct2d.d2d1_gaussianblur_prop
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: d2d1effects.h
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
 - d2d1effects.h
api_name:
 - D2D1_GAUSSIANBLUR_PROP
product: Windows
targetos: Windows
req.typenames: D2D1_GAUSSIANBLUR_PROP
req.redist: 
---

# D2D1_GAUSSIANBLUR_PROP enumeration


## -description


Identifiers for properties of the <a href="https://msdn.microsoft.com/6B8C9A0A-81D6-4CC2-B30B-995D4C2E59FC">Gaussian blur effect</a>.
        


## -enum-fields




### -field D2D1_GAUSSIANBLUR_PROP_STANDARD_DEVIATION

The amount of blur to be applied to the image. You can compute the blur radius of the kernel by multiplying the standard deviation by 3.
            The units of both the standard deviation and blur radius are DIPs. A value of zero DIPs disables this effect entirely.
            

The type is FLOAT.

The default value is 3.0f.


### -field D2D1_GAUSSIANBLUR_PROP_OPTIMIZATION

The optimization mode.
            

The type is <a href="https://msdn.microsoft.com/D6A8BB3A-8286-4410-8EA3-A9AEA1797C5E">D2D1_GAUSSIANBLUR_OPTIMIZATION</a>.

The default value is D2D1_GAUSSIANBLUR_OPTIMIZATION_BALANCED.


### -field D2D1_GAUSSIANBLUR_PROP_BORDER_MODE

The mode used to calculate the border of the image, soft or hard.
            

The type is <a href="https://msdn.microsoft.com/D6A8BB3A-8286-4410-8EA3-A9AEA1797C5E">D2D1_GAUSSIANBLUR_OPTIMIZATION</a>.

The default value is D2D1_BORDER_MODE_SOFT.


### -field D2D1_GAUSSIANBLUR_PROP_FORCE_DWORD



