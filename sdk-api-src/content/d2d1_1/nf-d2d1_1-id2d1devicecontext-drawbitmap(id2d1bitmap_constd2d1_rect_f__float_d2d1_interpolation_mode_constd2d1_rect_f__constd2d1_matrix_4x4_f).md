---
UID: NF:d2d1_1.ID2D1DeviceContext.DrawBitmap(ID2D1Bitmap,constD2D1_RECT_F&,FLOAT,D2D1_INTERPOLATION_MODE,constD2D1_RECT_F&,constD2D1_MATRIX_4X4_F)
title: ID2D1DeviceContext::DrawBitmap(ID2D1Bitmap,const D2D1_RECT_F &,FLOAT,D2D1_INTERPOLATION_MODE,const D2D1_RECT_F &,const D2D1_MATRIX_4X4_F) (d2d1_1.h)
description: Draws a bitmap to the render target. (overload 4/5)
helpviewer_keywords: ["DrawBitmap","DrawBitmap method [Direct2D]","DrawBitmap method [Direct2D]","ID2D1DeviceContext interface","ID2D1DeviceContext interface [Direct2D]","DrawBitmap method","ID2D1DeviceContext.DrawBitmap","ID2D1DeviceContext.DrawBitmap(ID2D1Bitmap","const D2D1_RECT_F &","FLOAT","D2D1_INTERPOLATION_MODE","const D2D1_RECT_F &","const D2D1_MATRIX_4X4_F)","ID2D1DeviceContext::DrawBitmap","ID2D1DeviceContext::DrawBitmap(ID2D1Bitmap","const D2D1_RECT_F &","FLOAT","D2D1_INTERPOLATION_MODE","const D2D1_RECT_F &","const D2D1_MATRIX_4X4_F &)","ID2D1DeviceContext::DrawBitmap(ID2D1Bitmap","const D2D1_RECT_F &","FLOAT","D2D1_INTERPOLATION_MODE","const D2D1_RECT_F &","const D2D1_MATRIX_4X4_F)","d2d1_1/ID2D1DeviceContext::DrawBitmap","direct2d.id2d1devicecontext_drawbitmap"]
old-location: direct2d\id2d1devicecontext_drawbitmap.htm
tech.root: Direct2D
ms.assetid: e6cff1b7-055b-442c-99aa-afeeee4d06e8
ms.date: 12/05/2018
ms.keywords: DrawBitmap, DrawBitmap method [Direct2D], DrawBitmap method [Direct2D],ID2D1DeviceContext interface, ID2D1DeviceContext interface [Direct2D],DrawBitmap method, ID2D1DeviceContext.DrawBitmap, ID2D1DeviceContext.DrawBitmap(ID2D1Bitmap,const D2D1_RECT_F &,FLOAT,D2D1_INTERPOLATION_MODE,const D2D1_RECT_F &,const D2D1_MATRIX_4X4_F), ID2D1DeviceContext::DrawBitmap, ID2D1DeviceContext::DrawBitmap(ID2D1Bitmap,const D2D1_RECT_F &,FLOAT,D2D1_INTERPOLATION_MODE,const D2D1_RECT_F &,const D2D1_MATRIX_4X4_F &), ID2D1DeviceContext::DrawBitmap(ID2D1Bitmap,const D2D1_RECT_F &,FLOAT,D2D1_INTERPOLATION_MODE,const D2D1_RECT_F &,const D2D1_MATRIX_4X4_F), d2d1_1/ID2D1DeviceContext::DrawBitmap, direct2d.id2d1devicecontext_drawbitmap
req.header: d2d1_1.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 and Platform Update for Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 and Platform Update for Windows Server 2008 R2 [desktop apps \| UWP apps]
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
req.dll: D2d1.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID2D1DeviceContext::DrawBitmap
 - d2d1_1/ID2D1DeviceContext::DrawBitmap
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
 - ID2D1DeviceContext.DrawBitmap
---

# ID2D1DeviceContext::DrawBitmap(ID2D1Bitmap,const D2D1_RECT_F &,FLOAT,D2D1_INTERPOLATION_MODE,const D2D1_RECT_F &,const D2D1_MATRIX_4X4_F)


## -description

Draws a bitmap to the render target.

## -parameters

### -param bitmap [in]

Type: <b><a href="/windows/desktop/api/d2d1/nn-d2d1-id2d1bitmap">ID2D1Bitmap</a>*</b>

The bitmap to draw.

### -param destinationRectangle [in, optional]

Type: <b><a href="/windows/desktop/Direct2D/d2d1-rect-f">D2D1_RECT_F</a>*</b>

The destination rectangle. The default is the size of the bitmap and the location is the upper left corner of the render target.

### -param opacity

Type: <b>FLOAT</b>

The opacity of the bitmap.

### -param interpolationMode

Type: <b><a href="/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_interpolation_mode">D2D1_INTERPOLATION_MODE</a></b>

The interpolation mode to use.

### -param sourceRectangle [in, optional]

Type: <b>const <a href="/windows/desktop/Direct2D/d2d1-rect-f">D2D1_RECT_F</a></b>

An optional source rectangle.

### -param perspectiveTransform [in, optional]

Type: <b>const <a href="/windows/desktop/Direct2D/d2d1-matrix-4x4-f">D2D1_MATRIX_4X4_F</a></b>

An optional perspective transform.

## -remarks

The destinationRectangle parameter defines the rectangle in the target where the bitmap will appear (in device-independent pixels (DIPs)).  This is affected by the currently set transform and the perspective transform, if set.  If NULL is specified, then the destination rectangle is (left=0, top=0, right = width(sourceRectangle), bottom = height(sourceRectangle)).



The <i>sourceRectangle</i> parameter defines the sub-rectangle of the source bitmap (in DIPs).  <b>DrawBitmap</b> will clip this rectangle to the size of the source bitmap, thus making it impossible to sample outside of the bitmap.  If NULL is specified, then the source rectangle is taken to be the size of the source bitmap.



If you specify <i>perspectiveTransform</i> it is applied to the rect in addition to the transform set on the render target.

## -see-also

<a href="/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1devicecontext">ID2D1DeviceContext</a>
