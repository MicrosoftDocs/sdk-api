---
UID: NF:d2d1.ID2D1RenderTarget.CreateBitmap(D2D1_SIZE_U,constvoid,UINT32,constD2D1_BITMAP_PROPERTIES,ID2D1Bitmap)
title: ID2D1RenderTarget::CreateBitmap(D2D1_SIZE_U,const void,UINT32,const D2D1_BITMAP_PROPERTIES,ID2D1Bitmap) (d2d1.h)
description: Creates an ID2D1BitmapBrush from the specified bitmap. (overload 2/3)
helpviewer_keywords: ["CreateBitmap","CreateBitmapBrush method [Direct2D]","CreateBitmapBrush method [Direct2D]","ID2D1RenderTarget interface","ID2D1RenderTarget interface [Direct2D]","CreateBitmapBrush method","ID2D1RenderTarget.CreateBitmap","ID2D1RenderTarget.CreateBitmap(D2D1_SIZE_U","const void","UINT32","const D2D1_BITMAP_PROPERTIES","ID2D1Bitmap)","ID2D1RenderTarget::CreateBitmap","ID2D1RenderTarget::CreateBitmap(D2D1_SIZE_U","const void","UINT32","const D2D1_BITMAP_PROPERTIES","ID2D1Bitmap)","ID2D1RenderTarget::CreateBitmapBrush","d2d1/ID2D1RenderTarget::CreateBitmapBrush","direct2d.ID2D1RenderTarget_CreateBitmapBrush_ptr_ID2D1Bitmap_ref_D2D1_BITMAP_BRUSH_PROPERTIES_ref_D2D1_BRUSH_PROPERTIES_ptr_ptr_ID2D1BitmapBrush"]
old-location: direct2d\ID2D1RenderTarget_CreateBitmapBrush_ptr_ID2D1Bitmap_ref_D2D1_BITMAP_BRUSH_PROPERTIES_ref_D2D1_BRUSH_PROPERTIES_ptr_ptr_ID2D1BitmapBrush.htm
tech.root: Direct2D
ms.assetid: 9c3be6a0-ac67-4dc1-9c5a-0ee47343cb86
ms.date: 12/05/2018
ms.keywords: CreateBitmap, CreateBitmapBrush method [Direct2D], CreateBitmapBrush method [Direct2D],ID2D1RenderTarget interface, ID2D1RenderTarget interface [Direct2D],CreateBitmapBrush method, ID2D1RenderTarget.CreateBitmap, ID2D1RenderTarget.CreateBitmap(D2D1_SIZE_U,const void,UINT32,const D2D1_BITMAP_PROPERTIES,ID2D1Bitmap), ID2D1RenderTarget::CreateBitmap, ID2D1RenderTarget::CreateBitmap(D2D1_SIZE_U,const void,UINT32,const D2D1_BITMAP_PROPERTIES,ID2D1Bitmap), ID2D1RenderTarget::CreateBitmapBrush, d2d1/ID2D1RenderTarget::CreateBitmapBrush, direct2d.ID2D1RenderTarget_CreateBitmapBrush_ptr_ID2D1Bitmap_ref_D2D1_BITMAP_BRUSH_PROPERTIES_ref_D2D1_BRUSH_PROPERTIES_ptr_ptr_ID2D1BitmapBrush
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
 - ID2D1RenderTarget::CreateBitmap
 - d2d1/ID2D1RenderTarget::CreateBitmap
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

## -description

Creates an <a href="/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush">ID2D1BitmapBrush</a> from the specified bitmap.

## -parameters

### -param size

Type: [in] <b><a href="/windows/win32/Direct2D/d2d1-size-u">D2D1_SIZE_U</a></b>

The dimensions of the bitmap to create, in pixels.

### -param srcData

Type: [in] <b>const void*</b>

A pointer to the memory location of the image data, or <b>NULL</b> to create an uninitialized bitmap.

### -param pitch

Type: [in] <b>UINT32</b>

The byte count of each scanline, which is equal to (the image width in pixels × the number of bytes per pixel) + memory padding. If <i>srcData</i> is <b>NULL</b>, this value is ignored. (Note that pitch is also sometimes called <i>stride</i>.)

### -param bitmapProperties

Type: [in] <b>const <a href="/windows/win32/api/d2d1/ns-d2d1-d2d1_bitmap_properties">D2D1_BITMAP_PROPERTIES</a>*</b>

The pixel format and dots per inch (DPI) of the bitmap to create.

### -param bitmap

Type: [out] <b><a href="/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap">ID2D1Bitmap</a>*</b>

The bitmap contents of the new brush.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) error code.

## -see-also

<a href="/windows/win32/Direct2D/direct2d-brushes-overview">Brushes Overview</a>

<a href="/windows/win32/Direct2D/how-to-create-a-bitmap-brush">How to Create a Bitmap Brush</a>

<a href="/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget">ID2D1RenderTarget</a>

