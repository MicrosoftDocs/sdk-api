---
UID: NE:d2d1effects.D2D1_BITMAPSOURCE_INTERPOLATION_MODE
title: D2D1_BITMAPSOURCE_INTERPOLATION_MODE
author: windows-driver-content
description: The interpolation mode used to scale the image in the Bitmap source effect.
old-location: direct2d\d2d1_bitmapsource_interpolation_mode.htm
old-project: Direct2D
ms.assetid: 2912E2FA-4B1D-43FF-9684-22C3B2720395
ms.author: windowsdriverdev
ms.date: 4/20/2018
ms.keywords: D2D1_BITMAPSOURCE_INTERPOLATION_MODE, D2D1_BITMAPSOURCE_INTERPOLATION_MODE enumeration [Direct2D], D2D1_BITMAPSOURCE_INTERPOLATION_MODE_CUBIC, D2D1_BITMAPSOURCE_INTERPOLATION_MODE_FANT, D2D1_BITMAPSOURCE_INTERPOLATION_MODE_LINEAR, D2D1_BITMAPSOURCE_INTERPOLATION_MODE_MIPMAP_LINEAR, D2D1_BITMAPSOURCE_INTERPOLATION_MODE_NEAREST_NEIGHBOR, d2d1effects/D2D1_BITMAPSOURCE_INTERPOLATION_MODE, d2d1effects/D2D1_BITMAPSOURCE_INTERPOLATION_MODE_CUBIC, d2d1effects/D2D1_BITMAPSOURCE_INTERPOLATION_MODE_FANT, d2d1effects/D2D1_BITMAPSOURCE_INTERPOLATION_MODE_LINEAR, d2d1effects/D2D1_BITMAPSOURCE_INTERPOLATION_MODE_MIPMAP_LINEAR, d2d1effects/D2D1_BITMAPSOURCE_INTERPOLATION_MODE_NEAREST_NEIGHBOR, direct2d.d2d1_bitmapsource_interpolation_mode
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
req.typenames: D2D1_BITMAPSOURCE_INTERPOLATION_MODE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	d2d1effects.h
api_name:
-	D2D1_BITMAPSOURCE_INTERPOLATION_MODE
product: Windows
targetos: Windows
req.lib: D2d1.lib
req.dll: D2d1.dll
req.irql: 
---

# D2D1_BITMAPSOURCE_INTERPOLATION_MODE enumeration


## -description


The interpolation mode used to scale the image in the <a href="https://msdn.microsoft.com/86646111-208A-4E6D-A28C-7B23A1742D24">Bitmap source effect</a>.
        If the mode disables the mipmap, then BitmapSouce will cache the image at the resolution determined by the Scale and EnableDPICorrection properties.
      


## -enum-fields




### -field D2D1_BITMAPSOURCE_INTERPOLATION_MODE_NEAREST_NEIGHBOR

Samples the nearest single point and uses that. Doesn't generate a mipmap. 


### -field D2D1_BITMAPSOURCE_INTERPOLATION_MODE_LINEAR

Uses a four point sample and linear interpolation. Doesn't generate a mipmap. 


### -field D2D1_BITMAPSOURCE_INTERPOLATION_MODE_CUBIC

Uses a 16 sample cubic kernel for interpolation. Doesn't generate a mipmap. 


### -field D2D1_BITMAPSOURCE_INTERPOLATION_MODE_FANT

Uses the WIC fant interpolation, the same as the IWICBitmapScaler interface. Doesn't generate a mipmap.


### -field D2D1_BITMAPSOURCE_INTERPOLATION_MODE_MIPMAP_LINEAR

Generates mipmap chain in system memory using bilinear interpolation. For each mipmap the effect scales to the nearest multiple of 0.5 using bilinear interpolation 
          and then scales the remaining amount using linear interpolation.


### -field D2D1_BITMAPSOURCE_INTERPOLATION_MODE_FORCE_DWORD



