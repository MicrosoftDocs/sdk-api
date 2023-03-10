---
UID: NE:windows.graphics.effects.interop.GRAPHICS_EFFECT_PROPERTY_MAPPING
title: GRAPHICS_EFFECT_PROPERTY_MAPPING (windows.graphics.effects.interop.h)
description: Indicates how a strongly-typed effect property maps to an underlying Direct2D effect property.
helpviewer_keywords: ["GRAPHICS_EFFECT_PROPERTY_MAPPING","GRAPHICS_EFFECT_PROPERTY_MAPPING enumeration","GRAPHICS_EFFECT_PROPERTY_MAPPING_COLORMATRIX_ALPHA_MODE","GRAPHICS_EFFECT_PROPERTY_MAPPING_COLOR_TO_VECTOR3","GRAPHICS_EFFECT_PROPERTY_MAPPING_COLOR_TO_VECTOR4","GRAPHICS_EFFECT_PROPERTY_MAPPING_DIRECT","GRAPHICS_EFFECT_PROPERTY_MAPPING_RADIANS_TO_DEGREES","GRAPHICS_EFFECT_PROPERTY_MAPPING_RECT_TO_VECTOR4","GRAPHICS_EFFECT_PROPERTY_MAPPING_UNKNOWN","GRAPHICS_EFFECT_PROPERTY_MAPPING_VECTORW","GRAPHICS_EFFECT_PROPERTY_MAPPING_VECTORX","GRAPHICS_EFFECT_PROPERTY_MAPPING_VECTORY","GRAPHICS_EFFECT_PROPERTY_MAPPING_VECTORZ","w_graph_fx.graphics_effect_property_mapping","windows/GRAPHICS_EFFECT_PROPERTY_MAPPING","windows/GRAPHICS_EFFECT_PROPERTY_MAPPING_COLORMATRIX_ALPHA_MODE","windows/GRAPHICS_EFFECT_PROPERTY_MAPPING_COLOR_TO_VECTOR3","windows/GRAPHICS_EFFECT_PROPERTY_MAPPING_COLOR_TO_VECTOR4","windows/GRAPHICS_EFFECT_PROPERTY_MAPPING_DIRECT","windows/GRAPHICS_EFFECT_PROPERTY_MAPPING_RADIANS_TO_DEGREES","windows/GRAPHICS_EFFECT_PROPERTY_MAPPING_RECT_TO_VECTOR4","windows/GRAPHICS_EFFECT_PROPERTY_MAPPING_UNKNOWN","windows/GRAPHICS_EFFECT_PROPERTY_MAPPING_VECTORW","windows/GRAPHICS_EFFECT_PROPERTY_MAPPING_VECTORX","windows/GRAPHICS_EFFECT_PROPERTY_MAPPING_VECTORY","windows/GRAPHICS_EFFECT_PROPERTY_MAPPING_VECTORZ"]
old-location: w_graph_fx\graphics_effect_property_mapping.htm
tech.root: winrt
ms.assetid: FD18E84C-045D-42AC-A2C6-956DA12BFEA2
ms.date: 12/05/2018
ms.keywords: GRAPHICS_EFFECT_PROPERTY_MAPPING, GRAPHICS_EFFECT_PROPERTY_MAPPING enumeration, GRAPHICS_EFFECT_PROPERTY_MAPPING_COLORMATRIX_ALPHA_MODE, GRAPHICS_EFFECT_PROPERTY_MAPPING_COLOR_TO_VECTOR3, GRAPHICS_EFFECT_PROPERTY_MAPPING_COLOR_TO_VECTOR4, GRAPHICS_EFFECT_PROPERTY_MAPPING_DIRECT, GRAPHICS_EFFECT_PROPERTY_MAPPING_RADIANS_TO_DEGREES, GRAPHICS_EFFECT_PROPERTY_MAPPING_RECT_TO_VECTOR4, GRAPHICS_EFFECT_PROPERTY_MAPPING_UNKNOWN, GRAPHICS_EFFECT_PROPERTY_MAPPING_VECTORW, GRAPHICS_EFFECT_PROPERTY_MAPPING_VECTORX, GRAPHICS_EFFECT_PROPERTY_MAPPING_VECTORY, GRAPHICS_EFFECT_PROPERTY_MAPPING_VECTORZ, w_graph_fx.graphics_effect_property_mapping, windows/GRAPHICS_EFFECT_PROPERTY_MAPPING, windows/GRAPHICS_EFFECT_PROPERTY_MAPPING_COLORMATRIX_ALPHA_MODE, windows/GRAPHICS_EFFECT_PROPERTY_MAPPING_COLOR_TO_VECTOR3, windows/GRAPHICS_EFFECT_PROPERTY_MAPPING_COLOR_TO_VECTOR4, windows/GRAPHICS_EFFECT_PROPERTY_MAPPING_DIRECT, windows/GRAPHICS_EFFECT_PROPERTY_MAPPING_RADIANS_TO_DEGREES, windows/GRAPHICS_EFFECT_PROPERTY_MAPPING_RECT_TO_VECTOR4, windows/GRAPHICS_EFFECT_PROPERTY_MAPPING_UNKNOWN, windows/GRAPHICS_EFFECT_PROPERTY_MAPPING_VECTORW, windows/GRAPHICS_EFFECT_PROPERTY_MAPPING_VECTORX, windows/GRAPHICS_EFFECT_PROPERTY_MAPPING_VECTORY, windows/GRAPHICS_EFFECT_PROPERTY_MAPPING_VECTORZ
req.header: windows.graphics.effects.interop.h
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
targetos: Windows
req.typenames: GRAPHICS_EFFECT_PROPERTY_MAPPING
req.redist: 
ms.custom: 19H1
f1_keywords:
 - GRAPHICS_EFFECT_PROPERTY_MAPPING
 - windows.graphics.effects.interop/GRAPHICS_EFFECT_PROPERTY_MAPPING
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - windows.graphics.effects.interop.h
api_name:
 - GRAPHICS_EFFECT_PROPERTY_MAPPING
---

# GRAPHICS_EFFECT_PROPERTY_MAPPING enumeration


## -description

Indicates how a strongly-typed effect property maps to an underlying Direct2D effect property. This enumeration supports the Windows.UI.Composition API and is not meant to be used directly in your code.

## -enum-fields

### -field GRAPHICS_EFFECT_PROPERTY_MAPPING_UNKNOWN

Specifies that the value cannot be mapped to a Direct2D effect property.

### -field GRAPHICS_EFFECT_PROPERTY_MAPPING_DIRECT

Specifies that the value can be set as-is on the Direct2D effect property.

### -field GRAPHICS_EFFECT_PROPERTY_MAPPING_VECTORX

Specifies that the value maps to the X component of a vector-typed Direct2D effect property.

### -field GRAPHICS_EFFECT_PROPERTY_MAPPING_VECTORY

Specifies that the value maps to the Y component of a vector-typed Direct2D effect property.

### -field GRAPHICS_EFFECT_PROPERTY_MAPPING_VECTORZ

Specifies that the value maps to the Z component of a vector-typed Direct2D effect property.

### -field GRAPHICS_EFFECT_PROPERTY_MAPPING_VECTORW

Specifies that the value maps to the W component of a vector-typed Direct2D effect property.

### -field GRAPHICS_EFFECT_PROPERTY_MAPPING_RECT_TO_VECTOR4

Specifies that a rect value maps to a Vector4 Direct2D effect property.

### -field GRAPHICS_EFFECT_PROPERTY_MAPPING_RADIANS_TO_DEGREES

Specifies that the value needs to be converted from radians to degrees before being set on the Direct2D effect property.

### -field GRAPHICS_EFFECT_PROPERTY_MAPPING_COLORMATRIX_ALPHA_MODE

Specifies a color matrix alpha mode enum value needs to be converted to the equivalent Direct2D enum value before being set on the effect property.

### -field GRAPHICS_EFFECT_PROPERTY_MAPPING_COLOR_TO_VECTOR3

Specifies that a Windows.UI.Color value needs to be converted to an RGB Vector3 before being set on the Direct2D effect property.

### -field GRAPHICS_EFFECT_PROPERTY_MAPPING_COLOR_TO_VECTOR4

Specifies that a Windows.UI.Color value needs to be converted to an RGBA Vector4 before being set on the Direct2D effect property.

