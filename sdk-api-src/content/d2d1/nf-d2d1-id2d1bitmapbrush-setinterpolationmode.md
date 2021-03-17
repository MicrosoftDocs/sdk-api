---
UID: NF:d2d1.ID2D1BitmapBrush.SetInterpolationMode
title: ID2D1BitmapBrush::SetInterpolationMode (d2d1.h)
description: Specifies the interpolation mode used when the brush bitmap is scaled or rotated.
helpviewer_keywords: ["ID2D1BitmapBrush interface [Direct2D]","SetInterpolationMode method","ID2D1BitmapBrush.SetInterpolationMode","ID2D1BitmapBrush::SetInterpolationMode","SetInterpolationMode","SetInterpolationMode method [Direct2D]","SetInterpolationMode method [Direct2D]","ID2D1BitmapBrush interface","d2d1/ID2D1BitmapBrush::SetInterpolationMode","direct2d.ID2D1BitmapBrush_SetInterpolationMode"]
old-location: direct2d\ID2D1BitmapBrush_SetInterpolationMode.htm
tech.root: Direct2D
ms.assetid: ad2a4211-c8ae-4242-9d6a-6548375f52a7
ms.date: 12/05/2018
ms.keywords: ID2D1BitmapBrush interface [Direct2D],SetInterpolationMode method, ID2D1BitmapBrush.SetInterpolationMode, ID2D1BitmapBrush::SetInterpolationMode, SetInterpolationMode, SetInterpolationMode method [Direct2D], SetInterpolationMode method [Direct2D],ID2D1BitmapBrush interface, d2d1/ID2D1BitmapBrush::SetInterpolationMode, direct2d.ID2D1BitmapBrush_SetInterpolationMode
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
req.lib: D2d1.lib
req.dll: D2d1.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID2D1BitmapBrush::SetInterpolationMode
 - d2d1/ID2D1BitmapBrush::SetInterpolationMode
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D2d1.dll
api_name:
 - ID2D1BitmapBrush.SetInterpolationMode
---

# ID2D1BitmapBrush::SetInterpolationMode


## -description

Specifies the interpolation mode used when the brush bitmap is scaled or rotated.

## -parameters

### -param interpolationMode

Type: <b><a href="/windows/win32/api/d2d1/ne-d2d1-d2d1_bitmap_interpolation_mode">D2D1_BITMAP_INTERPOLATION_MODE</a></b>

The interpolation mode used when the brush bitmap is scaled or rotated.

## -remarks

This method sets the interpolation mode for a bitmap, which is an enum value that is specified in the <a href="/windows/win32/api/d2d1/ne-d2d1-d2d1_bitmap_interpolation_mode">D2D1_BITMAP_INTERPOLATION_MODE</a> enumeration type.   D2D1_BITMAP_INTERPOLATION_MODE_NEAREST_NEIGHBOR represents nearest neighbor filtering. It looks up the nearest bitmap pixel to the current rendering pixel and chooses its exact color. D2D1_BITMAP_INTERPOLATION_MODE_LINEAR represents linear filtering, and  interpolates a color from the four nearest bitmap pixels.

The interpolation mode of a bitmap also affects subpixel translations. In a subpixel translation, bilinear interpolation positions the bitmap more precisely to the application requests, but blurs the bitmap in the process.

## -see-also

<a href="/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush">ID2D1BitmapBrush</a>



<a href="/windows/win32/api/d2d1/nf-d2d1-id2d1bitmapbrush-getinterpolationmode">ID2D1BitmapBrush::GetInterpolationMode</a>

