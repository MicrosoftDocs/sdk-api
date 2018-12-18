---
UID: NF:d2d1.ID2D1RenderTarget.CreateBitmapFromWicBitmap(IWICBitmapSource,ID2D1Bitmap)
title: ID2D1RenderTarget::CreateBitmapFromWicBitmap(IWICBitmapSource,ID2D1Bitmap)
author: windows-sdk-content
description: Creates an ID2D1Bitmap by copying the specified Microsoft Windows Imaging Component (WIC) bitmap.
old-location: direct2d\ID2D1RenderTarget_CreateBitmapFromWicBitmap_ptr_IWICBitmapSource_ptr_ptr_ID2D1Bitmap.htm
tech.root: direct2d
ms.assetid: b2a106b4-067b-42ad-97ab-b5c0f07e5204
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: CreateBitmapFromWicBitmap, CreateBitmapFromWicBitmap method [Direct2D], CreateBitmapFromWicBitmap method [Direct2D],ID2D1RenderTarget interface, ID2D1RenderTarget interface [Direct2D],CreateBitmapFromWicBitmap method, ID2D1RenderTarget.CreateBitmapFromWicBitmap, ID2D1RenderTarget.CreateBitmapFromWicBitmap(IWICBitmapSource,ID2D1Bitmap), ID2D1RenderTarget::CreateBitmapFromWicBitmap, ID2D1RenderTarget::CreateBitmapFromWicBitmap(IWICBitmapSource,ID2D1Bitmap), d2d1/ID2D1RenderTarget::CreateBitmapFromWicBitmap, direct2d.ID2D1RenderTarget_CreateBitmapFromWicBitmap_ptr_IWICBitmapSource_ptr_ptr_ID2D1Bitmap
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
---

# ID2D1RenderTarget::CreateBitmapFromWicBitmap(IWICBitmapSource,ID2D1Bitmap)


## -description


Creates an <a href="https://msdn.microsoft.com/e58216ea-e6b5-450f-a0ea-b879aa5dff38">ID2D1Bitmap</a> by copying the specified Microsoft Windows Imaging Component (WIC)  bitmap.


## -parameters




### -param wicBitmapSource [in]

Type: <b><a href="_wic_codec_iwicbitmapsource">IWICBitmapSource</a>*</b>

The WIC bitmap to copy.


### -param bitmap [out]

Type: <b><a href="https://msdn.microsoft.com/e58216ea-e6b5-450f-a0ea-b879aa5dff38">ID2D1Bitmap</a>**</b>

When this method returns, contains a pointer to a pointer to the new bitmap. This parameter is passed uninitialized.


## -returns



Type: <b><a href="a9046ed2-bfb2-4d56-a719-2824afce59ac">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Before Direct2D can load a WIC image, it must be converted to a supported pixel format and alpha mode. For a list of supported pixel formats and alpha modes, see <a href="https://msdn.microsoft.com/09b1f9c6-1780-4733-ac22-9e8c21466b67">Supported Pixel Formats and Alpha Modes</a>. 


#### Examples

For examples, see <a href="https://msdn.microsoft.com/4abfbc2b-2730-4d96-897e-1e2232383a72">How to Load a   Bitmap from a File</a> and <a href="https://msdn.microsoft.com/7285e6ea-ebc7-4693-8a77-99bff0b5d0d1">How to Load a Bitmap from a Resource</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/4abfbc2b-2730-4d96-897e-1e2232383a72">How to Load a   Bitmap from a File</a>



<a href="https://msdn.microsoft.com/e58216ea-e6b5-450f-a0ea-b879aa5dff38">ID2D1Bitmap</a>



<a href="https://msdn.microsoft.com/40629be9-5840-4bde-b369-56bbfd791775">ID2D1RenderTarget</a>



<a href="https://msdn.microsoft.com/09b1f9c6-1780-4733-ac22-9e8c21466b67">Supported Pixel Formats and Alpha Modes</a>
 

 

