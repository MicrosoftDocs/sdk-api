---
UID: NF:d2d1.ID2D1RenderTarget.CreateBitmapBrush(ID2D1Bitmap,const D2D1_BITMAP_BRUSH_PROPERTIES,const D2D1_BRUSH_PROPERTIES,ID2D1BitmapBrush)
title: ID2D1RenderTarget::CreateBitmapBrush(ID2D1Bitmap,const D2D1_BITMAP_BRUSH_PROPERTIES,const D2D1_BRUSH_PROPERTIES,ID2D1BitmapBrush)
author: windows-sdk-content
description: Creates an ID2D1BitmapBrush from the specified bitmap.
old-location: direct2d\ID2D1RenderTarget_CreateBitmapBrush_ptr_ID2D1Bitmap_ptr_D2D1_BITMAP_BRUSH_PROPERTIES_ptr_D2D1_BRUSH_PROPERTIES_ptr_ptr_ID2D1BitmapBrush.htm
tech.root: Direct2D
ms.assetid: ee6c8bb8-1468-462f-8573-6787af65bc35
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: CreateBitmapBrush, CreateBitmapBrush method [Direct2D], CreateBitmapBrush method [Direct2D],ID2D1RenderTarget interface, ID2D1RenderTarget interface [Direct2D],CreateBitmapBrush method, ID2D1RenderTarget.CreateBitmapBrush, ID2D1RenderTarget.CreateBitmapBrush(ID2D1Bitmap,const D2D1_BITMAP_BRUSH_PROPERTIES,const D2D1_BRUSH_PROPERTIES,ID2D1BitmapBrush), ID2D1RenderTarget::CreateBitmapBrush, ID2D1RenderTarget::CreateBitmapBrush(ID2D1Bitmap,const D2D1_BITMAP_BRUSH_PROPERTIES,const D2D1_BRUSH_PROPERTIES,ID2D1BitmapBrush), d2d1/ID2D1RenderTarget::CreateBitmapBrush, direct2d.ID2D1RenderTarget_CreateBitmapBrush_ptr_ID2D1Bitmap_ptr_D2D1_BITMAP_BRUSH_PROPERTIES_ptr_D2D1_BRUSH_PROPERTIES_ptr_ptr_ID2D1BitmapBrush
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
 - ID2D1RenderTarget.CreateBitmapBrush
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1RenderTarget::CreateBitmapBrush(ID2D1Bitmap,const D2D1_BITMAP_BRUSH_PROPERTIES,const D2D1_BRUSH_PROPERTIES,ID2D1BitmapBrush)


## -description


Creates an <a href="https://msdn.microsoft.com/22b14ffa-14cb-4e4d-bf80-7d81e4ae9ee4">ID2D1BitmapBrush</a> from the specified bitmap.


## -parameters




### -param bitmap [in]

Type: <b><a href="https://msdn.microsoft.com/e58216ea-e6b5-450f-a0ea-b879aa5dff38">ID2D1Bitmap</a>*</b>

The bitmap contents of the new brush.


### -param bitmapBrushProperties [in, optional]

Type: <b><a href="https://msdn.microsoft.com/e252d1b4-2f34-4479-94fc-636d4115b00c">D2D1_BITMAP_BRUSH_PROPERTIES</a>*</b>

The extend modes and interpolation mode of the new brush, or <b>NULL</b>. If you set this parameter to <b>NULL</b>, the brush defaults to the <a href="https://msdn.microsoft.com/6b6e1fe1-d43a-46cf-904d-5266b9bd6bf4">D2D1_EXTEND_MODE_CLAMP</a>  horizontal and vertical extend modes and the <a href="https://msdn.microsoft.com/b53b7e0a-aa8b-4788-896c-9825c9e6cceb">D2D1_BITMAP_INTERPOLATION_MODE_LINEAR</a> interpolation mode. 


### -param brushProperties [in, optional]

Type: <b><a href="https://msdn.microsoft.com/37b2fc18-a320-41c0-8717-dcd561a2f2df">D2D1_BRUSH_PROPERTIES</a>*</b>

A structure that contains the opacity and transform of the new brush, or <b>NULL</b>. If you set this parameter to <b>NULL</b>, the brush sets the opacity member to 1.0F and the transform member to the identity matrix.


### -param bitmapBrush [out]

Type: <b><a href="https://msdn.microsoft.com/22b14ffa-14cb-4e4d-bf80-7d81e4ae9ee4">ID2D1BitmapBrush</a>**</b>

When this method returns, this output parameter contains a pointer to a pointer to the new brush. Pass this parameter uninitialized.


## -returns



Type: <b><a href="a9046ed2-bfb2-4d56-a719-2824afce59ac">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/7a31d9e7-0521-40ee-b2c1-592dfaf5301e">Brushes Overview</a>



<a href="https://msdn.microsoft.com/8f78b30a-7507-4dd8-b6f4-12d88e3c9a1d">How to Create a Bitmap Brush</a>



<a href="https://msdn.microsoft.com/40629be9-5840-4bde-b369-56bbfd791775">ID2D1RenderTarget</a>
 

 

