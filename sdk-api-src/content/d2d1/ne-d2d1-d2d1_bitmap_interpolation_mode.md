---
UID: NE:d2d1.D2D1_BITMAP_INTERPOLATION_MODE
title: D2D1_BITMAP_INTERPOLATION_MODE (d2d1.h)
description: Specifies the algorithm that is used when images are scaled or rotated.
helpviewer_keywords: ["D2D1_BITMAP_INTERPOLATION_MODE","D2D1_BITMAP_INTERPOLATION_MODE enumeration [Direct2D]","D2D1_BITMAP_INTERPOLATION_MODE_LINEAR","D2D1_BITMAP_INTERPOLATION_MODE_NEAREST_NEIGHBOR","d2d1/D2D1_BITMAP_INTERPOLATION_MODE","d2d1/D2D1_BITMAP_INTERPOLATION_MODE_LINEAR","d2d1/D2D1_BITMAP_INTERPOLATION_MODE_NEAREST_NEIGHBOR","direct2d.D2D1_BITMAP_INTERPOLATION_MODE"]
old-location: direct2d\D2D1_BITMAP_INTERPOLATION_MODE.htm
tech.root: Direct2D
ms.assetid: b53b7e0a-aa8b-4788-896c-9825c9e6cceb
ms.date: 12/05/2018
ms.keywords: D2D1_BITMAP_INTERPOLATION_MODE, D2D1_BITMAP_INTERPOLATION_MODE enumeration [Direct2D], D2D1_BITMAP_INTERPOLATION_MODE_LINEAR, D2D1_BITMAP_INTERPOLATION_MODE_NEAREST_NEIGHBOR, d2d1/D2D1_BITMAP_INTERPOLATION_MODE, d2d1/D2D1_BITMAP_INTERPOLATION_MODE_LINEAR, d2d1/D2D1_BITMAP_INTERPOLATION_MODE_NEAREST_NEIGHBOR, direct2d.D2D1_BITMAP_INTERPOLATION_MODE
req.header: d2d1.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps \| UWP apps]
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
req.typenames: D2D1_BITMAP_INTERPOLATION_MODE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D2D1_BITMAP_INTERPOLATION_MODE
 - d2d1/D2D1_BITMAP_INTERPOLATION_MODE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d2d1.h
api_name:
 - D2D1_BITMAP_INTERPOLATION_MODE
---

# D2D1_BITMAP_INTERPOLATION_MODE enumeration


## -description

Specifies the algorithm that is used when images are scaled or rotated.
<div class="alert"><b>Note</b>  Starting in Windows 8, more interpolations modes are available.  See <a href="/windows/win32/api/d2d1_1/ne-d2d1_1-d2d1_interpolation_mode">D2D1_INTERPOLATION_MODE</a> for more info.</div><div> </div>

## -enum-fields

### -field D2D1_BITMAP_INTERPOLATION_MODE_NEAREST_NEIGHBOR

Use the exact color of the nearest bitmap pixel to the current rendering pixel.

### -field D2D1_BITMAP_INTERPOLATION_MODE_LINEAR

Interpolate a color from the four bitmap pixels that are the nearest to the rendering pixel.

### -field D2D1_BITMAP_INTERPOLATION_MODE_FORCE_DWORD:0xffffffff

## -remarks

To stretch an image, each pixel in the original image must be mapped to a group of pixels in the larger image. To shrink an image, groups of pixels in the original image must be mapped to single pixels in the smaller image. The effectiveness of the algorithms that perform these mappings determines the quality of a scaled image. Algorithms that produce higher-quality scaled images tend to require more processing time. <b>D2D1_BITMAP_INTERPOLATION_MODE_NEAREST_NEIGHBOR</b> provides faster but lower-quality interpolation, while <b>D2D1_BITMAP_INTERPOLATION_MODE_LINEAR</b> provides higher-quality interpolation.
