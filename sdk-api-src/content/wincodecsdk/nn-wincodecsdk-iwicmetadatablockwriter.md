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
---

# IWICMetadataBlockWriter interface


## -description


Exposes methods that enable the encoding of metadata. This interface is implemented by the decoder and its image frames.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWICMetadataBlockWriter</b> interface inherits from <a href="https://msdn.microsoft.com/09614b44-ebc2-44f4-9755-9df62f1b2178">IWICMetadataBlockReader</a>. <b>IWICMetadataBlockWriter</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/25a0e662-a249-4218-a77e-37b11e0f8536">AddWriter</a>
</td>
<td align="left" width="63%">
Adds a top-level metadata block by adding a <a href="https://msdn.microsoft.com/7e742a96-f9d0-49e1-80e4-31ec90680e60">IWICMetadataWriter</a> for it.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/14c8acb1-484a-46ad-8a38-79a4b1cfe0d1">GetWriterByIndex</a>
</td>
<td align="left" width="63%">
Retrieves the <a href="https://msdn.microsoft.com/7e742a96-f9d0-49e1-80e4-31ec90680e60">IWICMetadataWriter</a> that resides at the specified index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9ad9d818-7b3e-47eb-bc99-e26e7664383c">InitializeFromBlockReader</a>
</td>
<td align="left" width="63%">
Initializes an <b>IWICMetadataBlockWriter</b> from the given <a href="https://msdn.microsoft.com/09614b44-ebc2-44f4-9755-9df62f1b2178">IWICMetadataBlockReader</a>. This will prepopulate the metadata block writer with all the metadata in the metadata block reader.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/030c5b0e-5db7-40ae-889c-2e1335d2c50b">RemoveWriterByIndex</a>
</td>
<td align="left" width="63%">
Removes the metadata writer from the specified index location.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cf8f45ee-44ca-431c-b9c2-1b00c5574afe">SetWriterByIndex</a>
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



<a href="https://msdn.microsoft.com/58f03dc2-cc31-4d76-b75a-f332da1f900f">How to Write a WIC-Enabled CODEC</a>



<a href="https://msdn.microsoft.com/a7cfaa6d-e17d-458a-ae63-72963615bef8">How-to: Re-encode a JPEG Image with Metadata</a>



<a href="https://msdn.microsoft.com/09614b44-ebc2-44f4-9755-9df62f1b2178">IWICMetadataBlockReader</a>



<b>Other Resources</b>



<a href="https://msdn.microsoft.com/b1e0b936-a13a-42dd-8470-957ba1d90423">Overview of Reading and Writing Image Metadata</a>



<a href="https://msdn.microsoft.com/35727810-3c4c-4c11-a4a2-3ae2cf3b8142">WIC Metadata Overview</a>
 

 

