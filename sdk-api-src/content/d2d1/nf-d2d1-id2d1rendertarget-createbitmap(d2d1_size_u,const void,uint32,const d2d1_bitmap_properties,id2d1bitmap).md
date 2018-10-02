---
UID: NF:d2d1.ID2D1RenderTarget.CreateBitmap(D2D1_SIZE_U,const void,UINT32,const D2D1_BITMAP_PROPERTIES,ID2D1Bitmap)
title: ID2D1RenderTarget::CreateBitmap(D2D1_SIZE_U,const void,UINT32,const D2D1_BITMAP_PROPERTIES,ID2D1Bitmap)
author: windows-sdk-content
description: Creates a Direct2D bitmap from a pointer to in-memory source data.
old-location: direct2d\ID2D1RenderTarget_CreateBitmap_D2D_SIZE_U_ptr_void_UINT32_ptr_D2D1_BITMAP_PROPERTIES_ptr_ptr_ID2D1Bitmap.htm
tech.root: direct2d
ms.assetid: 76e91383-6da7-47ae-9d5e-a83d78556b29
ms.author: windowssdkdev
ms.date: 09/28/2018
ms.keywords: CreateBitmap, CreateBitmap method [Direct2D], CreateBitmap method [Direct2D],ID2D1RenderTarget interface, ID2D1RenderTarget interface [Direct2D],CreateBitmap method, ID2D1RenderTarget.CreateBitmap, ID2D1RenderTarget.CreateBitmap(D2D1_SIZE_U,const void,UINT32,const D2D1_BITMAP_PROPERTIES,ID2D1Bitmap), ID2D1RenderTarget::CreateBitmap, ID2D1RenderTarget::CreateBitmap(D2D1_SIZE_U,const void,UINT32,const D2D1_BITMAP_PROPERTIES,ID2D1Bitmap), d2d1/ID2D1RenderTarget::CreateBitmap, direct2d.ID2D1RenderTarget_CreateBitmap_D2D_SIZE_U_ptr_void_UINT32_ptr_D2D1_BITMAP_PROPERTIES_ptr_ptr_ID2D1Bitmap
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
 - ID2D1RenderTarget.CreateBitmap
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1RenderTarget::CreateBitmap(D2D1_SIZE_U,const void,UINT32,const D2D1_BITMAP_PROPERTIES,ID2D1Bitmap)


## -description


Creates a Direct2D bitmap from a pointer to in-memory source data.


## -parameters




### -param size

Type: <b><a href="https://msdn.microsoft.com/e28da5ee-7d68-4ec5-b477-c6ead0c725e6">D2D1_SIZE_U</a></b>

The dimension of the bitmap to create in pixels.


#### - srcData [in, optional]

Type: <b>void*</b>

A pointer to the memory location of the image data, or <b>NULL</b> to create an uninitialized bitmap.


#### - pitch

Type: <b>UINT32</b>

The byte count of each scanline, which is equal to (the image width in pixels × the number of bytes per pixel) + memory padding. If <i>srcData</i> is <b>NULL</b>, this value is ignored. (Note that pitch is also sometimes called <i>stride</i>.)


### -param bitmapProperties [in]

Type: <b>const <a href="https://msdn.microsoft.com/050246fd-f91a-4a2a-858a-5f0447e3ecbf">D2D1_BITMAP_PROPERTIES</a>*</b>

The pixel format and dots per inch (DPI) of the bitmap to create.


### -param bitmap [out]

Type: <b><a href="https://msdn.microsoft.com/e58216ea-e6b5-450f-a0ea-b879aa5dff38">ID2D1Bitmap</a>**</b>

When this method returns, contains a pointer to a pointer to the new bitmap. This parameter is passed uninitialized.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/40629be9-5840-4bde-b369-56bbfd791775">ID2D1RenderTarget</a>
 

 

