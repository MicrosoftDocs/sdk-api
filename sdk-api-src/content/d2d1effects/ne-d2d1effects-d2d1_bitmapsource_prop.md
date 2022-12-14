---
UID: NE:d2d1effects.D2D1_BITMAPSOURCE_PROP
title: D2D1_BITMAPSOURCE_PROP (d2d1effects.h)
description: Identifiers for properties of the Bitmap source effect.
helpviewer_keywords: ["D2D1_BITMAPSOURCE_PROP","D2D1_BITMAPSOURCE_PROP enumeration [Direct2D]","D2D1_BITMAPSOURCE_PROP_ALPHA_MODE","D2D1_BITMAPSOURCE_PROP_ENABLE_DPI_CORRECTION","D2D1_BITMAPSOURCE_PROP_INTERPOLATION_MODE","D2D1_BITMAPSOURCE_PROP_ORIENTATION","D2D1_BITMAPSOURCE_PROP_SCALE","D2D1_BITMAPSOURCE_PROP_WIC_BITMAP_SOURCE","d2d1effects/D2D1_BITMAPSOURCE_PROP","d2d1effects/D2D1_BITMAPSOURCE_PROP_ALPHA_MODE","d2d1effects/D2D1_BITMAPSOURCE_PROP_ENABLE_DPI_CORRECTION","d2d1effects/D2D1_BITMAPSOURCE_PROP_INTERPOLATION_MODE","d2d1effects/D2D1_BITMAPSOURCE_PROP_ORIENTATION","d2d1effects/D2D1_BITMAPSOURCE_PROP_SCALE","d2d1effects/D2D1_BITMAPSOURCE_PROP_WIC_BITMAP_SOURCE","direct2d.d2d1_bitmapsource_prop"]
old-location: direct2d\d2d1_bitmapsource_prop.htm
tech.root: Direct2D
ms.assetid: 02E1108D-FD73-4031-B709-5993D42D102F
ms.date: 12/05/2018
ms.keywords: D2D1_BITMAPSOURCE_PROP, D2D1_BITMAPSOURCE_PROP enumeration [Direct2D], D2D1_BITMAPSOURCE_PROP_ALPHA_MODE, D2D1_BITMAPSOURCE_PROP_ENABLE_DPI_CORRECTION, D2D1_BITMAPSOURCE_PROP_INTERPOLATION_MODE, D2D1_BITMAPSOURCE_PROP_ORIENTATION, D2D1_BITMAPSOURCE_PROP_SCALE, D2D1_BITMAPSOURCE_PROP_WIC_BITMAP_SOURCE, d2d1effects/D2D1_BITMAPSOURCE_PROP, d2d1effects/D2D1_BITMAPSOURCE_PROP_ALPHA_MODE, d2d1effects/D2D1_BITMAPSOURCE_PROP_ENABLE_DPI_CORRECTION, d2d1effects/D2D1_BITMAPSOURCE_PROP_INTERPOLATION_MODE, d2d1effects/D2D1_BITMAPSOURCE_PROP_ORIENTATION, d2d1effects/D2D1_BITMAPSOURCE_PROP_SCALE, d2d1effects/D2D1_BITMAPSOURCE_PROP_WIC_BITMAP_SOURCE, direct2d.d2d1_bitmapsource_prop
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
req.typenames: D2D1_BITMAPSOURCE_PROP
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D2D1_BITMAPSOURCE_PROP
 - d2d1effects/D2D1_BITMAPSOURCE_PROP
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
 - D2D1_BITMAPSOURCE_PROP
---

# D2D1_BITMAPSOURCE_PROP enumeration


## -description

Identifiers for properties of the <a href="/windows/desktop/Direct2D/bitmap-source">Bitmap source effect</a>.

## -enum-fields

### -field D2D1_BITMAPSOURCE_PROP_WIC_BITMAP_SOURCE:0

The IWICBitmapSource containing the image data to be loaded.
            

The type is IWICBitmapSource.

The default value is NULL.

### -field D2D1_BITMAPSOURCE_PROP_SCALE:1

The scale amount in the X and Y direction. The effect multiplies the width by the X value and the height by the Y value. 
          This property is a D2D1_VECTOR_2F defined as: (X scale, Y scale). The scale amounts are FLOAT, unitless, and must be positive or 0.
          

The type is D2D1_VECTOR_2F.

The default value is {1.0f, 1.0f}.

### -field D2D1_BITMAPSOURCE_PROP_INTERPOLATION_MODE:2

The interpolation mode used to scale the image.
          If the mode disables the mipmap, then BitmapSouce will cache the image at the resolution determined by the Scale and EnableDPICorrection properties.
          

The type is <a href="/windows/desktop/api/d2d1effects/ne-d2d1effects-d2d1_bitmapsource_interpolation_mode">D2D1_BITMAPSOURCE_INTERPOLATION_MODE</a>.

The default value is D2D1_BITMAPSOURCE_INTERPOLATION_MODE_LINEAR.

### -field D2D1_BITMAPSOURCE_PROP_ENABLE_DPI_CORRECTION:3

If you set this to TRUE, the effect will scale the input image to convert the DPI reported by IWICBitmapSource to the DPI of the device context. 
          The effect uses the interpolation mode you set with the InterpolationMode property. If you set this to FALSE, the effect uses a DPI of 96.0 for the output image.
          

The type is BOOL.

The default value is FALSE.

### -field D2D1_BITMAPSOURCE_PROP_ALPHA_MODE:4

The alpha mode of the output. This can be either premultiplied or straight.
          

The type is <a href="/windows/desktop/api/d2d1effects/ne-d2d1effects-d2d1_bitmapsource_alpha_mode">D2D1_BITMAPSOURCE_ALPHA_MODE</a>.

The default value is D2D1_BITMAPSOURCE_ALPHA_MODE_PREMULTIPLIED.

### -field D2D1_BITMAPSOURCE_PROP_ORIENTATION:5

A flip and/or rotation operation to be performed on the image.
          

The type is <a href="/windows/desktop/api/d2d1effects/ne-d2d1effects-d2d1_bitmapsource_orientation">D2D1_BITMAPSOURCE_ORIENTATION</a>.

The default value is D2D1_BITMAPSOURCE_ORIENTATION_DEFAULT.

### -field D2D1_BITMAPSOURCE_PROP_FORCE_DWORD:0xffffffff
