---
UID: NF:wincodec.IWICImagingFactory.CreateColorContext
title: IWICImagingFactory::CreateColorContext (wincodec.h)
description: Creates a new instance of the IWICColorContext class.
helpviewer_keywords: ["CreateColorContext","CreateColorContext method [Windows Imaging Component]","CreateColorContext method [Windows Imaging Component]","IWICImagingFactory interface","IWICImagingFactory interface [Windows Imaging Component]","CreateColorContext method","IWICImagingFactory.CreateColorContext","IWICImagingFactory::CreateColorContext","_wic_codec_iwicimagingfactory_createcolorcontext","wic._wic_codec_iwicimagingfactory_createcolorcontext","wincodec/IWICImagingFactory::CreateColorContext"]
old-location: wic\_wic_codec_iwicimagingfactory_createcolorcontext.htm
tech.root: wic
ms.assetid: 60ae0ec4-2bf4-43f0-9882-ff8b6f5f5923
ms.date: 12/05/2018
ms.keywords: CreateColorContext, CreateColorContext method [Windows Imaging Component], CreateColorContext method [Windows Imaging Component],IWICImagingFactory interface, IWICImagingFactory interface [Windows Imaging Component],CreateColorContext method, IWICImagingFactory.CreateColorContext, IWICImagingFactory::CreateColorContext, _wic_codec_iwicimagingfactory_createcolorcontext, wic._wic_codec_iwicimagingfactory_createcolorcontext, wincodec/IWICImagingFactory::CreateColorContext
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
 - IWICImagingFactory::CreateColorContext
 - wincodec/IWICImagingFactory::CreateColorContext
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
 - IWICImagingFactory.CreateColorContext
---

# IWICImagingFactory::CreateColorContext


## -description

Creates a new instance of the <a href="/windows/desktop/api/wincodec/nn-wincodec-iwiccolorcontext">IWICColorContext</a> class.

## -parameters

### -param ppIWICColorContext [out]

Type: <b><a href="/windows/desktop/api/wincodec/nn-wincodec-iwiccolorcontext">IWICColorContext</a>**</b>

A pointer that receives a pointer to a new <a href="/windows/desktop/api/wincodec/nn-wincodec-iwiccolorcontext">IWICColorContext</a>.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.