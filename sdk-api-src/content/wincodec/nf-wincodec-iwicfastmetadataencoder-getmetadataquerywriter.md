---
UID: NF:wincodec.IWICFastMetadataEncoder.GetMetadataQueryWriter
title: IWICFastMetadataEncoder::GetMetadataQueryWriter (wincodec.h)
description: Retrieves a metadata query writer for fast metadata encoding.
helpviewer_keywords: ["GetMetadataQueryWriter","GetMetadataQueryWriter method [Windows Imaging Component]","GetMetadataQueryWriter method [Windows Imaging Component]","IWICFastMetadataEncoder interface","IWICFastMetadataEncoder interface [Windows Imaging Component]","GetMetadataQueryWriter method","IWICFastMetadataEncoder.GetMetadataQueryWriter","IWICFastMetadataEncoder::GetMetadataQueryWriter","_wic_codec_iwicfastmetadataencoder_getmetadataquerywriter","wic._wic_codec_iwicfastmetadataencoder_getmetadataquerywriter","wincodec/IWICFastMetadataEncoder::GetMetadataQueryWriter"]
old-location: wic\_wic_codec_iwicfastmetadataencoder_getmetadataquerywriter.htm
tech.root: wic
ms.assetid: 1d8a0993-101a-4aa5-9e2f-c3f95b9d3d3f
ms.date: 12/05/2018
ms.keywords: GetMetadataQueryWriter, GetMetadataQueryWriter method [Windows Imaging Component], GetMetadataQueryWriter method [Windows Imaging Component],IWICFastMetadataEncoder interface, IWICFastMetadataEncoder interface [Windows Imaging Component],GetMetadataQueryWriter method, IWICFastMetadataEncoder.GetMetadataQueryWriter, IWICFastMetadataEncoder::GetMetadataQueryWriter, _wic_codec_iwicfastmetadataencoder_getmetadataquerywriter, wic._wic_codec_iwicfastmetadataencoder_getmetadataquerywriter, wincodec/IWICFastMetadataEncoder::GetMetadataQueryWriter
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
 - IWICFastMetadataEncoder::GetMetadataQueryWriter
 - wincodec/IWICFastMetadataEncoder::GetMetadataQueryWriter
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
 - IWICFastMetadataEncoder.GetMetadataQueryWriter
---

# IWICFastMetadataEncoder::GetMetadataQueryWriter


## -description

Retrieves a metadata query writer for fast metadata encoding.

## -parameters

### -param ppIMetadataQueryWriter [out]

Type: <b><a href="/windows/desktop/api/wincodec/nn-wincodec-iwicmetadataquerywriter">IWICMetadataQueryWriter</a>**</b>

When this method returns, contains a pointer to the fast metadata encoder's metadata query writer.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/wincodec/nn-wincodec-iwicfastmetadataencoder">IWICFastMetadataEncoder</a>



<a href="/windows/desktop/wic/-wic-codec-metadataquerylanguage">Metadata Query Language Overview</a>



<a href="/windows/desktop/wic/-wic-codec-readingwritingmetadata">Overview of Reading and Writing Image Metadata</a>



<a href="/windows/desktop/wic/-wic-about-metadata">WIC Metadata Overview</a>