---
UID: NF:wincodec.IWICImagingFactory.CreateStream
title: IWICImagingFactory::CreateStream (wincodec.h)
description: Creates a new instance of the IWICStream class.
helpviewer_keywords: ["CreateStream","CreateStream method [Windows Imaging Component]","CreateStream method [Windows Imaging Component]","IWICImagingFactory interface","IWICImagingFactory interface [Windows Imaging Component]","CreateStream method","IWICImagingFactory.CreateStream","IWICImagingFactory::CreateStream","_wic_codec_iwicimagingfactory_createstream","wic._wic_codec_iwicimagingfactory_createstream","wincodec/IWICImagingFactory::CreateStream"]
old-location: wic\_wic_codec_iwicimagingfactory_createstream.htm
tech.root: wic
ms.assetid: 1c2ecaf0-5222-4f9b-96fb-5d2da72d11d4
ms.date: 12/05/2018
ms.keywords: CreateStream, CreateStream method [Windows Imaging Component], CreateStream method [Windows Imaging Component],IWICImagingFactory interface, IWICImagingFactory interface [Windows Imaging Component],CreateStream method, IWICImagingFactory.CreateStream, IWICImagingFactory::CreateStream, _wic_codec_iwicimagingfactory_createstream, wic._wic_codec_iwicimagingfactory_createstream, wincodec/IWICImagingFactory::CreateStream
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
 - IWICImagingFactory::CreateStream
 - wincodec/IWICImagingFactory::CreateStream
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
 - IWICImagingFactory.CreateStream
---

# IWICImagingFactory::CreateStream


## -description

Creates a new instance of the <a href="/windows/desktop/api/wincodec/nn-wincodec-iwicstream">IWICStream</a> class.

## -parameters

### -param ppIWICStream [out]

Type: <b><a href="/windows/desktop/api/wincodec/nn-wincodec-iwicstream">IWICStream</a>**</b>

A pointer that receives a pointer to a new <a href="/windows/desktop/api/wincodec/nn-wincodec-iwicstream">IWICStream</a>.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.