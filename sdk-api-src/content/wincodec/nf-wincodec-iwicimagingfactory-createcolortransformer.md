---
UID: NF:wincodec.IWICImagingFactory.CreateColorTransformer
title: IWICImagingFactory::CreateColorTransformer (wincodec.h)
description: Creates a new instance of the IWICColorTransform class.
helpviewer_keywords: ["CreateColorTransformer","CreateColorTransformer method [Windows Imaging Component]","CreateColorTransformer method [Windows Imaging Component]","IWICImagingFactory interface","IWICImagingFactory interface [Windows Imaging Component]","CreateColorTransformer method","IWICImagingFactory.CreateColorTransformer","IWICImagingFactory::CreateColorTransformer","_wic_codec_iwicimagingfactory_createcolortransformer","wic._wic_codec_iwicimagingfactory_createcolortransformer","wincodec/IWICImagingFactory::CreateColorTransformer"]
old-location: wic\_wic_codec_iwicimagingfactory_createcolortransformer.htm
tech.root: wic
ms.assetid: 1cbe7987-2845-4d12-92f4-fcdd4ae6f370
ms.date: 12/05/2018
ms.keywords: CreateColorTransformer, CreateColorTransformer method [Windows Imaging Component], CreateColorTransformer method [Windows Imaging Component],IWICImagingFactory interface, IWICImagingFactory interface [Windows Imaging Component],CreateColorTransformer method, IWICImagingFactory.CreateColorTransformer, IWICImagingFactory::CreateColorTransformer, _wic_codec_iwicimagingfactory_createcolortransformer, wic._wic_codec_iwicimagingfactory_createcolortransformer, wincodec/IWICImagingFactory::CreateColorTransformer
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWICImagingFactory::CreateColorTransformer
 - wincodec/IWICImagingFactory::CreateColorTransformer
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Windowscodecs.lib
 - Windowscodecs.dll
api_name:
 - IWICImagingFactory.CreateColorTransformer
---

# IWICImagingFactory::CreateColorTransformer


## -description

Creates a new instance of the <a href="/windows/desktop/api/wincodec/nn-wincodec-iwiccolortransform">IWICColorTransform</a> class.

## -parameters

### -param ppIWICColorTransform [out]

Type: <b><a href="/windows/desktop/api/wincodec/nn-wincodec-iwiccolortransform">IWICColorTransform</a>**</b>

A pointer that receives a pointer to a new <a href="/windows/desktop/api/wincodec/nn-wincodec-iwiccolortransform">IWICColorTransform</a>.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.