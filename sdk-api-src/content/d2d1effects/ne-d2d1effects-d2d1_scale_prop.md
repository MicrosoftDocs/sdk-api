---
UID: NE:d2d1effects.D2D1_SCALE_PROP
title: D2D1_SCALE_PROP (d2d1effects.h)
description: Identifiers for properties of the Scale effect.
helpviewer_keywords: ["D2D1_SCALE_PROP","D2D1_SCALE_PROP enumeration [Direct2D]","D2D1_SCALE_PROP_BORDER_MODE","D2D1_SCALE_PROP_CENTER_POINT","D2D1_SCALE_PROP_INTERPOLATION_MODE","D2D1_SCALE_PROP_SCALE","D2D1_SCALE_PROP_SHARPNESS","d2d1effects/D2D1_SCALE_PROP","d2d1effects/D2D1_SCALE_PROP_BORDER_MODE","d2d1effects/D2D1_SCALE_PROP_CENTER_POINT","d2d1effects/D2D1_SCALE_PROP_INTERPOLATION_MODE","d2d1effects/D2D1_SCALE_PROP_SCALE","d2d1effects/D2D1_SCALE_PROP_SHARPNESS","direct2d.d2d1_scale_prop"]
old-location: direct2d\d2d1_scale_prop.htm
tech.root: Direct2D
ms.assetid: 0FBAC940-3E73-4672-AFD7-F29459849592
ms.date: 12/05/2018
ms.keywords: D2D1_SCALE_PROP, D2D1_SCALE_PROP enumeration [Direct2D], D2D1_SCALE_PROP_BORDER_MODE, D2D1_SCALE_PROP_CENTER_POINT, D2D1_SCALE_PROP_INTERPOLATION_MODE, D2D1_SCALE_PROP_SCALE, D2D1_SCALE_PROP_SHARPNESS, d2d1effects/D2D1_SCALE_PROP, d2d1effects/D2D1_SCALE_PROP_BORDER_MODE, d2d1effects/D2D1_SCALE_PROP_CENTER_POINT, d2d1effects/D2D1_SCALE_PROP_INTERPOLATION_MODE, d2d1effects/D2D1_SCALE_PROP_SCALE, d2d1effects/D2D1_SCALE_PROP_SHARPNESS, direct2d.d2d1_scale_prop
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
targetos: Windows
req.typenames: D2D1_SCALE_PROP
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D2D1_SCALE_PROP
 - d2d1effects/D2D1_SCALE_PROP
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d2d1effects.h
api_name:
 - D2D1_SCALE_PROP
---

# D2D1_SCALE_PROP enumeration


## -description

Identifiers for properties of the <a href="/windows/desktop/Direct2D/high-quality-scale">Scale effect</a>.

## -enum-fields

### -field D2D1_SCALE_PROP_SCALE:0

The scale amount in the X and Y direction as a ratio of the output size to the input size.
            

This property a <a href="/windows/desktop/api/dcommon/ns-dcommon-d2d_vector_2f">D2D1_VECTOR_2F</a> defined as: (X scale, Y scale). 
            The scale amounts are FLOAT, unitless, and must be positive or 0.

The type is <a href="/windows/desktop/api/dcommon/ns-dcommon-d2d_vector_2f">D2D1_VECTOR_2F</a>.

The default value is {1.0f, 1.0f}.

### -field D2D1_SCALE_PROP_CENTER_POINT:1

The image scaling center point. This property is a <a href="/windows/desktop/api/dcommon/ns-dcommon-d2d_vector_2f">D2D1_VECTOR_2F</a> defined as: (point X, point Y). The units are in DIPs.
            

Use the center point property to scale around a point other than the upper-left corner.

The type is <a href="/windows/desktop/api/dcommon/ns-dcommon-d2d_vector_2f">D2D1_VECTOR_2F</a>.

The default value is {0.0f, 0.0f}.

### -field D2D1_SCALE_PROP_INTERPOLATION_MODE:2

The interpolation mode the effect uses to scale the image. There are 6 scale modes that range in quality and speed.
            

The type is <a href="/windows/desktop/api/d2d1effects/ne-d2d1effects-d2d1_scale_interpolation_mode">D2D1_SCALE_INTERPOLATION_MODE</a>.

The default value is D2D1_SCALE_INTERPOLATION_MODE_LINEAR.

### -field D2D1_SCALE_PROP_BORDER_MODE:3

The mode used to calculate the border of the image, soft or hard. 
            

The type is <a href="/windows/desktop/api/d2d1effects/ne-d2d1effects-d2d1_border_mode">D2D1_BORDER_MODE</a>.

The default value is D2D1_BORDER_MODE_SOFT.

### -field D2D1_SCALE_PROP_SHARPNESS:4

In the high quality cubic interpolation mode, the sharpness level of the scaling filter as a float between 0 and 1. The values are unitless. 
            You can use sharpness to adjust the quality of an image when you scale the image down.
            

The sharpness factor affects the shape of the kernel. The higher the sharpness factor, the smaller the kernel.

<div class="alert"><b>Note</b>  This property affects only the high quality cubic interpolation mode.</div>
<div> </div>
The type is FLOAT.

The default value is 0.0f.

### -field D2D1_SCALE_PROP_FORCE_DWORD:0xffffffff
