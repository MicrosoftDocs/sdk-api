---
UID: NE:d2d1effects.D2D1_ARITHMETICCOMPOSITE_PROP
title: D2D1_ARITHMETICCOMPOSITE_PROP (d2d1effects.h)
author: windows-sdk-content
description: Identifiers for the properties of the Arithmetic composite effect.
old-location: direct2d\d2d1_arithmeticcomposite_prop.htm
tech.root: Direct2D
ms.assetid: C3B1E6D9-2A8B-40C7-BE0C-C570F69C7DFB
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: D2D1_ARITHMETICCOMPOSITE_PROP, D2D1_ARITHMETICCOMPOSITE_PROP enumeration [Direct2D], D2D1_ARITHMETICCOMPOSITE_PROP_CLAMP_OUTPUT, D2D1_ARITHMETICCOMPOSITE_PROP_COEFFICIENTS, d2d1effects/D2D1_ARITHMETICCOMPOSITE_PROP, d2d1effects/D2D1_ARITHMETICCOMPOSITE_PROP_CLAMP_OUTPUT, d2d1effects/D2D1_ARITHMETICCOMPOSITE_PROP_COEFFICIENTS, direct2d.d2d1_arithmeticcomposite_prop
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
 - D2D1_ARITHMETICCOMPOSITE_PROP
product: Windows
targetos: Windows
req.typenames: D2D1_ARITHMETICCOMPOSITE_PROP
req.redist: 
---

# D2D1_ARITHMETICCOMPOSITE_PROP enumeration


## -description


Identifiers for the properties of the <a href="https://msdn.microsoft.com/6EC8CD61-5B51-4A8E-8A61-B291ABB5C5E0">Arithmetic composite effect</a>.
        


## -enum-fields




### -field D2D1_ARITHMETICCOMPOSITE_PROP_COEFFICIENTS

The coefficients for the equation used to composite the two input images. The coefficients are unitless and unbounded.
            

Type is D2D1_VECTOR_4F.

Default value is {1.0f, 0.0f, 0.0f, 0.0f}.


### -field D2D1_ARITHMETICCOMPOSITE_PROP_CLAMP_OUTPUT

The effect clamps color values to between 0 and 1 before the effect passes the values to the next effect in the graph.
            If you set this to TRUE the effect will clamp the values. If you set this to FALSE, the effect will not clamp the color values, 
            but other effects and the output surface may clamp the values if they are not of high enough precision.
            

Type is BOOL.

Default value is FALSE.


### -field D2D1_ARITHMETICCOMPOSITE_PROP_FORCE_DWORD



