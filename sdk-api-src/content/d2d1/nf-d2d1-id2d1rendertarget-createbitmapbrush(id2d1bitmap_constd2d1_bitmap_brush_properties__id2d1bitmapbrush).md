---
UID: NF:d2d1.ID2D1RenderTarget.CreateBitmapBrush(ID2D1Bitmap,const D2D1_BITMAP_BRUSH_PROPERTIES &,ID2D1BitmapBrush)
title: ID2D1RenderTarget::CreateBitmapBrush(ID2D1Bitmap,const D2D1_BITMAP_BRUSH_PROPERTIES &,ID2D1BitmapBrush) (d2d1.h)
author: windows-sdk-content
description: Creates an ID2D1BitmapBrush from the specified bitmap. The brush uses the default values for its opacity and transform.
old-location: direct2d\ID2D1RenderTarget_CreateBitmapBrush_ptr_ID2D1Bitmap_ref_D2D1_BITMAP_BRUSH_PROPERTIES_ptr_ptr_ID2D1BitmapBrush.htm
tech.root: Direct2D
ms.assetid: a2ccc6d0-f18e-4ffa-9810-e1f1639d5321
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CreateBitmapBrush, CreateBitmapBrush method [Direct2D], CreateBitmapBrush method [Direct2D],ID2D1RenderTarget interface, ID2D1RenderTarget interface [Direct2D],CreateBitmapBrush method, ID2D1RenderTarget.CreateBitmapBrush, ID2D1RenderTarget.CreateBitmapBrush(ID2D1Bitmap,const D2D1_BITMAP_BRUSH_PROPERTIES &,ID2D1BitmapBrush), ID2D1RenderTarget::CreateBitmapBrush, ID2D1RenderTarget::CreateBitmapBrush(ID2D1Bitmap,const D2D1_BITMAP_BRUSH_PROPERTIES &,ID2D1BitmapBrush), d2d1/ID2D1RenderTarget::CreateBitmapBrush, direct2d.ID2D1RenderTarget_CreateBitmapBrush_ptr_ID2D1Bitmap_ref_D2D1_BITMAP_BRUSH_PROPERTIES_ptr_ptr_ID2D1BitmapBrush
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
ms.custom: 19H1
---

# ID2D1RenderTarget::CreateBitmapBrush(ID2D1Bitmap,const D2D1_BITMAP_BRUSH_PROPERTIES &,ID2D1BitmapBrush)


## -description


Creates an <a href="https://msdn.microsoft.com/22b14ffa-14cb-4e4d-bf80-7d81e4ae9ee4">ID2D1BitmapBrush</a> from the specified bitmap. The brush uses the default values for its opacity and transform.


## -parameters




### -param bitmap [in]

Type: <b><a href="https://msdn.microsoft.com/e58216ea-e6b5-450f-a0ea-b879aa5dff38">ID2D1Bitmap</a>*</b>

The bitmap contents of the new brush.


### -param bitmapBrushProperties [ref]

Type: <b>const <a href="https://msdn.microsoft.com/e252d1b4-2f34-4479-94fc-636d4115b00c">D2D1_BITMAP_BRUSH_PROPERTIES</a></b>

The extend modes and interpolation mode of the new brush. 


### -param bitmapBrush [out]

Type: <b><a href="https://msdn.microsoft.com/22b14ffa-14cb-4e4d-bf80-7d81e4ae9ee4">ID2D1BitmapBrush</a>**</b>

When this method returns, contains a pointer to a pointer to the new brush. This parameter is passed uninitialized.


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The bitmap brush created by this method has an opacity of 1.0f and the identity matrix as its transform.


#### Examples

For an example showing how to paint an area with a bitmap brush, see <a href="https://msdn.microsoft.com/8f78b30a-7507-4dd8-b6f4-12d88e3c9a1d">How to Create a Bitmap Brush</a>. 

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/7a31d9e7-0521-40ee-b2c1-592dfaf5301e">Brushes Overview</a>



<a href="https://msdn.microsoft.com/8f78b30a-7507-4dd8-b6f4-12d88e3c9a1d">How to Create a Bitmap Brush</a>



<a href="https://msdn.microsoft.com/40629be9-5840-4bde-b369-56bbfd791775">ID2D1RenderTarget</a>
 

 

