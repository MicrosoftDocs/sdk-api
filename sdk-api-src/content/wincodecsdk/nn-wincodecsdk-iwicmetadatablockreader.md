---
UID: NN:wincodecsdk.IWICMetadataBlockReader
title: IWICMetadataBlockReader (wincodecsdk.h)
description: Exposes methods that provide access to all of the codec's top level metadata blocks.
old-location: wic\_wic_codec_iwicmetadatablockreader.htm
tech.root: wic
ms.assetid: 09614b44-ebc2-44f4-9755-9df62f1b2178
ms.date: 12/05/2018
ms.keywords: IWICMetadataBlockReader, IWICMetadataBlockReader interface [Windows Imaging Component], IWICMetadataBlockReader interface [Windows Imaging Component],described, _wic_codec_iwicmetadatablockreader, wic._wic_codec_iwicmetadatablockreader, wincodecsdk/IWICMetadataBlockReader
ms.topic: interface
f1_keywords:
- wincodecsdk/IWICMetadataBlockReader
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Windowscodecs.dll
api_name:
- IWICMetadataBlockReader
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWICMetadataBlockReader interface


## -description


Exposes methods that provide access to all of the codec's top level metadata blocks.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWICMetadataBlockReader</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWICMetadataBlockReader</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWICMetadataBlockReader</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wincodecsdk/nf-wincodecsdk-iwicmetadatablockreader-getcontainerformat">GetContainerFormat</a>
</td>
<td align="left" width="63%">
Retrieves the container format of the decoder.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wincodecsdk/nf-wincodecsdk-iwicmetadatablockreader-getcount">GetCount</a>
</td>
<td align="left" width="63%">
Retrieves the number of top level metadata blocks.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wincodecsdk/nf-wincodecsdk-iwicmetadatablockreader-getenumerator">GetEnumerator</a>
</td>
<td align="left" width="63%">
Retrieves an enumeration of each of the top level metadata blocks.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wincodecsdk/nf-wincodecsdk-iwicmetadatablockreader-getreaderbyindex">GetReaderByIndex</a>
</td>
<td align="left" width="63%">
Retrieves an <a href="https://docs.microsoft.com/windows/desktop/api/wincodecsdk/nn-wincodecsdk-iwicmetadatareader">IWICMetadataReader</a> for a specified top level metadata block, providing access to the embedded metadata blocks.

</td>
</tr>
</table> 


## -remarks



<b>IWICMetadataBlockReader</b> and <a href="https://docs.microsoft.com/windows/desktop/api/wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter">IWICMetadataBlockWriter</a> operate at the root level only; that is, they provide read and write access, respectively, to the top level metadata blocks. They are implemented by <a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapframedecode">IWICBitmapFrameDecode</a> and <a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapframeencode">IWICBitmapFrameEncode</a>, respectively. To handle any metadata blocks that are not at the top level of the hierarchy, use <a href="https://docs.microsoft.com/windows/desktop/api/wincodecsdk/nn-wincodecsdk-iwicmetadatareader">IWICMetadataReader</a> or <a href="https://docs.microsoft.com/windows/desktop/api/wincodecsdk/nn-wincodecsdk-iwicmetadatawriter">IWICMetadataWriter</a>.


<div class="alert"><b>Note</b>  The codec's decoder and encoder implement this interface to expose the enumeration of all top level metadata blocks.  While the codec parses the image stream, it calls services like <a href="https://docs.microsoft.com/windows/desktop/api/wincodecsdk/nf-wincodecsdk-iwiccomponentfactory-createmetadatareaderfromcontainer">CreateMetadataReaderFromContainer</a> to instantiate metadata readers for any block that is recognized as being able to be embedded in the decoder's container format.  The collection of metadata readers is exposed through this interface. For more info, see <a href="https://docs.microsoft.com/windows/desktop/wic/-wic-howtowriteacodec">How to Write a WIC-Enabled CODEC</a>.</div>
<div> </div>



## -see-also




<b>Conceptual</b>



<a href="https://docs.microsoft.com/windows/desktop/wic/-wic-codec-metadatahandlers">Metadata Extensibility Overview</a>



<a href="https://docs.microsoft.com/windows/desktop/wic/-wic-codec-readingwritingmetadata">Overview of Reading and Writing Image Metadata</a>



<a href="https://docs.microsoft.com/windows/desktop/wic/-wic-about-metadata">WIC Metadata Overview</a>
 

 

