---
UID: NF:wincodec.IWICImagingFactory.CreateDecoderFromStream
title: IWICImagingFactory::CreateDecoderFromStream (wincodec.h)
description: Creates a new instance of the IWICBitmapDecoder class based on the given IStream.
helpviewer_keywords: ["CreateDecoderFromStream","CreateDecoderFromStream method [Windows Imaging Component]","CreateDecoderFromStream method [Windows Imaging Component]","IWICImagingFactory interface","IWICImagingFactory interface [Windows Imaging Component]","CreateDecoderFromStream method","IWICImagingFactory.CreateDecoderFromStream","IWICImagingFactory::CreateDecoderFromStream","_wic_codec_iwicimagingfactory_createdecoderfromstream","wic._wic_codec_iwicimagingfactory_createdecoderfromstream","wincodec/IWICImagingFactory::CreateDecoderFromStream"]
old-location: wic\_wic_codec_iwicimagingfactory_createdecoderfromstream.htm
tech.root: wic
ms.assetid: b9328715-54a0-4c9a-9977-3252068b7e4b
ms.date: 12/05/2018
ms.keywords: CreateDecoderFromStream, CreateDecoderFromStream method [Windows Imaging Component], CreateDecoderFromStream method [Windows Imaging Component],IWICImagingFactory interface, IWICImagingFactory interface [Windows Imaging Component],CreateDecoderFromStream method, IWICImagingFactory.CreateDecoderFromStream, IWICImagingFactory::CreateDecoderFromStream, _wic_codec_iwicimagingfactory_createdecoderfromstream, wic._wic_codec_iwicimagingfactory_createdecoderfromstream, wincodec/IWICImagingFactory::CreateDecoderFromStream
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
 - IWICImagingFactory::CreateDecoderFromStream
 - wincodec/IWICImagingFactory::CreateDecoderFromStream
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
 - IWICImagingFactory.CreateDecoderFromStream
---

# IWICImagingFactory::CreateDecoderFromStream


## -description

Creates a new instance of the <a href="/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapdecoder">IWICBitmapDecoder</a> class based on the given <a href="/windows/desktop/api/objidl/nn-objidl-istream">IStream</a>.

## -parameters

### -param pIStream [in]

Type: <b><a href="/windows/desktop/api/objidl/nn-objidl-istream">IStream</a>*</b>

The stream to create the decoder from.

### -param pguidVendor [in]

Type: <b>const GUID*</b>

The GUID for the preferred decoder vendor. Use <b>NULL</b> if no preferred vendor.

### -param metadataOptions [in]

Type: <b><a href="/windows/desktop/api/wincodec/ne-wincodec-wicdecodeoptions">WICDecodeOptions</a></b>

The <a href="/windows/desktop/api/wincodec/ne-wincodec-wicdecodeoptions">WICDecodeOptions</a> to use when creating the decoder.

### -param ppIDecoder [out, retval]

Type: <b><a href="/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapdecoder">IWICBitmapDecoder</a>**</b>

A pointer that receives a pointer to a new <a href="/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapdecoder">IWICBitmapDecoder</a>.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.