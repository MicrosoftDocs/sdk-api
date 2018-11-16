---
UID: NF:d2d1.ID2D1BitmapBrush.SetInterpolationMode
title: ID2D1BitmapBrush::SetInterpolationMode
author: windows-sdk-content
description: Specifies the interpolation mode used when the brush bitmap is scaled or rotated.
old-location: direct2d\ID2D1BitmapBrush_SetInterpolationMode.htm
tech.root: Direct2D
ms.assetid: ad2a4211-c8ae-4242-9d6a-6548375f52a7
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: ID2D1BitmapBrush interface [Direct2D],SetInterpolationMode method, ID2D1BitmapBrush.SetInterpolationMode, ID2D1BitmapBrush::SetInterpolationMode, SetInterpolationMode, SetInterpolationMode method [Direct2D], SetInterpolationMode method [Direct2D],ID2D1BitmapBrush interface, d2d1/ID2D1BitmapBrush::SetInterpolationMode, direct2d.ID2D1BitmapBrush_SetInterpolationMode
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D2d1.dll
api_name:
 - ID2D1BitmapBrush.SetInterpolationMode
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- d2d1.h
: 
- ID2D1BitmapBrush.SetInterpolationMode
: 
---

# ID2D1BitmapBrush::SetInterpolationMode


## -description


Specifies the interpolation mode used when the brush bitmap is scaled or rotated.


## -parameters




### -param interpolationMode

Type: <b><a href="https://msdn.microsoft.com/b53b7e0a-aa8b-4788-896c-9825c9e6cceb">D2D1_BITMAP_INTERPOLATION_MODE</a></b>

The interpolation mode used when the brush bitmap is scaled or rotated.


## -returns



This method does not return a value.




## -remarks



This method sets the interpolation mode for a bitmap, which is an enum value that is specified in the <a href="https://msdn.microsoft.com/b53b7e0a-aa8b-4788-896c-9825c9e6cceb">D2D1_BITMAP_INTERPOLATION_MODE</a> enumeration type.   D2D1_BITMAP_INTERPOLATION_MODE_NEAREST_NEIGHBOR represents nearest neighbor filtering. It looks up the nearest bitmap pixel to the current rendering pixel and chooses its exact color. D2D1_BITMAP_INTERPOLATION_MODE_LINEAR represents linear filtering, and  interpolates a color from the four nearest bitmap pixels.

The interpolation mode of a bitmap also affects subpixel translations. In a subpixel translation, bilinear interpolation positions the bitmap more precisely to the application requests, but blurs the bitmap in the process.






## -see-also




<a href="https://msdn.microsoft.com/22b14ffa-14cb-4e4d-bf80-7d81e4ae9ee4">ID2D1BitmapBrush</a>



<a href="https://msdn.microsoft.com/b0bc487b-3259-4f25-b4ab-7468ccf96d98">ID2D1BitmapBrush::GetInterpolationMode</a>
 

 

