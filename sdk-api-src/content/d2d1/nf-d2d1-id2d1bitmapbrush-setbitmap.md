---
UID: NF:d2d1.ID2D1BitmapBrush.SetBitmap
title: ID2D1BitmapBrush::SetBitmap
author: windows-sdk-content
description: Specifies the bitmap source that this brush uses to paint.
old-location: direct2d\ID2D1BitmapBrush_SetBitmap.htm
tech.root: direct2d
ms.assetid: 776dba7f-11d0-4055-9071-8719ac192f00
ms.author: windowssdkdev
ms.date: 11/13/2018
ms.keywords: ID2D1BitmapBrush interface [Direct2D],SetBitmap method, ID2D1BitmapBrush.SetBitmap, ID2D1BitmapBrush::SetBitmap, SetBitmap, SetBitmap method [Direct2D], SetBitmap method [Direct2D],ID2D1BitmapBrush interface, d2d1/ID2D1BitmapBrush::SetBitmap, direct2d.ID2D1BitmapBrush_SetBitmap
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
 - ID2D1BitmapBrush.SetBitmap
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
- ID2D1BitmapBrush.SetBitmap
: 
---

# ID2D1BitmapBrush::SetBitmap


## -description


Specifies the bitmap source that this brush uses to paint. 


## -parameters




### -param bitmap [in]

Type: <b><a href="https://msdn.microsoft.com/e58216ea-e6b5-450f-a0ea-b879aa5dff38">ID2D1Bitmap</a>*</b>

The bitmap source used by the brush.


## -returns



This method does not return a value.




## -remarks



This method specifies the bitmap source that this brush uses to paint. The bitmap is not resized or rescaled automatically to fit the geometry that it fills. The bitmap stays at its native size. To resize or translate the bitmap, use the <a href="https://msdn.microsoft.com/ef9fdd4f-6338-498e-bbed-5fc676fc53b3">SetTransform</a> method to apply  a transform to the brush. 

The native size of a bitmap is the width and height in bitmap pixels, divided by the bitmap DPI. This native size forms the base tile of the brush. To tile a subregion of the bitmap, you must generate a new bitmap containing this subregion and use <b>SetBitmap</b> to apply it to the brush. 





## -see-also




<a href="https://msdn.microsoft.com/22b14ffa-14cb-4e4d-bf80-7d81e4ae9ee4">ID2D1BitmapBrush</a>
 

 

