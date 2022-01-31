---
UID: NE:d2d1effects.D2D1_2DAFFINETRANSFORM_PROP
title: D2D1_2DAFFINETRANSFORM_PROP (d2d1effects.h)
description: Identifiers for properties of the 2D affine transform effect.
helpviewer_keywords: ["D2D1_2DAFFINETRANSFORM_PROP","D2D1_2DAFFINETRANSFORM_PROP enumeration [Direct2D]","D2D1_2DAFFINETRANSFORM_PROP_BORDER_MODE","D2D1_2DAFFINETRANSFORM_PROP_INTERPOLATION_MODE","D2D1_2DAFFINETRANSFORM_PROP_SHARPNESS","D2D1_2DAFFINETRANSFORM_PROP_TRANSFORM_MATRIX","d2d1effects/D2D1_2DAFFINETRANSFORM_PROP","d2d1effects/D2D1_2DAFFINETRANSFORM_PROP_BORDER_MODE","d2d1effects/D2D1_2DAFFINETRANSFORM_PROP_INTERPOLATION_MODE","d2d1effects/D2D1_2DAFFINETRANSFORM_PROP_SHARPNESS","d2d1effects/D2D1_2DAFFINETRANSFORM_PROP_TRANSFORM_MATRIX","direct2d.d2d1_2daffinetransform_prop"]
old-location: direct2d\d2d1_2daffinetransform_prop.htm
tech.root: Direct2D
ms.assetid: B1D8916F-124B-40BF-ABC5-78745D98DF97
ms.date: 12/05/2018
ms.keywords: D2D1_2DAFFINETRANSFORM_PROP, D2D1_2DAFFINETRANSFORM_PROP enumeration [Direct2D], D2D1_2DAFFINETRANSFORM_PROP_BORDER_MODE, D2D1_2DAFFINETRANSFORM_PROP_INTERPOLATION_MODE, D2D1_2DAFFINETRANSFORM_PROP_SHARPNESS, D2D1_2DAFFINETRANSFORM_PROP_TRANSFORM_MATRIX, d2d1effects/D2D1_2DAFFINETRANSFORM_PROP, d2d1effects/D2D1_2DAFFINETRANSFORM_PROP_BORDER_MODE, d2d1effects/D2D1_2DAFFINETRANSFORM_PROP_INTERPOLATION_MODE, d2d1effects/D2D1_2DAFFINETRANSFORM_PROP_SHARPNESS, d2d1effects/D2D1_2DAFFINETRANSFORM_PROP_TRANSFORM_MATRIX, direct2d.d2d1_2daffinetransform_prop
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
req.typenames: D2D1_2DAFFINETRANSFORM_PROP
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D2D1_2DAFFINETRANSFORM_PROP
 - d2d1effects/D2D1_2DAFFINETRANSFORM_PROP
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
 - D2D1_2DAFFINETRANSFORM_PROP
---

# D2D1_2DAFFINETRANSFORM_PROP enumeration


## -description

Identifiers for properties of the <a href="/windows/desktop/Direct2D/2d-affine-transform">2D affine transform effect</a>.

## -enum-fields

### -field D2D1_2DAFFINETRANSFORM_PROP_INTERPOLATION_MODE:0

The interpolation mode used to scale the image. There are 6 scale modes that range in quality and speed.
            

Type is <a href="/windows/desktop/api/d2d1effects/ne-d2d1effects-d2d1_2daffinetransform_interpolation_mode">D2D1_2DAFFINETRANSFORM_INTERPOLATION_MODE</a>.

Default value is D2D1_2DAFFINETRANSFORM_INTERPOLATION_MODE_LINEAR.

### -field D2D1_2DAFFINETRANSFORM_PROP_BORDER_MODE:1

The mode used to calculate the border of the image, soft or hard.
            

Type is <a href="/windows/desktop/api/d2d1effects/ne-d2d1effects-d2d1_border_mode">D2D1_BORDER_MODE</a>.

Default value is D2D1_BORDER_MODE_SOFT.

### -field D2D1_2DAFFINETRANSFORM_PROP_TRANSFORM_MATRIX:2

The 3x2 matrix to transform the image using the Direct2D matrix transform.
            

Type is <a href="/windows/desktop/Direct2D/d2d1-matrix-3x2-f">D2D1_MATRIX_3X2_F</a>.

Default value is Matrix3x2F::Identity().

### -field D2D1_2DAFFINETRANSFORM_PROP_SHARPNESS:3

In the high quality cubic interpolation mode, the sharpness level of the scaling filter as a float between 0 and 1. The values are unitless. You can use sharpness to adjust the quality of an image when you scale the image.
            The sharpness factor affects the shape of the kernel. The higher the sharpness factor, the smaller the kernel.
            

<div class="alert"><b>Note</b>  This property affects only the high quality cubic interpolation mode.</div>
<div> </div>
Type is FLOAT.

Default value is 1.0f.

### -field D2D1_2DAFFINETRANSFORM_PROP_FORCE_DWORD:0xffffffff
