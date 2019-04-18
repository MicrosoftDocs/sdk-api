---
UID: NN:wincodecsdk.IWICMetadataReader
title: IWICMetadataReader (wincodecsdk.h)
author: windows-sdk-content
description: Exposes methods that provide access to underlining metadata content. This interface is implemented by independent software vendors (ISVs) to create new metadata readers.
old-location: wic\_wic_codec_iwicmetadatareader.htm
tech.root: wic
ms.assetid: 0495ecf1-128a-4576-8420-0e79f1454015
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IWICMetadataReader, IWICMetadataReader interface [Windows Imaging Component], IWICMetadataReader interface [Windows Imaging Component],described, _wic_codec_iwicmetadatareader, wic._wic_codec_iwicmetadatareader, wincodecsdk/IWICMetadataReader
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
 - IWICMetadataReader
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWICMetadataReader interface


## -description


Exposes methods that provide access to underlining metadata content. This interface is implemented by independent software vendors (ISVs) to create new metadata readers.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWICMetadataReader</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWICMetadataReader</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWICMetadataReader</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ce9b0267-112a-4aa9-8786-272ee4da4d8b">GetCount</a>
</td>
<td align="left" width="63%">
Gets the number of metadata items within the reader.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8dfb2b8d-2825-470e-8adc-85437d8fe863">GetEnumerator</a>
</td>
<td align="left" width="63%">
Gets an enumerator of all the metadata items.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5dcbfac4-9a77-4453-be1e-3c42e94d548e">GetMetadataFormat</a>
</td>
<td align="left" width="63%">
Gets the metadata format associated with the reader.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f3843044-4963-4e9f-8b5d-69d0201c9ec9">GetMetadataHandlerInfo</a>
</td>
<td align="left" width="63%">
Gets the metadata handler info associated with the reader.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7ae1328d-cda7-4522-9bcf-2c4b16fd6984">GetValue</a>
</td>
<td align="left" width="63%">
Gets the metadata item value.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/dd22e0e6-d607-48ae-a51c-b49003004f1f">GetValueByIndex</a>
</td>
<td align="left" width="63%">
Gets the metadata item at the given index.

</td>
</tr>
</table> 


## -remarks



A metadata reader can be used to access metadata blocks and items within a metadata block instead of using a query reader. To directly access the metadata reader, query a decoder or its frames for the <a href="https://msdn.microsoft.com/09614b44-ebc2-44f4-9755-9df62f1b2178">IWICMetadataBlockReader</a> interface to enumerate each metadata reader.




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/08f1872b-6e4d-44ee-abc7-48685e435acc">Metadata Extensibility Overview</a>



<a href="https://msdn.microsoft.com/5ffa0a69-b53d-4be3-b802-deaaa743e6bd">Metadata Query Language Overview</a>



<a href="https://msdn.microsoft.com/b1e0b936-a13a-42dd-8470-957ba1d90423">Overview of Reading and Writing Image Metadata</a>



<a href="https://msdn.microsoft.com/35727810-3c4c-4c11-a4a2-3ae2cf3b8142">WIC Metadata Overview</a>
 

 

