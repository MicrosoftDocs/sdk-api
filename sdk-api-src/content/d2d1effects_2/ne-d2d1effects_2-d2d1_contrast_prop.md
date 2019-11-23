---
UID: NE:d2d1effects_2.D2D1_CONTRAST_PROP
title: D2D1_CONTRAST_PROP (d2d1effects_2.h)

description: Identifiers for properties of the Contrast effect.
old-location: direct2d\d2d1_contrast_prop.htm
tech.root: Direct2D
ms.assetid: 04215468-F6AA-4AA4-8F03-4858CE57FC14

ms.date: 12/05/2018
ms.keywords: D2D1_CONTRAST_PROP, D2D1_CONTRAST_PROP enumeration [Direct2D], D2D1_CONTRAST_PROP_CLAMP_INPUT, D2D1_CONTRAST_PROP_CONTRAST, d2d1effects_2/D2D1_CONTRAST_PROP, d2d1effects_2/D2D1_CONTRAST_PROP_CLAMP_INPUT, d2d1effects_2/D2D1_CONTRAST_PROP_CONTRAST, direct2d.d2d1_contrast_prop
ms.topic: enum
f1_keywords: 
 - "d2d1effects_2/D2D1_CONTRAST_PROP"
dev_langs:
 - c++
req.header: d2d1effects_2.h
req.include-header: D2d1_effects_2.h
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
 - D2D1_CONTRAST_PROP
targetos: Windows
req.typenames: D2D1_CONTRAST_PROP
req.redist: 
ms.custom: 19H1
---

# D2D1_CONTRAST_PROP enumeration


## -description


Identifiers for properties of the <a href="https://docs.microsoft.com/windows/desktop/Direct2D/contrast-effect">Contrast effect</a>.


## -enum-fields




### -field D2D1_CONTRAST_PROP_CONTRAST

The D2D1_CONTRAST_PROP_CONTRAST property is a float value indicating the amount by which to adjust the contrast of the image. Negative values reduce contrast, while positive values increase contrast.  
          Minimum value is -1.0f, maximum value is 1.0f.  The default value for the property is 0.0f.


### -field D2D1_CONTRAST_PROP_CLAMP_INPUT

The D2D1_CONTRAST_PROP_CLAMP_INPUT property is a boolean value indicating whether or not to clamp the input to [0.0, 1.0]. The default value for the property is FALSE.


### -field D2D1_CONTRAST_PROP_FORCE_DWORD




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Direct2D/built-in-effects">Built-in Effects</a>



<a href="https://docs.microsoft.com/windows/desktop/Direct2D/contrast-effect">Contrast effect</a>



<a href="https://docs.microsoft.com/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createeffect">CreateEffect</a>
 

 

