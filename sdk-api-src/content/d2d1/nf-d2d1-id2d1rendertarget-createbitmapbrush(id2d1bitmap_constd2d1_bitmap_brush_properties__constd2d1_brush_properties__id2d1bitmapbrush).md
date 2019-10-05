---
UID: NF:d2d1.ID2D1RenderTarget.CreateBitmapBrush(ID2D1Bitmap,const D2D1_BITMAP_BRUSH_PROPERTIES &,const D2D1_BRUSH_PROPERTIES &,ID2D1BitmapBrush)
title: ID2D1RenderTarget::CreateBitmapBrush(ID2D1Bitmap,const D2D1_BITMAP_BRUSH_PROPERTIES &,const D2D1_BRUSH_PROPERTIES &,ID2D1BitmapBrush) (d2d1.h)
author: windows-sdk-content
description: Creates an ID2D1BitmapBrush from the specified bitmap.
old-location: direct2d\ID2D1RenderTarget_CreateBitmapBrush_ptr_ID2D1Bitmap_ptr_D2D1_BITMAP_BRUSH_PROPERTIES_ptr_D2D1_BRUSH_PROPERTIES_ptr_ptr_ID2D1BitmapBrush.htm
tech.root: Direct2D
ms.assetid: ee6c8bb8-1468-462f-8573-6787af65bc35
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CreateBitmapBrush, CreateBitmapBrush method [Direct2D], CreateBitmapBrush method [Direct2D],ID2D1RenderTarget interface, ID2D1RenderTarget interface [Direct2D],CreateBitmapBrush method, ID2D1RenderTarget.CreateBitmapBrush, ID2D1RenderTarget.CreateBitmapBrush(ID2D1Bitmap,const D2D1_BITMAP_BRUSH_PROPERTIES &,const D2D1_BRUSH_PROPERTIES &,ID2D1BitmapBrush), ID2D1RenderTarget::CreateBitmapBrush, ID2D1RenderTarget::CreateBitmapBrush(ID2D1Bitmap,const D2D1_BITMAP_BRUSH_PROPERTIES &,const D2D1_BRUSH_PROPERTIES &,ID2D1BitmapBrush), ID2D1RenderTarget::CreateBitmapBrush(ID2D1Bitmap,const D2D1_BITMAP_BRUSH_PROPERTIES,const D2D1_BRUSH_PROPERTIES,ID2D1BitmapBrush), d2d1/ID2D1RenderTarget::CreateBitmapBrush, direct2d.ID2D1RenderTarget_CreateBitmapBrush_ptr_ID2D1Bitmap_ptr_D2D1_BITMAP_BRUSH_PROPERTIES_ptr_D2D1_BRUSH_PROPERTIES_ptr_ptr_ID2D1BitmapBrush
ms.topic: method
f1_keywords: 
 - "d2d1/ID2D1RenderTarget.CreateBitmapBrush"
dev_langs:
 - c++
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

# ID2D1RenderTarget::CreateBitmapBrush(ID2D1Bitmap,const D2D1_BITMAP_BRUSH_PROPERTIES &,const D2D1_BRUSH_PROPERTIES &,ID2D1BitmapBrush)


## -description


Creates an <a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nn-d2d1-id2d1bitmapbrush">ID2D1BitmapBrush</a> from the specified bitmap.


## -parameters




### -param bitmap [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nn-d2d1-id2d1bitmap">ID2D1Bitmap</a>*</b>

The bitmap contents of the new brush.


### -param bitmapBrushProperties [in, optional]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/d2d1/ns-d2d1-d2d1_bitmap_brush_properties">D2D1_BITMAP_BRUSH_PROPERTIES</a>*</b>

The extend modes and interpolation mode of the new brush, or <b>NULL</b>. If you set this parameter to <b>NULL</b>, the brush defaults to the <a href="https://docs.microsoft.com/windows/desktop/api/d2d1/ne-d2d1-d2d1_extend_mode">D2D1_EXTEND_MODE_CLAMP</a>  horizontal and vertical extend modes and the <a href="https://docs.microsoft.com/windows/desktop/api/d2d1/ne-d2d1-d2d1_bitmap_interpolation_mode">D2D1_BITMAP_INTERPOLATION_MODE_LINEAR</a> interpolation mode. 


### -param brushProperties [in, optional]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/d2d1/ns-d2d1-d2d1_brush_properties">D2D1_BRUSH_PROPERTIES</a>*</b>

A structure that contains the opacity and transform of the new brush, or <b>NULL</b>. If you set this parameter to <b>NULL</b>, the brush sets the opacity member to 1.0F and the transform member to the identity matrix.


### -param bitmapBrush [out]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nn-d2d1-id2d1bitmapbrush">ID2D1BitmapBrush</a>**</b>

When this method returns, this output parameter contains a pointer to a pointer to the new brush. Pass this parameter uninitialized.


## -returns



Type: <b><a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/hh437604(v=vs.85)">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Direct2D/direct2d-brushes-overview">Brushes Overview</a>



<a href="https://docs.microsoft.com/windows/desktop/Direct2D/how-to-create-a-bitmap-brush">How to Create a Bitmap Brush</a>



<a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nn-d2d1-id2d1rendertarget">ID2D1RenderTarget</a>
 

 

