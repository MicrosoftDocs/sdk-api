---
UID: NF:wincodec.IWICBitmapEncoder.GetMetadataQueryWriter
title: IWICBitmapEncoder::GetMetadataQueryWriter (wincodec.h)
description: Retrieves a metadata query writer for the encoder.
helpviewer_keywords: ["GetMetadataQueryWriter","GetMetadataQueryWriter method [Windows Imaging Component]","GetMetadataQueryWriter method [Windows Imaging Component]","IWICBitmapEncoder interface","IWICBitmapEncoder interface [Windows Imaging Component]","GetMetadataQueryWriter method","IWICBitmapEncoder.GetMetadataQueryWriter","IWICBitmapEncoder::GetMetadataQueryWriter","_wic_codec_iwicbitmapencoder_getmetadataquerywriter","wic._wic_codec_iwicbitmapencoder_getmetadataquerywriter","wincodec/IWICBitmapEncoder::GetMetadataQueryWriter"]
old-location: wic\_wic_codec_iwicbitmapencoder_getmetadataquerywriter.htm
tech.root: wic
ms.assetid: 11160c48-dbbe-45b6-864c-6a6713ec9ab5
ms.date: 12/05/2018
ms.keywords: GetMetadataQueryWriter, GetMetadataQueryWriter method [Windows Imaging Component], GetMetadataQueryWriter method [Windows Imaging Component],IWICBitmapEncoder interface, IWICBitmapEncoder interface [Windows Imaging Component],GetMetadataQueryWriter method, IWICBitmapEncoder.GetMetadataQueryWriter, IWICBitmapEncoder::GetMetadataQueryWriter, _wic_codec_iwicbitmapencoder_getmetadataquerywriter, wic._wic_codec_iwicbitmapencoder_getmetadataquerywriter, wincodec/IWICBitmapEncoder::GetMetadataQueryWriter
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
 - IWICBitmapEncoder::GetMetadataQueryWriter
 - wincodec/IWICBitmapEncoder::GetMetadataQueryWriter
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
 - IWICBitmapEncoder.GetMetadataQueryWriter
---

# IWICBitmapEncoder::GetMetadataQueryWriter


## -description

Retrieves a metadata query writer for the encoder.

## -parameters

### -param ppIMetadataQueryWriter [out]

Type: <b><a href="/windows/desktop/api/wincodec/nn-wincodec-iwicmetadataquerywriter">IWICMetadataQueryWriter</a>**</b>

When this method returns, contains a pointer to the encoder's metadata query writer.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/wic/-wic-codec-jpegmetadataencoding">How-to: Re-encode a JPEG Image with Metadata</a>



<a href="/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder">IWICBitmapEncoder</a>



<a href="/windows/desktop/wic/-wic-codec-metadataquerylanguage">Metadata Query Language Overview</a>



<a href="/windows/desktop/wic/-wic-codec-readingwritingmetadata">Overview of Reading and Writing Image Metadata</a>



<a href="/windows/desktop/wic/-wic-about-metadata">WIC Metadata Overview</a>