---
UID: NN:wincodecsdk.IWICMetadataBlockWriter
title: IWICMetadataBlockWriter (wincodecsdk.h)
author: windows-sdk-content
description: Exposes methods that enable the encoding of metadata. This interface is implemented by the decoder and its image frames.
old-location: wic\_wic_codec_iwicmetadatablockwriter.htm
tech.root: wic
ms.assetid: d8e44c64-dd58-4d36-8add-0a0b2e2af5a4
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IWICMetadataBlockWriter, IWICMetadataBlockWriter interface [Windows Imaging Component], IWICMetadataBlockWriter interface [Windows Imaging Component],described, _wic_codec_iwicmetadatablockwriter, wic._wic_codec_iwicmetadatablockwriter, wincodecsdk/IWICMetadataBlockWriter
ms.topic: interface
f1_keywords: 
 - "wincodecsdk/IWICMetadataBlockWriter"
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
 - IWICMetadataBlockWriter
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWICMetadataBlockWriter interface


## -description


Exposes methods that enable the encoding of metadata. This interface is implemented by the decoder and its image frames.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWICMetadataBlockWriter</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader">IWICMetadataBlockReader</a>. <b>IWICMetadataBlockWriter</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWICMetadataBlockWriter</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wincodecsdk/nf-wincodecsdk-iwicmetadatablockwriter-addwriter">AddWriter</a>
</td>
<td align="left" width="63%">
Adds a top-level metadata block by adding a <a href="https://docs.microsoft.com/windows/desktop/api/wincodecsdk/nn-wincodecsdk-iwicmetadatawriter">IWICMetadataWriter</a> for it.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wincodecsdk/nf-wincodecsdk-iwicmetadatablockwriter-getwriterbyindex">GetWriterByIndex</a>
</td>
<td align="left" width="63%">
Retrieves the <a href="https://docs.microsoft.com/windows/desktop/api/wincodecsdk/nn-wincodecsdk-iwicmetadatawriter">IWICMetadataWriter</a> that resides at the specified index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wincodecsdk/nf-wincodecsdk-iwicmetadatablockwriter-initializefromblockreader">InitializeFromBlockReader</a>
</td>
<td align="left" width="63%">
Initializes an <b>IWICMetadataBlockWriter</b> from the given <a href="https://docs.microsoft.com/windows/desktop/api/wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader">IWICMetadataBlockReader</a>. This will prepopulate the metadata block writer with all the metadata in the metadata block reader.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wincodecsdk/nf-wincodecsdk-iwicmetadatablockwriter-removewriterbyindex">RemoveWriterByIndex</a>
</td>
<td align="left" width="63%">
Removes the metadata writer from the specified index location.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wincodecsdk/nf-wincodecsdk-iwicmetadatablockwriter-setwriterbyindex">SetWriterByIndex</a>
</td>
<td align="left" width="63%">
Replaces the metadata writer at the specified index location.

</td>
</tr>
</table> 


## -remarks



When the encoder is told to commit, it goes through each metadata writer and serializes the metadata content into the encoding stream.
            If the metadata block contains metadata important to the integrity of the file, such as the image width or height or other intrinsic information about the image, the encoder must set the critical metadata items prior to serializing the metadata.
         




## -see-also




<b>Conceptual</b>



<a href="https://docs.microsoft.com/windows/desktop/wic/-wic-howtowriteacodec">How to Write a WIC-Enabled CODEC</a>



<a href="https://docs.microsoft.com/windows/desktop/wic/-wic-codec-jpegmetadataencoding">How-to: Re-encode a JPEG Image with Metadata</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader">IWICMetadataBlockReader</a>



<b>Other Resources</b>



<a href="https://docs.microsoft.com/windows/desktop/wic/-wic-codec-readingwritingmetadata">Overview of Reading and Writing Image Metadata</a>



<a href="https://docs.microsoft.com/windows/desktop/wic/-wic-about-metadata">WIC Metadata Overview</a>
 

 

