---
UID: NF:wincodec.IWICBitmapFrameDecode.GetMetadataQueryReader
title: IWICBitmapFrameDecode::GetMetadataQueryReader (wincodec.h)
description: Retrieves a metadata query reader for the frame.
helpviewer_keywords: ["GetMetadataQueryReader","GetMetadataQueryReader method [Windows Imaging Component]","GetMetadataQueryReader method [Windows Imaging Component]","IWICBitmapFrameDecode interface","IWICBitmapFrameDecode interface [Windows Imaging Component]","GetMetadataQueryReader method","IWICBitmapFrameDecode.GetMetadataQueryReader","IWICBitmapFrameDecode::GetMetadataQueryReader","_wic_codec_iwicbitmapframedecode_getmetadataqueryreader","wic._wic_codec_iwicbitmapframedecode_getmetadataqueryreader","wincodec/IWICBitmapFrameDecode::GetMetadataQueryReader"]
old-location: wic\_wic_codec_iwicbitmapframedecode_getmetadataqueryreader.htm
tech.root: wic
ms.assetid: e28de664-f9f1-4cf1-b2a7-f310548a3786
ms.date: 12/05/2018
ms.keywords: GetMetadataQueryReader, GetMetadataQueryReader method [Windows Imaging Component], GetMetadataQueryReader method [Windows Imaging Component],IWICBitmapFrameDecode interface, IWICBitmapFrameDecode interface [Windows Imaging Component],GetMetadataQueryReader method, IWICBitmapFrameDecode.GetMetadataQueryReader, IWICBitmapFrameDecode::GetMetadataQueryReader, _wic_codec_iwicbitmapframedecode_getmetadataqueryreader, wic._wic_codec_iwicbitmapframedecode_getmetadataqueryreader, wincodec/IWICBitmapFrameDecode::GetMetadataQueryReader
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
 - IWICBitmapFrameDecode::GetMetadataQueryReader
 - wincodec/IWICBitmapFrameDecode::GetMetadataQueryReader
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
 - IWICBitmapFrameDecode.GetMetadataQueryReader
---

# IWICBitmapFrameDecode::GetMetadataQueryReader


## -description

Retrieves a metadata query reader for the frame.

## -parameters

### -param ppIMetadataQueryReader [out]

Type: <b><a href="/windows/desktop/api/wincodec/nn-wincodec-iwicmetadataqueryreader">IWICMetadataQueryReader</a>**</b>

When this method returns, contains a pointer to the frame's metadata query reader.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

For image formats with one frame (JPG, PNG, JPEG-XR), the frame-level query reader of the first frame is used to access all image metadata, and the decoder-level query reader isn’t used. For formats with more than one frame (GIF, TIFF), the frame-level query reader for a given frame is used to access metadata specific to that frame, and in the case of GIF a decoder-level metadata reader will be present. If the decoder doesn’t support metadata (BMP, ICO), this will return <a href="/windows/desktop/wic/-wic-codec-error-codes">WINCODEC_ERR_UNSUPPORTEDOPERATION</a>.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapframedecode">IWICBitmapFrameDecode</a>



<a href="/windows/desktop/wic/-wic-codec-metadataquerylanguage">Metadata Query Language Overview</a>



<a href="/windows/desktop/wic/-wic-codec-readingwritingmetadata">Overview of Reading and Writing Image Metadata</a>



<a href="/windows/desktop/wic/-wic-about-metadata">WIC Metadata Overview</a>