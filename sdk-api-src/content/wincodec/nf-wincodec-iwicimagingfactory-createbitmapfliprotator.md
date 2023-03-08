---
UID: NF:wincodec.IWICImagingFactory.CreateBitmapFlipRotator
title: IWICImagingFactory::CreateBitmapFlipRotator (wincodec.h)
description: Creates a new instance of an IWICBitmapFlipRotator object.
helpviewer_keywords: ["CreateBitmapFlipRotator","CreateBitmapFlipRotator method [Windows Imaging Component]","CreateBitmapFlipRotator method [Windows Imaging Component]","IWICImagingFactory interface","IWICImagingFactory interface [Windows Imaging Component]","CreateBitmapFlipRotator method","IWICImagingFactory.CreateBitmapFlipRotator","IWICImagingFactory::CreateBitmapFlipRotator","_wic_codec_iwicimagingfactory_createbitmapfliprotator","wic._wic_codec_iwicimagingfactory_createbitmapfliprotator","wincodec/IWICImagingFactory::CreateBitmapFlipRotator"]
old-location: wic\_wic_codec_iwicimagingfactory_createbitmapfliprotator.htm
tech.root: wic
ms.assetid: ec044a38-b39d-4421-8e56-a8be0586cc49
ms.date: 12/05/2018
ms.keywords: CreateBitmapFlipRotator, CreateBitmapFlipRotator method [Windows Imaging Component], CreateBitmapFlipRotator method [Windows Imaging Component],IWICImagingFactory interface, IWICImagingFactory interface [Windows Imaging Component],CreateBitmapFlipRotator method, IWICImagingFactory.CreateBitmapFlipRotator, IWICImagingFactory::CreateBitmapFlipRotator, _wic_codec_iwicimagingfactory_createbitmapfliprotator, wic._wic_codec_iwicimagingfactory_createbitmapfliprotator, wincodec/IWICImagingFactory::CreateBitmapFlipRotator
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
 - IWICImagingFactory::CreateBitmapFlipRotator
 - wincodec/IWICImagingFactory::CreateBitmapFlipRotator
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
 - IWICImagingFactory.CreateBitmapFlipRotator
---

# IWICImagingFactory::CreateBitmapFlipRotator


## -description

Creates a new instance of an <a href="/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapfliprotator">IWICBitmapFlipRotator</a> object.

## -parameters

### -param ppIBitmapFlipRotator [out]

Type: <b><a href="/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapfliprotator">IWICBitmapFlipRotator</a>**</b>

A pointer that receives a pointer to a new <a href="/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapfliprotator">IWICBitmapFlipRotator</a>.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.