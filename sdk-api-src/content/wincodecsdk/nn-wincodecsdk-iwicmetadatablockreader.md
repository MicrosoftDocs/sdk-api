---
UID: NN:wincodecsdk.IWICMetadataBlockReader
title: IWICMetadataBlockReader (wincodecsdk.h)
description: Exposes methods that provide access to all of the codec's top level metadata blocks.
helpviewer_keywords: ["IWICMetadataBlockReader","IWICMetadataBlockReader interface [Windows Imaging Component]","IWICMetadataBlockReader interface [Windows Imaging Component]","described","_wic_codec_iwicmetadatablockreader","wic._wic_codec_iwicmetadatablockreader","wincodecsdk/IWICMetadataBlockReader"]
old-location: wic\_wic_codec_iwicmetadatablockreader.htm
tech.root: wic
ms.assetid: 09614b44-ebc2-44f4-9755-9df62f1b2178
ms.date: 12/05/2018
ms.keywords: IWICMetadataBlockReader, IWICMetadataBlockReader interface [Windows Imaging Component], IWICMetadataBlockReader interface [Windows Imaging Component],described, _wic_codec_iwicmetadatablockreader, wic._wic_codec_iwicmetadatablockreader, wincodecsdk/IWICMetadataBlockReader
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
 - IWICMetadataBlockReader
 - wincodecsdk/IWICMetadataBlockReader
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
 - IWICMetadataBlockReader
---

# IWICMetadataBlockReader interface


## -description

Exposes methods that provide access to all of the codec's top level metadata blocks.

## -inheritance

The <b>IWICMetadataBlockReader</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWICMetadataBlockReader</b> also has these types of members:

## -remarks

<b>IWICMetadataBlockReader</b> and <a href="/windows/desktop/api/wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter">IWICMetadataBlockWriter</a> operate at the root level only; that is, they provide read and write access, respectively, to the top level metadata blocks. They are implemented by <a href="/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapframedecode">IWICBitmapFrameDecode</a> and <a href="/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapframeencode">IWICBitmapFrameEncode</a>, respectively. To handle any metadata blocks that are not at the top level of the hierarchy, use <a href="/windows/desktop/api/wincodecsdk/nn-wincodecsdk-iwicmetadatareader">IWICMetadataReader</a> or <a href="/windows/desktop/api/wincodecsdk/nn-wincodecsdk-iwicmetadatawriter">IWICMetadataWriter</a>.


<div class="alert"><b>Note</b>  The codec's decoder and encoder implement this interface to expose the enumeration of all top level metadata blocks.  While the codec parses the image stream, it calls services like <a href="/windows/desktop/api/wincodecsdk/nf-wincodecsdk-iwiccomponentfactory-createmetadatareaderfromcontainer">CreateMetadataReaderFromContainer</a> to instantiate metadata readers for any block that is recognized as being able to be embedded in the decoder's container format.  The collection of metadata readers is exposed through this interface. For more info, see <a href="/windows/desktop/wic/-wic-howtowriteacodec">How to Write a WIC-Enabled CODEC</a>.</div>
<div> </div>

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/wic/-wic-codec-metadatahandlers">Metadata Extensibility Overview</a>



<a href="/windows/desktop/wic/-wic-codec-readingwritingmetadata">Overview of Reading and Writing Image Metadata</a>



<a href="/windows/desktop/wic/-wic-about-metadata">WIC Metadata Overview</a>
