---
UID: NF:wincodec.IWICBitmapDecoder.GetMetadataQueryReader
title: IWICBitmapDecoder::GetMetadataQueryReader (wincodec.h)
description: Retrieves the metadata query reader from the decoder.
helpviewer_keywords: ["GetMetadataQueryReader","GetMetadataQueryReader method [Windows Imaging Component]","GetMetadataQueryReader method [Windows Imaging Component]","IWICBitmapDecoder interface","IWICBitmapDecoder interface [Windows Imaging Component]","GetMetadataQueryReader method","IWICBitmapDecoder.GetMetadataQueryReader","IWICBitmapDecoder::GetMetadataQueryReader","_wic_codec_iwicbitmapdecoder_getmetadataqueryreader","wic._wic_codec_iwicbitmapdecoder_getmetadataqueryreader","wincodec/IWICBitmapDecoder::GetMetadataQueryReader"]
old-location: wic\_wic_codec_iwicbitmapdecoder_getmetadataqueryreader.htm
tech.root: wic
ms.assetid: 353ce6d8-ef33-44b6-ab8a-7c5903a024f6
ms.date: 12/05/2018
ms.keywords: GetMetadataQueryReader, GetMetadataQueryReader method [Windows Imaging Component], GetMetadataQueryReader method [Windows Imaging Component],IWICBitmapDecoder interface, IWICBitmapDecoder interface [Windows Imaging Component],GetMetadataQueryReader method, IWICBitmapDecoder.GetMetadataQueryReader, IWICBitmapDecoder::GetMetadataQueryReader, _wic_codec_iwicbitmapdecoder_getmetadataqueryreader, wic._wic_codec_iwicbitmapdecoder_getmetadataqueryreader, wincodec/IWICBitmapDecoder::GetMetadataQueryReader
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
 - IWICBitmapDecoder::GetMetadataQueryReader
 - wincodec/IWICBitmapDecoder::GetMetadataQueryReader
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
 - IWICBitmapDecoder.GetMetadataQueryReader
---

# IWICBitmapDecoder::GetMetadataQueryReader


## -description

Retrieves the metadata query reader from the decoder.

## -parameters

### -param ppIMetadataQueryReader [out]

Type: <b><a href="/windows/desktop/api/wincodec/nn-wincodec-iwicmetadataqueryreader">IWICMetadataQueryReader</a>**</b>

Receives a pointer to the decoder's <a href="/windows/desktop/api/wincodec/nn-wincodec-iwicmetadataqueryreader">IWICMetadataQueryReader</a>.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

If an image format does not support container-level metadata, this will return <a href="/windows/desktop/wic/-wic-codec-error-codes">WINCODEC_ERR_UNSUPPORTEDOPERATION</a>. The only Windows provided image format that supports container-level metadata is GIF. Instead, use <a href="/windows/desktop/api/wincodec/nf-wincodec-iwicbitmapframedecode-getmetadataqueryreader">IWICBitmapFrameDecode::GetMetadataQueryReader</a>.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapdecoder">IWICBitmapDecoder</a>



<a href="/windows/desktop/wic/-wic-codec-metadataquerylanguage">Metadata Query Language Overview</a>



<a href="/windows/desktop/wic/-wic-codec-readingwritingmetadata">Overview of Reading and Writing Image Metadata</a>



<a href="/windows/desktop/wic/-wic-about-metadata">WIC Metadata Overview</a>