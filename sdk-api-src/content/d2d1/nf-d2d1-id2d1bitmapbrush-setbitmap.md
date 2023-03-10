---
UID: NF:d2d1.ID2D1BitmapBrush.SetBitmap
title: ID2D1BitmapBrush::SetBitmap (d2d1.h)
description: Specifies the bitmap source that this brush uses to paint.
helpviewer_keywords: ["ID2D1BitmapBrush interface [Direct2D]","SetBitmap method","ID2D1BitmapBrush.SetBitmap","ID2D1BitmapBrush::SetBitmap","SetBitmap","SetBitmap method [Direct2D]","SetBitmap method [Direct2D]","ID2D1BitmapBrush interface","d2d1/ID2D1BitmapBrush::SetBitmap","direct2d.ID2D1BitmapBrush_SetBitmap"]
old-location: direct2d\ID2D1BitmapBrush_SetBitmap.htm
tech.root: Direct2D
ms.assetid: 776dba7f-11d0-4055-9071-8719ac192f00
ms.date: 12/05/2018
ms.keywords: ID2D1BitmapBrush interface [Direct2D],SetBitmap method, ID2D1BitmapBrush.SetBitmap, ID2D1BitmapBrush::SetBitmap, SetBitmap, SetBitmap method [Direct2D], SetBitmap method [Direct2D],ID2D1BitmapBrush interface, d2d1/ID2D1BitmapBrush::SetBitmap, direct2d.ID2D1BitmapBrush_SetBitmap
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
 - ID2D1BitmapBrush::SetBitmap
 - d2d1/ID2D1BitmapBrush::SetBitmap
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
 - ID2D1BitmapBrush.SetBitmap
---

# ID2D1BitmapBrush::SetBitmap


## -description

Specifies the bitmap source that this brush uses to paint.

## -parameters

### -param bitmap [in]

Type: <b><a href="/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap">ID2D1Bitmap</a>*</b>

The bitmap source used by the brush.

## -remarks

This method specifies the bitmap source that this brush uses to paint. The bitmap is not resized or rescaled automatically to fit the geometry that it fills. The bitmap stays at its native size. To resize or translate the bitmap, use the <a href="/windows/win32/api/d2d1/nf-d2d1-id2d1brush-settransform(constd2d1_matrix_3x2_f)">SetTransform</a> method to apply  a transform to the brush. 

The native size of a bitmap is the width and height in bitmap pixels, divided by the bitmap DPI. This native size forms the base tile of the brush. To tile a subregion of the bitmap, you must generate a new bitmap containing this subregion and use <b>SetBitmap</b> to apply it to the brush.

## -see-also

<a href="/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush">ID2D1BitmapBrush</a>

