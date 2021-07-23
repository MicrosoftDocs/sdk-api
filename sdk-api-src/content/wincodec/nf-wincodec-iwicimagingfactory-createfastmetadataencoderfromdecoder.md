---
UID: NF:wincodec.IWICImagingFactory.CreateFastMetadataEncoderFromDecoder
title: IWICImagingFactory::CreateFastMetadataEncoderFromDecoder (wincodec.h)
description: Creates a new instance of the fast metadata encoder based on the given IWICBitmapDecoder.
helpviewer_keywords: ["CreateFastMetadataEncoderFromDecoder","CreateFastMetadataEncoderFromDecoder method [Windows Imaging Component]","CreateFastMetadataEncoderFromDecoder method [Windows Imaging Component]","IWICImagingFactory interface","IWICImagingFactory interface [Windows Imaging Component]","CreateFastMetadataEncoderFromDecoder method","IWICImagingFactory.CreateFastMetadataEncoderFromDecoder","IWICImagingFactory::CreateFastMetadataEncoderFromDecoder","_wic_codec_iwicimagingfactory_createfastmetadataencoderfromdecoder","wic._wic_codec_iwicimagingfactory_createfastmetadataencoderfromdecoder","wincodec/IWICImagingFactory::CreateFastMetadataEncoderFromDecoder"]
old-location: wic\_wic_codec_iwicimagingfactory_createfastmetadataencoderfromdecoder.htm
tech.root: wic
ms.assetid: 3264a987-4308-4c50-b99c-70142bc49476
ms.date: 12/05/2018
ms.keywords: CreateFastMetadataEncoderFromDecoder, CreateFastMetadataEncoderFromDecoder method [Windows Imaging Component], CreateFastMetadataEncoderFromDecoder method [Windows Imaging Component],IWICImagingFactory interface, IWICImagingFactory interface [Windows Imaging Component],CreateFastMetadataEncoderFromDecoder method, IWICImagingFactory.CreateFastMetadataEncoderFromDecoder, IWICImagingFactory::CreateFastMetadataEncoderFromDecoder, _wic_codec_iwicimagingfactory_createfastmetadataencoderfromdecoder, wic._wic_codec_iwicimagingfactory_createfastmetadataencoderfromdecoder, wincodec/IWICImagingFactory::CreateFastMetadataEncoderFromDecoder
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
 - IWICImagingFactory::CreateFastMetadataEncoderFromDecoder
 - wincodec/IWICImagingFactory::CreateFastMetadataEncoderFromDecoder
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
 - IWICImagingFactory.CreateFastMetadataEncoderFromDecoder
---

# IWICImagingFactory::CreateFastMetadataEncoderFromDecoder


## -description

Creates a new instance of the fast metadata encoder based on the given <a href="/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapdecoder">IWICBitmapDecoder</a>.

## -parameters

### -param pIDecoder [in]

Type: <b><a href="/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapdecoder">IWICBitmapDecoder</a>*</b>

The decoder to create the fast metadata encoder from.

### -param ppIFastEncoder [out]

Type: <b><a href="/windows/desktop/api/wincodec/nn-wincodec-iwicfastmetadataencoder">IWICFastMetadataEncoder</a>**</b>

When this method returns, contains a pointer to the new <a href="/windows/desktop/api/wincodec/nn-wincodec-iwicfastmetadataencoder">IWICFastMetadataEncoder</a>.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The Windows provided codecs do not support fast metadata encoding at the decoder level, and only support fast metadata encoding at the frame level. To create a fast metadata encoder from a frame, see <a href="/windows/desktop/api/wincodec/nf-wincodec-iwicimagingfactory-createfastmetadataencoderfromframedecode">CreateFastMetadataEncoderFromFrameDecode</a>.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/wincodec/nn-wincodec-iwicimagingfactory">IWICImagingFactory</a>



<a href="/windows/desktop/wic/-wic-codec-metadataquerylanguage">Metadata Query Language Overview</a>



<a href="/windows/desktop/wic/-wic-codec-readingwritingmetadata">Overview of Reading and Writing Image Metadata</a>



<a href="/windows/desktop/wic/-wic-about-metadata">WIC Metadata Overview</a>