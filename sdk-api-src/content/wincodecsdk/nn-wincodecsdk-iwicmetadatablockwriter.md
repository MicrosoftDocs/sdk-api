---
UID: NN:wincodecsdk.IWICMetadataBlockWriter
title: IWICMetadataBlockWriter (wincodecsdk.h)
description: Exposes methods that enable the encoding of metadata. This interface is implemented by the decoder and its image frames.
helpviewer_keywords: ["IWICMetadataBlockWriter","IWICMetadataBlockWriter interface [Windows Imaging Component]","IWICMetadataBlockWriter interface [Windows Imaging Component]","described","_wic_codec_iwicmetadatablockwriter","wic._wic_codec_iwicmetadatablockwriter","wincodecsdk/IWICMetadataBlockWriter"]
old-location: wic\_wic_codec_iwicmetadatablockwriter.htm
tech.root: wic
ms.assetid: d8e44c64-dd58-4d36-8add-0a0b2e2af5a4
ms.date: 12/05/2018
ms.keywords: IWICMetadataBlockWriter, IWICMetadataBlockWriter interface [Windows Imaging Component], IWICMetadataBlockWriter interface [Windows Imaging Component],described, _wic_codec_iwicmetadatablockwriter, wic._wic_codec_iwicmetadatablockwriter, wincodecsdk/IWICMetadataBlockWriter
req.header: wincodecsdk.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wincodecsdk.idl
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
 - IWICMetadataBlockWriter
 - wincodecsdk/IWICMetadataBlockWriter
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
 - IWICMetadataBlockWriter
---

# IWICMetadataBlockWriter interface


## -description

Exposes methods that enable the encoding of metadata. This interface is implemented by the decoder and its image frames.

## -inheritance

The <b>IWICMetadataBlockWriter</b> interface inherits from <a href="/windows/desktop/api/wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader">IWICMetadataBlockReader</a>. <b>IWICMetadataBlockWriter</b> also has these types of members:

## -remarks

When the encoder is told to commit, it goes through each metadata writer and serializes the metadata content into the encoding stream.
            If the metadata block contains metadata important to the integrity of the file, such as the image width or height or other intrinsic information about the image, the encoder must set the critical metadata items prior to serializing the metadata.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/wic/-wic-howtowriteacodec">How to Write a WIC-Enabled CODEC</a>



<a href="/windows/desktop/wic/-wic-codec-jpegmetadataencoding">How-to: Re-encode a JPEG Image with Metadata</a>



<a href="/windows/desktop/api/wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader">IWICMetadataBlockReader</a>



<b>Other Resources</b>



<a href="/windows/desktop/wic/-wic-codec-readingwritingmetadata">Overview of Reading and Writing Image Metadata</a>



<a href="/windows/desktop/wic/-wic-about-metadata">WIC Metadata Overview</a>
