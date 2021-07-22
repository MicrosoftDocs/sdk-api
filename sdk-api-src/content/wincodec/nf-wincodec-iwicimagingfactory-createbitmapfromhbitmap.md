---
UID: NF:wincodec.IWICImagingFactory.CreateBitmapFromHBITMAP
title: IWICImagingFactory::CreateBitmapFromHBITMAP (wincodec.h)
description: Creates an IWICBitmap from a bitmap handle.
helpviewer_keywords: ["CreateBitmapFromHBITMAP","CreateBitmapFromHBITMAP method [Windows Imaging Component]","CreateBitmapFromHBITMAP method [Windows Imaging Component]","IWICImagingFactory interface","IWICImagingFactory interface [Windows Imaging Component]","CreateBitmapFromHBITMAP method","IWICImagingFactory.CreateBitmapFromHBITMAP","IWICImagingFactory::CreateBitmapFromHBITMAP","_wic_codec_iwicimagingfactory_createbitmapfromhbitmap","wic._wic_codec_iwicimagingfactory_createbitmapfromhbitmap","wincodec/IWICImagingFactory::CreateBitmapFromHBITMAP"]
old-location: wic\_wic_codec_iwicimagingfactory_createbitmapfromhbitmap.htm
tech.root: wic
ms.assetid: 8483f352-c31b-4afe-a011-ebef3430c576
ms.date: 12/05/2018
ms.keywords: CreateBitmapFromHBITMAP, CreateBitmapFromHBITMAP method [Windows Imaging Component], CreateBitmapFromHBITMAP method [Windows Imaging Component],IWICImagingFactory interface, IWICImagingFactory interface [Windows Imaging Component],CreateBitmapFromHBITMAP method, IWICImagingFactory.CreateBitmapFromHBITMAP, IWICImagingFactory::CreateBitmapFromHBITMAP, _wic_codec_iwicimagingfactory_createbitmapfromhbitmap, wic._wic_codec_iwicimagingfactory_createbitmapfromhbitmap, wincodec/IWICImagingFactory::CreateBitmapFromHBITMAP
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
 - IWICImagingFactory::CreateBitmapFromHBITMAP
 - wincodec/IWICImagingFactory::CreateBitmapFromHBITMAP
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
 - IWICImagingFactory.CreateBitmapFromHBITMAP
---

# IWICImagingFactory::CreateBitmapFromHBITMAP


## -description

Creates an <a href="/windows/desktop/api/wincodec/nn-wincodec-iwicbitmap">IWICBitmap</a> from a bitmap handle.

## -parameters

### -param hBitmap [in]

Type: <b>HBITMAP</b>

A bitmap handle to create the bitmap from.

### -param hPalette [in]

Type: <b>HPALETTE</b>

A palette handle used to create the bitmap.

### -param options [in]

Type: <b><a href="/windows/desktop/api/wincodec/ne-wincodec-wicbitmapalphachanneloption">WICBitmapAlphaChannelOption</a></b>

The alpha channel options to create the bitmap.

### -param ppIBitmap [out]

Type: <b><a href="/windows/desktop/api/wincodec/nn-wincodec-iwicbitmap">IWICBitmap</a>**</b>

A pointer that receives a pointer to the new bitmap.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

For a non-palletized bitmap, set NULL for the <i>hPalette</i> parameter.

## -see-also

<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap">GDI+ Bitmap class</a>



<a href="/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-bitmap-gethbitmap">GDI+ Bitmap.GetHBITMAP method</a>



<a href="/windows/desktop/api/wincodec/nn-wincodec-iwicimagingfactory">IWICImagingFactory</a>



<a href="/windows/desktop/api/wincodec/ne-wincodec-wicbitmapalphachanneloption">WICBitmapAlphaChannelOption</a>