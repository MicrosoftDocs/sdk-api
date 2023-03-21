---
UID: NF:d2d1.ID2D1RenderTarget.DrawBitmap(ID2D1Bitmap,constD2D1_RECT_F,FLOAT,D2D1_BITMAP_INTERPOLATION_MODE,constD2D1_RECT_F)
title: ID2D1RenderTarget::DrawBitmap (d2d1.h)
description: Draws the specified bitmap after scaling it to the size of the specified rectangle. (overload 3/3)
helpviewer_keywords: ["DrawBitmap","DrawBitmap method [Direct2D]","DrawBitmap method [Direct2D]","ID2D1RenderTarget interface","ID2D1RenderTarget interface [Direct2D]","DrawBitmap method","ID2D1RenderTarget.DrawBitmap","ID2D1RenderTarget::DrawBitmap","ID2D1RenderTarget::DrawBitmap(ID2D1Bitmap","const D2D1_RECT_F","FLOAT","D2D1_BITMAP_INTERPOLATION_MODE","const D2D1_RECT_F)","d2d1/ID2D1RenderTarget::DrawBitmap","direct2d.ID2D1RenderTarget_DrawBitmap_ptr_ID2D1Bitmap_ptr_D2D_RECT_F_FLOAT_D2D1_BITMAP_INTERPOLATION_MODE_ptr_D2D_RECT_F"]
old-location: direct2d\ID2D1RenderTarget_DrawBitmap_ptr_ID2D1Bitmap_ptr_D2D_RECT_F_FLOAT_D2D1_BITMAP_INTERPOLATION_MODE_ptr_D2D_RECT_F.htm
tech.root: Direct2D
ms.assetid: 35636d4a-8121-4f78-a481-f17ace558329
ms.date: 12/05/2018
ms.keywords: DrawBitmap, DrawBitmap method [Direct2D], DrawBitmap method [Direct2D],ID2D1RenderTarget interface, ID2D1RenderTarget interface [Direct2D],DrawBitmap method, ID2D1RenderTarget.DrawBitmap, ID2D1RenderTarget::DrawBitmap, ID2D1RenderTarget::DrawBitmap(ID2D1Bitmap,const D2D1_RECT_F,FLOAT,D2D1_BITMAP_INTERPOLATION_MODE,const D2D1_RECT_F), d2d1/ID2D1RenderTarget::DrawBitmap, direct2d.ID2D1RenderTarget_DrawBitmap_ptr_ID2D1Bitmap_ptr_D2D_RECT_F_FLOAT_D2D1_BITMAP_INTERPOLATION_MODE_ptr_D2D_RECT_F
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
 - ID2D1RenderTarget::DrawBitmap
 - d2d1/ID2D1RenderTarget::DrawBitmap
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
 - ID2D1RenderTarget.DrawBitmap
---

# ID2D1RenderTarget::DrawBitmap


## -description

Draws the specified bitmap after scaling it to the size of the specified rectangle.

## -parameters

### -param bitmap [in]

Type: <b><a href="/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap">ID2D1Bitmap</a>*</b>

The bitmap to render.

### -param destinationRectangle [in, optional]

Type: <b>const <a href="/windows/win32/Direct2D/d2d1-rect-f">D2D1_RECT_F</a>*</b>

The size and position, in device-independent pixels in the render target's coordinate space, of the area to which the bitmap is drawn; <b>NULL</b> to draw the selected portion of the bitmap at the origin of the render target.  If the rectangle is specified but not well-ordered, nothing is drawn, but the render target does not enter an error state.

### -param opacity

Type: <b>FLOAT</b>

A value between 0.0f and 1.0f, inclusive, that specifies an opacity value to apply to the bitmap; this value is multiplied against the alpha values of the bitmap's contents.  The default value is 1.0f.

### -param interpolationMode

Type: <b><a href="/windows/win32/api/d2d1/ne-d2d1-d2d1_bitmap_interpolation_mode">D2D1_BITMAP_INTERPOLATION_MODE</a></b>

The interpolation mode to use if the bitmap is scaled or rotated by the drawing operation. The default value is <a href="/windows/win32/api/d2d1/ne-d2d1-d2d1_bitmap_interpolation_mode">D2D1_BITMAP_INTERPOLATION_MODE_LINEAR</a>.

### -param sourceRectangle [in, optional]

Type: <b>const <a href="/windows/win32/Direct2D/d2d1-rect-f">D2D1_RECT_F</a>*</b>

The size and position, in device-independent pixels in the bitmap's coordinate space, of the area within the bitmap to be drawn; <b>NULL</b> to draw the entire bitmap.

## -remarks

This method doesn't return an error code if it fails. To determine whether a drawing operation (such as <a href="/windows/win32/Direct2D/id2d1rendertarget-drawbitmap">DrawBitmap</a>) failed, check the result returned by the <a href="/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw">ID2D1RenderTarget::EndDraw</a> or <a href="/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush">ID2D1RenderTarget::Flush</a> methods. 


## Examples

For an example, see <a href="/windows/win32/Direct2D/how-to-draw-a-bitmap">How to Draw a Bitmap</a>. For an example showing how to load a bitmap from a resource or a file, see <a href="/windows/win32/Direct2D/how-to-load-a-bitmap-from-a-resource">How to Load a Bitmap from a Resource</a> and <a href="/windows/win32/Direct2D/how-to-load-a-direct2d-bitmap-from-a-file">How to Load a Bitmap from a File</a>.

<div class="code"></div>

## -see-also

<a href="/windows/win32/Direct2D/how-to-draw-a-bitmap">How to Draw a Bitmap</a>



<a href="/windows/win32/Direct2D/how-to-load-a-direct2d-bitmap-from-a-file">How to Load a Bitmap from a File</a>



<a href="/windows/win32/Direct2D/how-to-load-a-bitmap-from-a-resource">How to Load a Bitmap from a Resource</a>



<a href="/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget">ID2D1RenderTarget</a>

