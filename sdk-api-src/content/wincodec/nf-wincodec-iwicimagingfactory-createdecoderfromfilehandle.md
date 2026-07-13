---
UID: NF:wincodec.IWICImagingFactory.CreateDecoderFromFileHandle
title: IWICImagingFactory::CreateDecoderFromFileHandle (wincodec.h)
description: Creates a new instance of the IWICBitmapDecoder based on the given file handle.
helpviewer_keywords: ["CreateDecoderFromFileHandle","CreateDecoderFromFileHandle method [Windows Imaging Component]","CreateDecoderFromFileHandle method [Windows Imaging Component]","IWICImagingFactory interface","IWICImagingFactory interface [Windows Imaging Component]","CreateDecoderFromFileHandle method","IWICImagingFactory.CreateDecoderFromFileHandle","IWICImagingFactory::CreateDecoderFromFileHandle","_wic_codec_iwicimagingfactory_createdecoderfromfilehandle","wic._wic_codec_iwicimagingfactory_createdecoderfromfilehandle","wincodec/IWICImagingFactory::CreateDecoderFromFileHandle"]
old-location: wic\_wic_codec_iwicimagingfactory_createdecoderfromfilehandle.htm
tech.root: wic
ms.assetid: 94cf408c-bcea-419a-bf87-fac1e15e0a12
ms.date: 12/05/2018
ms.keywords: CreateDecoderFromFileHandle, CreateDecoderFromFileHandle method [Windows Imaging Component], CreateDecoderFromFileHandle method [Windows Imaging Component],IWICImagingFactory interface, IWICImagingFactory interface [Windows Imaging Component],CreateDecoderFromFileHandle method, IWICImagingFactory.CreateDecoderFromFileHandle, IWICImagingFactory::CreateDecoderFromFileHandle, _wic_codec_iwicimagingfactory_createdecoderfromfilehandle, wic._wic_codec_iwicimagingfactory_createdecoderfromfilehandle, wincodec/IWICImagingFactory::CreateDecoderFromFileHandle
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
 - IWICImagingFactory::CreateDecoderFromFileHandle
 - wincodec/IWICImagingFactory::CreateDecoderFromFileHandle
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
 - IWICImagingFactory.CreateDecoderFromFileHandle
---

# IWICImagingFactory::CreateDecoderFromFileHandle


## -description

Creates a new instance of the <a href="/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapdecoder">IWICBitmapDecoder</a> based on the given file handle.

## -parameters

### -param hFile [in]

Type: <b>ULONG_PTR</b>

The file handle to create the decoder from.

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

## -remarks

When a decoder is created using this method, the file handle must remain alive during the lifetime of the decoder.

## -see-also

<a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a>



<a href="/windows/desktop/api/wincodec/nn-wincodec-iwicimagingfactory">IWICImagingFactory</a>