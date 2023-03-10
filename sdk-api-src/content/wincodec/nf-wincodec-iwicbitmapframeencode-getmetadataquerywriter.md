---
UID: NF:wincodec.IWICBitmapFrameEncode.GetMetadataQueryWriter
title: IWICBitmapFrameEncode::GetMetadataQueryWriter (wincodec.h)
description: Gets the metadata query writer for the encoder frame.
helpviewer_keywords: ["GetMetadataQueryWriter","GetMetadataQueryWriter method [Windows Imaging Component]","GetMetadataQueryWriter method [Windows Imaging Component]","IWICBitmapFrameEncode interface","IWICBitmapFrameEncode interface [Windows Imaging Component]","GetMetadataQueryWriter method","IWICBitmapFrameEncode.GetMetadataQueryWriter","IWICBitmapFrameEncode::GetMetadataQueryWriter","_wic_codec_iwicbitmapframeencode_getmetadataquerywriter","wic._wic_codec_iwicbitmapframeencode_getmetadataquerywriter","wincodec/IWICBitmapFrameEncode::GetMetadataQueryWriter"]
old-location: wic\_wic_codec_iwicbitmapframeencode_getmetadataquerywriter.htm
tech.root: wic
ms.assetid: 0ff79820-5f44-4262-b97f-df783829e44b
ms.date: 12/05/2018
ms.keywords: GetMetadataQueryWriter, GetMetadataQueryWriter method [Windows Imaging Component], GetMetadataQueryWriter method [Windows Imaging Component],IWICBitmapFrameEncode interface, IWICBitmapFrameEncode interface [Windows Imaging Component],GetMetadataQueryWriter method, IWICBitmapFrameEncode.GetMetadataQueryWriter, IWICBitmapFrameEncode::GetMetadataQueryWriter, _wic_codec_iwicbitmapframeencode_getmetadataquerywriter, wic._wic_codec_iwicbitmapframeencode_getmetadataquerywriter, wincodec/IWICBitmapFrameEncode::GetMetadataQueryWriter
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
 - IWICBitmapFrameEncode::GetMetadataQueryWriter
 - wincodec/IWICBitmapFrameEncode::GetMetadataQueryWriter
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
 - IWICBitmapFrameEncode.GetMetadataQueryWriter
---

# IWICBitmapFrameEncode::GetMetadataQueryWriter


## -description

Gets the metadata query writer for the encoder frame.

## -parameters

### -param ppIMetadataQueryWriter [out]

Type: <b><a href="/windows/desktop/api/wincodec/nn-wincodec-iwicmetadataquerywriter">IWICMetadataQueryWriter</a>**</b>

When this method returns, contains a pointer to metadata query writer for the encoder frame.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

If you are setting metadata on the frame, you must do this before you use <a href="/windows/desktop/api/wincodec/nf-wincodec-iwicbitmapframeencode-writepixels">IWICBitmapFrameEncode::WritePixels</a> or <a href="/windows/desktop/api/wincodec/nf-wincodec-iwicbitmapframeencode-writesource">IWICBitmapFrameEncode::WriteSource</a> to write any image pixels to the frame

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/wic/-wic-codec-jpegmetadataencoding">How-to: Re-encode a JPEG Image with Metadata</a>



<a href="/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapframeencode">IWICBitmapFrameEncode</a>



<a href="/windows/desktop/wic/-wic-codec-metadataquerylanguage">Metadata Query Language Overview</a>



<a href="/windows/desktop/wic/-wic-codec-readingwritingmetadata">Overview of Reading and Writing Image Metadata</a>



<a href="/windows/desktop/wic/-wic-about-metadata">WIC Metadata Overview</a>