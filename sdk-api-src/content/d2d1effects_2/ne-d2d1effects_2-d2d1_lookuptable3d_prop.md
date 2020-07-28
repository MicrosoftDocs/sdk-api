---
UID: NE:d2d1effects_2.D2D1_LOOKUPTABLE3D_PROP
title: D2D1_LOOKUPTABLE3D_PROP (d2d1effects_2.h)
description: Identifiers for the properties of the 3D Lookup Table effect.
helpviewer_keywords: ["D2D1_LOOKUPTABLE3D_PROP","D2D1_LOOKUPTABLE3D_PROP enumeration [Direct2D]","D2D1_LOOKUPTABLE3D_PROP_ALPHA_MODE","D2D1_LOOKUPTABLE3D_PROP_LUT","d2d1effects_2/D2D1_LOOKUPTABLE3D_PROP","d2d1effects_2/D2D1_LOOKUPTABLE3D_PROP_ALPHA_MODE","d2d1effects_2/D2D1_LOOKUPTABLE3D_PROP_LUT","direct2d.d2d1_lookuptable3d_prop"]
old-location: direct2d\d2d1_lookuptable3d_prop.htm
tech.root: Direct2D
ms.assetid: A0F866CD-78FE-441E-810E-763347F84323
ms.date: 12/05/2018
ms.keywords: D2D1_LOOKUPTABLE3D_PROP, D2D1_LOOKUPTABLE3D_PROP enumeration [Direct2D], D2D1_LOOKUPTABLE3D_PROP_ALPHA_MODE, D2D1_LOOKUPTABLE3D_PROP_LUT, d2d1effects_2/D2D1_LOOKUPTABLE3D_PROP, d2d1effects_2/D2D1_LOOKUPTABLE3D_PROP_ALPHA_MODE, d2d1effects_2/D2D1_LOOKUPTABLE3D_PROP_LUT, direct2d.d2d1_lookuptable3d_prop
f1_keywords:
- d2d1effects_2/D2D1_LOOKUPTABLE3D_PROP
dev_langs:
- c++
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
- D2D1_LOOKUPTABLE3D_PROP
targetos: Windows
req.typenames: D2D1_LOOKUPTABLE3D_PROP
req.redist: 
ms.custom: 19H1
---

# D2D1_LOOKUPTABLE3D_PROP enumeration


## -description


Identifiers for the properties of the 3D Lookup Table effect.


## -enum-fields




### -field D2D1_LOOKUPTABLE3D_PROP_LUT

The D2D1_LOOKUPTABLE3D_PROP_LUT property is a pointer to an <a href="https://docs.microsoft.com/windows/desktop/api/d2d1_3/nn-d2d1_3-id2d1lookuptable3d">ID2D1LookupTable3D</a> object.  The default value is null.


### -field D2D1_LOOKUPTABLE3D_PROP_ALPHA_MODE

The D2D1_LOOKUPTABLE3D_PROP_ALPHA_MODE property is a <a href="https://docs.microsoft.com/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode">D2D1_ALPHA_MODE</a> value indicating the alpha mode of the input file.
          See the About Alpha Modes section of the <a href="https://docs.microsoft.com/windows/desktop/Direct2D/supported-pixel-formats-and-alpha-modes">Supported Pixel Formats and Alpha Modes</a> topic for additional information.


### -field D2D1_LOOKUPTABLE3D_PROP_FORCE_DWORD




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Direct2D/built-in-effects">Built-in Effects</a>



<a href="https://docs.microsoft.com/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createeffect">CreateEffect</a>
 

 

