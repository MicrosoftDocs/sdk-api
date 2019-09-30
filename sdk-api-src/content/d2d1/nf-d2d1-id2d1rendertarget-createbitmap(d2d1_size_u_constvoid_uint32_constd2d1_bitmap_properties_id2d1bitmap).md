---
UID: NF:d2d1.ID2D1RenderTarget.CreateBitmap(D2D1_SIZE_U,const void,UINT32,const D2D1_BITMAP_PROPERTIES,ID2D1Bitmap)
title: ID2D1RenderTarget::CreateBitmap(D2D1_SIZE_U,const void,UINT32,const D2D1_BITMAP_PROPERTIES,ID2D1Bitmap) (d2d1.h)
author: windows-sdk-content
description: Creates an ID2D1BitmapBrush from the specified bitmap.
old-location: direct2d\ID2D1RenderTarget_CreateBitmapBrush_ptr_ID2D1Bitmap_ref_D2D1_BITMAP_BRUSH_PROPERTIES_ref_D2D1_BRUSH_PROPERTIES_ptr_ptr_ID2D1BitmapBrush.htm
tech.root: Direct2D
ms.assetid: 9c3be6a0-ac67-4dc1-9c5a-0ee47343cb86
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CreateBitmap, CreateBitmapBrush method [Direct2D], CreateBitmapBrush method [Direct2D],ID2D1RenderTarget interface, ID2D1RenderTarget interface [Direct2D],CreateBitmapBrush method, ID2D1RenderTarget.CreateBitmap, ID2D1RenderTarget.CreateBitmap(D2D1_SIZE_U,const void,UINT32,const D2D1_BITMAP_PROPERTIES,ID2D1Bitmap), ID2D1RenderTarget::CreateBitmap, ID2D1RenderTarget::CreateBitmap(D2D1_SIZE_U,const void,UINT32,const D2D1_BITMAP_PROPERTIES,ID2D1Bitmap), ID2D1RenderTarget::CreateBitmapBrush, d2d1/ID2D1RenderTarget::CreateBitmapBrush, direct2d.ID2D1RenderTarget_CreateBitmapBrush_ptr_ID2D1Bitmap_ref_D2D1_BITMAP_BRUSH_PROPERTIES_ref_D2D1_BRUSH_PROPERTIES_ptr_ptr_ID2D1BitmapBrush
ms.topic: method
f1_keywords: 
 - "d2d1/ID2D1RenderTarget.CreateBitmapBrush"
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
 - ID2D1RenderTarget.CreateBitmapBrush
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID2D1RenderTarget::CreateBitmap(D2D1_SIZE_U,const void,UINT32,const D2D1_BITMAP_PROPERTIES,ID2D1Bitmap)


## -description


Creates an <a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nn-d2d1-id2d1bitmapbrush">ID2D1BitmapBrush</a> from the specified bitmap.


## -parameters




### -param size

TBD


### -param srcData

TBD


### -param pitch

TBD


### -param bitmapProperties

TBD


### -param bitmap [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nn-d2d1-id2d1bitmap">ID2D1Bitmap</a>*</b>

The bitmap contents of the new brush.


#### - bitmapBrush [out]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nn-d2d1-id2d1bitmapbrush">ID2D1BitmapBrush</a>**</b>

When this method returns, contains a pointer to a pointer to the new brush. This parameter is passed uninitialized.


#### - bitmapBrushProperties [ref]

Type: <b>const <a href="https://docs.microsoft.com/windows/desktop/api/d2d1/ns-d2d1-d2d1_bitmap_brush_properties">D2D1_BITMAP_BRUSH_PROPERTIES</a></b>

The extend modes and interpolation mode of the new brush. 


#### - brushProperties [ref]

Type: <b>const <a href="https://docs.microsoft.com/windows/desktop/api/d2d1/ns-d2d1-d2d1_brush_properties">D2D1_BRUSH_PROPERTIES</a></b>

The opacity and transform of the new brush.


## -returns



Type: <b><a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/hh437604(v=vs.85)">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Direct2D/direct2d-brushes-overview">Brushes Overview</a>



<a href="https://docs.microsoft.com/windows/desktop/Direct2D/how-to-create-a-bitmap-brush">How to Create a Bitmap Brush</a>



<a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nn-d2d1-id2d1rendertarget">ID2D1RenderTarget</a>
 

 

