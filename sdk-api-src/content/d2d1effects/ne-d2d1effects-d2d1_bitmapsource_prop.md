---
UID: NE:d2d1effects.D2D1_BITMAPSOURCE_PROP
title: D2D1_BITMAPSOURCE_PROP
author: windows-sdk-content
description: Identifiers for properties of the Bitmap source effect.
old-location: direct2d\d2d1_bitmapsource_prop.htm
tech.root: direct2d
ms.assetid: 02E1108D-FD73-4031-B709-5993D42D102F
ms.author: windowssdkdev
ms.date: 11/13/2018
ms.keywords: D2D1_BITMAPSOURCE_PROP, D2D1_BITMAPSOURCE_PROP enumeration [Direct2D], D2D1_BITMAPSOURCE_PROP_ALPHA_MODE, D2D1_BITMAPSOURCE_PROP_ENABLE_DPI_CORRECTION, D2D1_BITMAPSOURCE_PROP_INTERPOLATION_MODE, D2D1_BITMAPSOURCE_PROP_ORIENTATION, D2D1_BITMAPSOURCE_PROP_SCALE, D2D1_BITMAPSOURCE_PROP_WIC_BITMAP_SOURCE, d2d1effects/D2D1_BITMAPSOURCE_PROP, d2d1effects/D2D1_BITMAPSOURCE_PROP_ALPHA_MODE, d2d1effects/D2D1_BITMAPSOURCE_PROP_ENABLE_DPI_CORRECTION, d2d1effects/D2D1_BITMAPSOURCE_PROP_INTERPOLATION_MODE, d2d1effects/D2D1_BITMAPSOURCE_PROP_ORIENTATION, d2d1effects/D2D1_BITMAPSOURCE_PROP_SCALE, d2d1effects/D2D1_BITMAPSOURCE_PROP_WIC_BITMAP_SOURCE, direct2d.d2d1_bitmapsource_prop
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
 - D2D1_BITMAPSOURCE_PROP
product: Windows
targetos: Windows
req.typenames: D2D1_BITMAPSOURCE_PROP
req.redist: 
---

# D2D1_BITMAPSOURCE_PROP enumeration


## -description


Identifiers for properties of the <a href="https://msdn.microsoft.com/86646111-208A-4E6D-A28C-7B23A1742D24">Bitmap source effect</a>.
        


## -enum-fields




### -field D2D1_BITMAPSOURCE_PROP_WIC_BITMAP_SOURCE

The IWICBitmapSource containing the image data to be loaded.
            

The type is IWICBitmapSource.

The default value is NULL.


### -field D2D1_BITMAPSOURCE_PROP_SCALE

The scale amount in the X and Y direction. The effect multiplies the width by the X value and the height by the Y value. 
          This property is a D2D1_VECTOR_2F defined as: (X scale, Y scale). The scale amounts are FLOAT, unitless, and must be positive or 0.
          

The type is D2D1_VECTOR_2F.

The default value is {1.0f, 1.0f}.


### -field D2D1_BITMAPSOURCE_PROP_INTERPOLATION_MODE

The interpolation mode used to scale the image.
          If the mode disables the mipmap, then BitmapSouce will cache the image at the resolution determined by the Scale and EnableDPICorrection properties.
          

The type is <a href="https://msdn.microsoft.com/2912E2FA-4B1D-43FF-9684-22C3B2720395">D2D1_BITMAPSOURCE_INTERPOLATION_MODE</a>.

The default value is D2D1_BITMAPSOURCE_INTERPOLATION_MODE_LINEAR.


### -field D2D1_BITMAPSOURCE_PROP_ENABLE_DPI_CORRECTION

If you set this to TRUE, the effect will scale the input image to convert the DPI reported by IWICBitmapSource to the DPI of the device context. 
          The effect uses the interpolation mode you set with the InterpolationMode property. If you set this to FALSE, the effect uses a DPI of 96.0 for the output image.
          

The type is BOOL.

The default value is FALSE.


### -field D2D1_BITMAPSOURCE_PROP_ALPHA_MODE

The alpha mode of the output. This can be either premultiplied or straight.
          

The type is <a href="https://msdn.microsoft.com/2DC16975-3ABF-4880-9F62-2EE55FE604F6">D2D1_BITMAPSOURCE_ALPHA_MODE</a>.

The default value is D2D1_BITMAPSOURCE_ALPHA_MODE_PREMULTIPLIED.


### -field D2D1_BITMAPSOURCE_PROP_ORIENTATION

A flip and/or rotation operation to be performed on the image.
          

The type is <a href="https://msdn.microsoft.com/15359FE9-99CB-4047-B5C2-0EAFC87963F0">D2D1_BITMAPSOURCE_ORIENTATION</a>.

The default value is D2D1_BITMAPSOURCE_ORIENTATION_DEFAULT.


### -field D2D1_BITMAPSOURCE_PROP_FORCE_DWORD



