---
UID: NF:wincodec.IWICImagingFactory.CreateBitmapFromHICON
title: IWICImagingFactory::CreateBitmapFromHICON (wincodec.h)
description: Creates an IWICBitmap from an icon handle.
helpviewer_keywords: ["CreateBitmapFromHICON","CreateBitmapFromHICON method [Windows Imaging Component]","CreateBitmapFromHICON method [Windows Imaging Component]","IWICImagingFactory interface","IWICImagingFactory interface [Windows Imaging Component]","CreateBitmapFromHICON method","IWICImagingFactory.CreateBitmapFromHICON","IWICImagingFactory::CreateBitmapFromHICON","_wic_codec_iwicimagingfactory_createbitmapfromhicon","wic._wic_codec_iwicimagingfactory_createbitmapfromhicon","wincodec/IWICImagingFactory::CreateBitmapFromHICON"]
old-location: wic\_wic_codec_iwicimagingfactory_createbitmapfromhicon.htm
tech.root: wic
ms.assetid: a67695a1-30ac-4e28-a9a9-582601139e17
ms.date: 12/05/2018
ms.keywords: CreateBitmapFromHICON, CreateBitmapFromHICON method [Windows Imaging Component], CreateBitmapFromHICON method [Windows Imaging Component],IWICImagingFactory interface, IWICImagingFactory interface [Windows Imaging Component],CreateBitmapFromHICON method, IWICImagingFactory.CreateBitmapFromHICON, IWICImagingFactory::CreateBitmapFromHICON, _wic_codec_iwicimagingfactory_createbitmapfromhicon, wic._wic_codec_iwicimagingfactory_createbitmapfromhicon, wincodec/IWICImagingFactory::CreateBitmapFromHICON
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
 - IWICImagingFactory::CreateBitmapFromHICON
 - wincodec/IWICImagingFactory::CreateBitmapFromHICON
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
 - IWICImagingFactory.CreateBitmapFromHICON
---

# IWICImagingFactory::CreateBitmapFromHICON


## -description

Creates an <a href="/windows/desktop/api/wincodec/nn-wincodec-iwicbitmap">IWICBitmap</a> from an icon handle.

## -parameters

### -param hIcon [in]

Type: <b>HICON</b>

The icon handle to create the new bitmap from.

### -param ppIBitmap [out]

Type: <b><a href="/windows/desktop/api/wincodec/nn-wincodec-iwicbitmap">IWICBitmap</a>**</b>

A pointer that receives a pointer to the new bitmap.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.