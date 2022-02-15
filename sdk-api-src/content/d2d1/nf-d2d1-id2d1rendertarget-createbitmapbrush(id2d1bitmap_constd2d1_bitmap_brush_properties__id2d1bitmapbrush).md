---
UID: NF:d2d1.ID2D1RenderTarget.CreateBitmapBrush(ID2D1Bitmap,constD2D1_BITMAP_BRUSH_PROPERTIES&,ID2D1BitmapBrush)
title: ID2D1RenderTarget::CreateBitmapBrush(ID2D1Bitmap,const D2D1_BITMAP_BRUSH_PROPERTIES &,ID2D1BitmapBrush) (d2d1.h)
description: Creates an ID2D1BitmapBrush from the specified bitmap. The brush uses the default values for its opacity and transform.
helpviewer_keywords: ["CreateBitmapBrush","CreateBitmapBrush method [Direct2D]","CreateBitmapBrush method [Direct2D]","ID2D1RenderTarget interface","ID2D1RenderTarget interface [Direct2D]","CreateBitmapBrush method","ID2D1RenderTarget.CreateBitmapBrush","ID2D1RenderTarget.CreateBitmapBrush(ID2D1Bitmap","const D2D1_BITMAP_BRUSH_PROPERTIES &","ID2D1BitmapBrush)","ID2D1RenderTarget::CreateBitmapBrush","ID2D1RenderTarget::CreateBitmapBrush(ID2D1Bitmap","const D2D1_BITMAP_BRUSH_PROPERTIES &","ID2D1BitmapBrush)","d2d1/ID2D1RenderTarget::CreateBitmapBrush","direct2d.ID2D1RenderTarget_CreateBitmapBrush_ptr_ID2D1Bitmap_ref_D2D1_BITMAP_BRUSH_PROPERTIES_ptr_ptr_ID2D1BitmapBrush"]
old-location: direct2d\ID2D1RenderTarget_CreateBitmapBrush_ptr_ID2D1Bitmap_ref_D2D1_BITMAP_BRUSH_PROPERTIES_ptr_ptr_ID2D1BitmapBrush.htm
tech.root: Direct2D
ms.assetid: a2ccc6d0-f18e-4ffa-9810-e1f1639d5321
ms.date: 12/05/2018
ms.keywords: CreateBitmapBrush, CreateBitmapBrush method [Direct2D], CreateBitmapBrush method [Direct2D],ID2D1RenderTarget interface, ID2D1RenderTarget interface [Direct2D],CreateBitmapBrush method, ID2D1RenderTarget.CreateBitmapBrush, ID2D1RenderTarget.CreateBitmapBrush(ID2D1Bitmap,const D2D1_BITMAP_BRUSH_PROPERTIES &,ID2D1BitmapBrush), ID2D1RenderTarget::CreateBitmapBrush, ID2D1RenderTarget::CreateBitmapBrush(ID2D1Bitmap,const D2D1_BITMAP_BRUSH_PROPERTIES &,ID2D1BitmapBrush), d2d1/ID2D1RenderTarget::CreateBitmapBrush, direct2d.ID2D1RenderTarget_CreateBitmapBrush_ptr_ID2D1Bitmap_ref_D2D1_BITMAP_BRUSH_PROPERTIES_ptr_ptr_ID2D1BitmapBrush
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
 - ID2D1RenderTarget::CreateBitmapBrush
 - d2d1/ID2D1RenderTarget::CreateBitmapBrush
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
 - ID2D1RenderTarget.CreateBitmapBrush
---

# ID2D1RenderTarget::CreateBitmapBrush(ID2D1Bitmap,const D2D1_BITMAP_BRUSH_PROPERTIES &,ID2D1BitmapBrush)


## -description

Creates an <a href="/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush">ID2D1BitmapBrush</a> from the specified bitmap. The brush uses the default values for its opacity and transform.

## -parameters

### -param bitmap [in]

Type: <b><a href="/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap">ID2D1Bitmap</a>*</b>

The bitmap contents of the new brush.

### -param bitmapBrushProperties [ref]

Type: <b>const <a href="/windows/win32/api/d2d1/ns-d2d1-d2d1_bitmap_brush_properties">D2D1_BITMAP_BRUSH_PROPERTIES</a></b>

The extend modes and interpolation mode of the new brush.

### -param bitmapBrush [out]

Type: <b><a href="/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush">ID2D1BitmapBrush</a>**</b>

When this method returns, contains a pointer to a pointer to the new brush. This parameter is passed uninitialized.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) error code.

## -remarks

The bitmap brush created by this method has an opacity of 1.0f and the identity matrix as its transform.


## Examples

For an example showing how to paint an area with a bitmap brush, see <a href="/windows/win32/Direct2D/how-to-create-a-bitmap-brush">How to Create a Bitmap Brush</a>. 

<div class="code"></div>

## -see-also

<a href="/windows/win32/Direct2D/direct2d-brushes-overview">Brushes Overview</a>



<a href="/windows/win32/Direct2D/how-to-create-a-bitmap-brush">How to Create a Bitmap Brush</a>



<a href="/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget">ID2D1RenderTarget</a>

