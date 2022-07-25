---
UID: NF:wincodec.IWICImagingFactory.CreatePalette
title: IWICImagingFactory::CreatePalette (wincodec.h)
description: Creates a new instance of the IWICPalette class.
helpviewer_keywords: ["CreatePalette","CreatePalette method [Windows Imaging Component]","CreatePalette method [Windows Imaging Component]","IWICImagingFactory interface","IWICImagingFactory interface [Windows Imaging Component]","CreatePalette method","IWICImagingFactory.CreatePalette","IWICImagingFactory::CreatePalette","_wic_codec_iwicimagingfactory_createpalette","wic._wic_codec_iwicimagingfactory_createpalette","wincodec/IWICImagingFactory::CreatePalette"]
old-location: wic\_wic_codec_iwicimagingfactory_createpalette.htm
tech.root: wic
ms.assetid: 135440ee-ea70-40da-9ee1-618a8e10170a
ms.date: 12/05/2018
ms.keywords: CreatePalette, CreatePalette method [Windows Imaging Component], CreatePalette method [Windows Imaging Component],IWICImagingFactory interface, IWICImagingFactory interface [Windows Imaging Component],CreatePalette method, IWICImagingFactory.CreatePalette, IWICImagingFactory::CreatePalette, _wic_codec_iwicimagingfactory_createpalette, wic._wic_codec_iwicimagingfactory_createpalette, wincodec/IWICImagingFactory::CreatePalette
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
 - IWICImagingFactory::CreatePalette
 - wincodec/IWICImagingFactory::CreatePalette
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
 - IWICImagingFactory.CreatePalette
---

# IWICImagingFactory::CreatePalette


## -description

Creates a new instance of the <a href="/windows/desktop/api/wincodec/nn-wincodec-iwicpalette">IWICPalette</a> class.

## -parameters

### -param ppIPalette [out]

Type: <b><a href="/windows/desktop/api/wincodec/nn-wincodec-iwicpalette">IWICPalette</a>**</b>

A pointer that receives a pointer to a new <a href="/windows/desktop/api/wincodec/nn-wincodec-iwicpalette">IWICPalette</a>.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.