---
UID: NF:d2d1.ID2D1RenderTarget.CreateBitmapFromWicBitmap(IWICBitmapSource,const D2D1_BITMAP_PROPERTIES &,ID2D1Bitmap)
title: ID2D1RenderTarget::CreateBitmapFromWicBitmap(IWICBitmapSource,const D2D1_BITMAP_PROPERTIES &,ID2D1Bitmap) (d2d1.h)
author: windows-sdk-content
description: Creates an ID2D1Bitmap by copying the specified Microsoft Windows Imaging Component (WIC) bitmap.
old-location: direct2d\ID2D1RenderTarget_CreateBitmapFromWicBitmap_ptr_IWICBitmapSource_ptr_D2D1_BITMAP_PROPERTIES_ptr_ptr_ID2D1Bitmap.htm
tech.root: Direct2D
ms.assetid: a6c571d1-a144-4f7f-9530-944c11ff4ac9
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CreateBitmapFromWicBitmap, CreateBitmapFromWicBitmap method [Direct2D], CreateBitmapFromWicBitmap method [Direct2D],ID2D1RenderTarget interface, ID2D1RenderTarget interface [Direct2D],CreateBitmapFromWicBitmap method, ID2D1RenderTarget.CreateBitmapFromWicBitmap, ID2D1RenderTarget.CreateBitmapFromWicBitmap(IWICBitmapSource,const D2D1_BITMAP_PROPERTIES &,ID2D1Bitmap), ID2D1RenderTarget::CreateBitmapFromWicBitmap, ID2D1RenderTarget::CreateBitmapFromWicBitmap(IWICBitmapSource,const D2D1_BITMAP_PROPERTIES &,ID2D1Bitmap), d2d1/ID2D1RenderTarget::CreateBitmapFromWicBitmap, direct2d.ID2D1RenderTarget_CreateBitmapFromWicBitmap_ptr_IWICBitmapSource_ptr_D2D1_BITMAP_PROPERTIES_ptr_ptr_ID2D1Bitmap
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
 - ID2D1RenderTarget.CreateBitmapFromWicBitmap
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID2D1RenderTarget::CreateBitmapFromWicBitmap(IWICBitmapSource,const D2D1_BITMAP_PROPERTIES &,ID2D1Bitmap)


## -description


Creates an <a href="https://msdn.microsoft.com/e58216ea-e6b5-450f-a0ea-b879aa5dff38">ID2D1Bitmap</a> by copying the specified Microsoft Windows Imaging Component (WIC)  bitmap.


## -parameters




### -param wicBitmapSource [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Ee690171(v=VS.85).aspx">IWICBitmapSource</a>*</b>

The WIC bitmap to copy.


### -param bitmapProperties [in, optional]

Type: <b>const <a href="https://msdn.microsoft.com/050246fd-f91a-4a2a-858a-5f0447e3ecbf">D2D1_BITMAP_PROPERTIES</a>*</b>

The pixel format and DPI of the bitmap to create. The pixel format must match the pixel format of <i>wicBitmapSource</i>, or the method will fail. To prevent a mismatch, you can pass <b>NULL</b> or pass the value obtained from calling the <a href="https://msdn.microsoft.com/97128e07-68c2-40ab-bad1-7b6f599291b9">D2D1::PixelFormat</a> helper function without specifying any parameter values. If both <i>dpiX</i> and <i>dpiY</i> are  0.0f, the default DPI, 96, is used. DPI information embedded in <i>wicBitmapSource</i>  is ignored.


### -param bitmap [out]

Type: <b><a href="https://msdn.microsoft.com/e58216ea-e6b5-450f-a0ea-b879aa5dff38">ID2D1Bitmap</a>**</b>

When this method returns, contains the address of a pointer to the new bitmap. This parameter is passed uninitialized.


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Before Direct2D can load a WIC bitmap, that bitmap must be converted to a supported pixel format and alpha mode. For a list of supported pixel formats and alpha modes, see <a href="https://msdn.microsoft.com/09b1f9c6-1780-4733-ac22-9e8c21466b67">Supported Pixel Formats and Alpha Modes</a>. 


#### Examples

For examples, see <a href="https://msdn.microsoft.com/4abfbc2b-2730-4d96-897e-1e2232383a72">How to Load a   Bitmap from a File</a> and <a href="https://msdn.microsoft.com/7285e6ea-ebc7-4693-8a77-99bff0b5d0d1">How to Load a Bitmap from a Resource</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/4abfbc2b-2730-4d96-897e-1e2232383a72">How to Load a   Bitmap from a File</a>



<a href="https://msdn.microsoft.com/e58216ea-e6b5-450f-a0ea-b879aa5dff38">ID2D1Bitmap</a>



<a href="https://msdn.microsoft.com/40629be9-5840-4bde-b369-56bbfd791775">ID2D1RenderTarget</a>



<a href="https://msdn.microsoft.com/09b1f9c6-1780-4733-ac22-9e8c21466b67">Supported Pixel Formats and Alpha Modes</a>
 

 

