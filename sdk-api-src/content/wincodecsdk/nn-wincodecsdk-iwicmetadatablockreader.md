---
UID: NN:wincodecsdk.IWICMetadataBlockReader
title: IWICMetadataBlockReader
author: windows-sdk-content
description: Exposes methods that provide access to all of the codec's top level metadata blocks.
old-location: wic\_wic_codec_iwicmetadatablockreader.htm
tech.root: wic
ms.assetid: 09614b44-ebc2-44f4-9755-9df62f1b2178
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IWICMetadataBlockReader, IWICMetadataBlockReader interface [Windows Imaging Component], IWICMetadataBlockReader interface [Windows Imaging Component],described, _wic_codec_iwicmetadatablockreader, wic._wic_codec_iwicmetadatablockreader, wincodecsdk/IWICMetadataBlockReader
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
 - IWICMetadataBlockReader
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWICMetadataBlockReader interface


## -description


Exposes methods that provide access to all of the codec's top level metadata blocks.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWICMetadataBlockReader</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWICMetadataBlockReader</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/b53e6b4e-e5b9-4e4a-b10b-443e3ca2d689">GetContainerFormat</a>
</td>
<td align="left" width="63%">
Retrieves the container format of the decoder.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/212e2376-9fad-4bfc-8883-ce89d05c35e6">GetCount</a>
</td>
<td align="left" width="63%">
Retrieves the number of top level metadata blocks.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/81441e25-f124-4978-830d-2ade9cde6917">GetEnumerator</a>
</td>
<td align="left" width="63%">
Retrieves an enumeration of each of the top level metadata blocks.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fb0d0951-7bb1-4bf7-9bfb-50f522929baf">GetReaderByIndex</a>
</td>
<td align="left" width="63%">
Retrieves an <a href="https://msdn.microsoft.com/0495ecf1-128a-4576-8420-0e79f1454015">IWICMetadataReader</a> for a specified top level metadata block, providing access to the embedded metadata blocks.

</td>
</tr>
</table> 


## -remarks



<b>IWICMetadataBlockReader</b> and <a href="https://msdn.microsoft.com/d8e44c64-dd58-4d36-8add-0a0b2e2af5a4">IWICMetadataBlockWriter</a> operate at the root level only; that is, they provide read and write access, respectively, to the top level metadata blocks. They are implemented by <a href="https://msdn.microsoft.com/1498b800-6449-440f-bed7-85891637e559">IWICBitmapFrameDecode</a> and <a href="https://msdn.microsoft.com/a8de774b-3783-46be-9a21-c9fec2f10ffd">IWICBitmapFrameEncode</a>, respectively. To handle any metadata blocks that are not at the top level of the hierarchy, use <a href="https://msdn.microsoft.com/0495ecf1-128a-4576-8420-0e79f1454015">IWICMetadataReader</a> or <a href="https://msdn.microsoft.com/7e742a96-f9d0-49e1-80e4-31ec90680e60">IWICMetadataWriter</a>.


<div class="alert"><b>Note</b>  The codec's decoder and encoder implement this interface to expose the enumeration of all top level metadata blocks.  While the codec parses the image stream, it calls services like <a href="https://msdn.microsoft.com/876d2d5a-8247-4e4a-b402-0ee02d9b0158">CreateMetadataReaderFromContainer</a> to instantiate metadata readers for any block that is recognized as being able to be embedded in the decoder's container format.  The collection of metadata readers is exposed through this interface. For more info, see <a href="https://msdn.microsoft.com/en-us/library/Ee719883(v=VS.85).aspx">How to Write a WIC-Enabled CODEC</a>.</div>
<div> </div>



## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/08f1872b-6e4d-44ee-abc7-48685e435acc">Metadata Extensibility Overview</a>



<a href="https://msdn.microsoft.com/b1e0b936-a13a-42dd-8470-957ba1d90423">Overview of Reading and Writing Image Metadata</a>



<a href="https://msdn.microsoft.com/35727810-3c4c-4c11-a4a2-3ae2cf3b8142">WIC Metadata Overview</a>
 

 

