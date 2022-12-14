---
UID: NF:d2d1.ID2D1RenderTarget.CreateBitmapFromWicBitmap(IWICBitmapSource,ID2D1Bitmap)
title: ID2D1RenderTarget::CreateBitmapFromWicBitmap(IWICBitmapSource,ID2D1Bitmap) (d2d1.h)
description: Creates an ID2D1Bitmap by copying the specified Microsoft Windows Imaging Component (WIC) bitmap. (overload 3/4)
helpviewer_keywords: ["CreateBitmapFromWicBitmap","CreateBitmapFromWicBitmap method [Direct2D]","CreateBitmapFromWicBitmap method [Direct2D]","ID2D1RenderTarget interface","ID2D1RenderTarget interface [Direct2D]","CreateBitmapFromWicBitmap method","ID2D1RenderTarget.CreateBitmapFromWicBitmap","ID2D1RenderTarget.CreateBitmapFromWicBitmap(IWICBitmapSource","ID2D1Bitmap)","ID2D1RenderTarget::CreateBitmapFromWicBitmap","ID2D1RenderTarget::CreateBitmapFromWicBitmap(IWICBitmapSource","ID2D1Bitmap)","d2d1/ID2D1RenderTarget::CreateBitmapFromWicBitmap","direct2d.ID2D1RenderTarget_CreateBitmapFromWicBitmap_ptr_IWICBitmapSource_ptr_ptr_ID2D1Bitmap"]
old-location: direct2d\ID2D1RenderTarget_CreateBitmapFromWicBitmap_ptr_IWICBitmapSource_ptr_ptr_ID2D1Bitmap.htm
tech.root: Direct2D
ms.assetid: b2a106b4-067b-42ad-97ab-b5c0f07e5204
ms.date: 12/05/2018
ms.keywords: CreateBitmapFromWicBitmap, CreateBitmapFromWicBitmap method [Direct2D], CreateBitmapFromWicBitmap method [Direct2D],ID2D1RenderTarget interface, ID2D1RenderTarget interface [Direct2D],CreateBitmapFromWicBitmap method, ID2D1RenderTarget.CreateBitmapFromWicBitmap, ID2D1RenderTarget.CreateBitmapFromWicBitmap(IWICBitmapSource,ID2D1Bitmap), ID2D1RenderTarget::CreateBitmapFromWicBitmap, ID2D1RenderTarget::CreateBitmapFromWicBitmap(IWICBitmapSource,ID2D1Bitmap), d2d1/ID2D1RenderTarget::CreateBitmapFromWicBitmap, direct2d.ID2D1RenderTarget_CreateBitmapFromWicBitmap_ptr_IWICBitmapSource_ptr_ptr_ID2D1Bitmap
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

### -param bitmap [out]

Type: <b><a href="/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap">ID2D1Bitmap</a>**</b>

When this method returns, contains a pointer to a pointer to the new bitmap. This parameter is passed uninitialized.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) error code.

## -remarks

Before Direct2D can load a WIC image, it must be converted to a supported pixel format and alpha mode. For a list of supported pixel formats and alpha modes, see <a href="/windows/win32/Direct2D/supported-pixel-formats-and-alpha-modes">Supported Pixel Formats and Alpha Modes</a>. 

## Examples

For examples, see <a href="/windows/win32/Direct2D/how-to-load-a-direct2d-bitmap-from-a-file">How to Load a Bitmap from a File</a> and <a href="/windows/win32/Direct2D/how-to-load-a-bitmap-from-a-resource">How to Load a Bitmap from a Resource</a>.

## -see-also

<a href="/windows/win32/Direct2D/how-to-load-a-direct2d-bitmap-from-a-file">How to Load a Bitmap from a File</a>

<a href="/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap">ID2D1Bitmap</a>

<a href="/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget">ID2D1RenderTarget</a>

<a href="/windows/win32/Direct2D/supported-pixel-formats-and-alpha-modes">Supported Pixel Formats and Alpha Modes</a>

