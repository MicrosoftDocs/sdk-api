---
UID: NF:d2d1.ID2D1RenderTarget.CreateBitmapFromWicBitmap(IWICBitmapSource,constD2D1_BITMAP_PROPERTIES,ID2D1Bitmap)
title: ID2D1RenderTarget::CreateBitmapFromWicBitmap (d2d1.h)
description: Creates an ID2D1Bitmap by copying the specified Microsoft Windows Imaging Component (WIC) bitmap. (overload 4/4)
helpviewer_keywords: ["CreateBitmapFromWicBitmap","CreateBitmapFromWicBitmap method [Direct2D]","CreateBitmapFromWicBitmap method [Direct2D]","ID2D1RenderTarget interface","ID2D1RenderTarget interface [Direct2D]","CreateBitmapFromWicBitmap method","ID2D1RenderTarget.CreateBitmapFromWicBitmap","ID2D1RenderTarget::CreateBitmapFromWicBitmap","ID2D1RenderTarget::CreateBitmapFromWicBitmap(IWICBitmapSource","const D2D1_BITMAP_PROPERTIES &","ID2D1Bitmap)","d2d1/ID2D1RenderTarget::CreateBitmapFromWicBitmap","direct2d.ID2D1RenderTarget_CreateBitmapFromWicBitmap_ptr_IWICBitmapSource_ptr_D2D1_BITMAP_PROPERTIES_ptr_ptr_ID2D1Bitmap"]
old-location: direct2d\ID2D1RenderTarget_CreateBitmapFromWicBitmap_ptr_IWICBitmapSource_ptr_D2D1_BITMAP_PROPERTIES_ptr_ptr_ID2D1Bitmap.htm
tech.root: Direct2D
ms.assetid: a6c571d1-a144-4f7f-9530-944c11ff4ac9
ms.date: 12/05/2018
ms.keywords: CreateBitmapFromWicBitmap, CreateBitmapFromWicBitmap method [Direct2D], CreateBitmapFromWicBitmap method [Direct2D],ID2D1RenderTarget interface, ID2D1RenderTarget interface [Direct2D],CreateBitmapFromWicBitmap method, ID2D1RenderTarget.CreateBitmapFromWicBitmap, ID2D1RenderTarget::CreateBitmapFromWicBitmap, ID2D1RenderTarget::CreateBitmapFromWicBitmap(IWICBitmapSource,const D2D1_BITMAP_PROPERTIES &,ID2D1Bitmap), d2d1/ID2D1RenderTarget::CreateBitmapFromWicBitmap, direct2d.ID2D1RenderTarget_CreateBitmapFromWicBitmap_ptr_IWICBitmapSource_ptr_D2D1_BITMAP_PROPERTIES_ptr_ptr_ID2D1Bitmap
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
 - ID2D1RenderTarget::CreateBitmapFromWicBitmap
 - d2d1/ID2D1RenderTarget::CreateBitmapFromWicBitmap
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
 - ID2D1RenderTarget.CreateBitmapFromWicBitmap
---

## -description

Creates an <a href="/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap">ID2D1Bitmap</a> by copying the specified Microsoft Windows Imaging Component (WIC) bitmap.

## -parameters

### -param wicBitmapSource

Type: [in] <b><a href="/windows/win32/api/wincodec/nn-wincodec-iwicbitmapsource">IWICBitmapSource</a>*</b>

The WIC bitmap to copy.

### -param bitmapProperties

Type: [in, optional] <b>const <a href="/windows/win32/api/d2d1/ns-d2d1-d2d1_bitmap_properties">D2D1_BITMAP_PROPERTIES</a>*</b>

The pixel format and DPI of the bitmap to create. The pixel format must match the pixel format of <i>wicBitmapSource</i>, or the method will fail. To prevent a mismatch, you can pass <b>NULL</b> or pass the value obtained from calling the <a href="/windows/win32/api/d2d1helper/nf-d2d1helper-pixelformat">D2D1::PixelFormat</a> helper function without specifying any parameter values. If both <i>dpiX</i> and <i>dpiY</i> are 0.0f, the default DPI, 96, is used. DPI information embedded in <i>wicBitmapSource</i> is ignored.

### -param bitmap [out]

Type: <b><a href="/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap">ID2D1Bitmap</a>**</b>

When this method returns, contains the address of a pointer to the new bitmap. This parameter is passed uninitialized.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) error code.

## -remarks

Before Direct2D can load a WIC bitmap, that bitmap must be converted to a supported pixel format and alpha mode. For a list of supported pixel formats and alpha modes, see <a href="/windows/win32/Direct2D/supported-pixel-formats-and-alpha-modes">Supported Pixel Formats and Alpha Modes</a>. 

## Examples

For examples, see <a href="/windows/win32/Direct2D/how-to-load-a-direct2d-bitmap-from-a-file">How to Load a Bitmap from a File</a> and <a href="/windows/win32/Direct2D/how-to-load-a-bitmap-from-a-resource">How to Load a Bitmap from a Resource</a>.

## -see-also

<a href="/windows/win32/Direct2D/how-to-load-a-direct2d-bitmap-from-a-file">How to Load a Bitmap from a File</a>

<a href="/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap">ID2D1Bitmap</a>

<a href="/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget">ID2D1RenderTarget</a>

<a href="/windows/win32/Direct2D/supported-pixel-formats-and-alpha-modes">Supported Pixel Formats and Alpha Modes</a>

