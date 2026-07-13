---
UID: NF:wincodec.IWICImagingFactory.CreateBitmapFromSourceRect
title: IWICImagingFactory::CreateBitmapFromSourceRect (wincodec.h)
description: Creates an IWICBitmap from a specified rectangle of an IWICBitmapSource.
helpviewer_keywords: ["CreateBitmapFromSourceRect","CreateBitmapFromSourceRect method [Windows Imaging Component]","CreateBitmapFromSourceRect method [Windows Imaging Component]","IWICImagingFactory interface","IWICImagingFactory interface [Windows Imaging Component]","CreateBitmapFromSourceRect method","IWICImagingFactory.CreateBitmapFromSourceRect","IWICImagingFactory::CreateBitmapFromSourceRect","_wic_codec_iwicimagingfactory_createbitmapfromsourcerect","wic._wic_codec_iwicimagingfactory_createbitmapfromsourcerect","wincodec/IWICImagingFactory::CreateBitmapFromSourceRect"]
old-location: wic\_wic_codec_iwicimagingfactory_createbitmapfromsourcerect.htm
tech.root: wic
ms.assetid: 54111643-523a-4197-b7e9-ee0efeae5b88
ms.date: 12/05/2018
ms.keywords: CreateBitmapFromSourceRect, CreateBitmapFromSourceRect method [Windows Imaging Component], CreateBitmapFromSourceRect method [Windows Imaging Component],IWICImagingFactory interface, IWICImagingFactory interface [Windows Imaging Component],CreateBitmapFromSourceRect method, IWICImagingFactory.CreateBitmapFromSourceRect, IWICImagingFactory::CreateBitmapFromSourceRect, _wic_codec_iwicimagingfactory_createbitmapfromsourcerect, wic._wic_codec_iwicimagingfactory_createbitmapfromsourcerect, wincodec/IWICImagingFactory::CreateBitmapFromSourceRect
req.header: wincodec.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wincodec.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Windowscodecs.lib
req.dll: Windowscodecs.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWICImagingFactory::CreateBitmapFromSourceRect
 - wincodec/IWICImagingFactory::CreateBitmapFromSourceRect
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Windowscodecs.dll
api_name:
 - IWICImagingFactory.CreateBitmapFromSourceRect
---

# IWICImagingFactory::CreateBitmapFromSourceRect


## -description

Creates an <a href="/windows/desktop/api/wincodec/nn-wincodec-iwicbitmap">IWICBitmap</a> from a specified rectangle of an <a href="/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapsource">IWICBitmapSource</a>.

## -parameters

### -param pIBitmapSource [in]

Type: <b><a href="/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapsource">IWICBitmapSource</a>*</b>

The <a href="/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapsource">IWICBitmapSource</a> to create the bitmap from.

### -param x [in]

Type: <b>UINT</b>

The horizontal coordinate of the upper-left corner of the rectangle.

### -param y [in]

Type: <b>UINT</b>

The vertical coordinate of the upper-left corner of the rectangle.

### -param width [in]

Type: <b>UINT</b>

The width of the rectangle and the new bitmap.

### -param height [in]

Type: <b>UINT</b>

The height of the rectangle and the new bitmap.

### -param ppIBitmap [out]

Type: <b><a href="/windows/desktop/api/wincodec/nn-wincodec-iwicbitmap">IWICBitmap</a>**</b>

A pointer that receives a pointer to the new bitmap.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Providing a rectangle that is larger than the source will produce undefined results.

This method always creates a separate copy of the source image, similar to the cache option <a href="/windows/desktop/api/wincodec/ne-wincodec-wicbitmapcreatecacheoption">WICBitmapCacheOnLoad</a>.