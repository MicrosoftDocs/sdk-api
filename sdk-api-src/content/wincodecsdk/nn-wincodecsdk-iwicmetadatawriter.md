---
UID: NN:wincodecsdk.IWICMetadataWriter
title: IWICMetadataWriter
author: windows-sdk-content
description: Exposes methods that provide access to writing metadata content. This is implemented by independent software vendors (ISVs) to create new metadata writers.
old-location: wic\_wic_codec_iwicmetadatawriter.htm
tech.root: wic
ms.assetid: 7e742a96-f9d0-49e1-80e4-31ec90680e60
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IWICMetadataWriter, IWICMetadataWriter interface [Windows Imaging Component], IWICMetadataWriter interface [Windows Imaging Component],described, _wic_codec_iwicmetadatawriter, wic._wic_codec_iwicmetadatawriter, wincodecsdk/IWICMetadataWriter
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IWICMetadataWriter
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWICMetadataWriter interface


## -description


Exposes methods that provide access to writing metadata content. This is implemented by independent software vendors (ISVs) to create new metadata writers.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWICMetadataWriter</b> interface inherits from <a href="https://msdn.microsoft.com/0495ecf1-128a-4576-8420-0e79f1454015">IWICMetadataReader</a>. <b>IWICMetadataWriter</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWICMetadataWriter</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cc47b0d1-5772-4609-9696-816d39d04b34">RemoveValue</a>
</td>
<td align="left" width="63%">
Removes the metadata item that matches the given parameters.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/65cf7e21-e474-4652-9ee1-0802362f65ca">RemoveValueByIndex</a>
</td>
<td align="left" width="63%">
Removes the metadata item at the specified index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bda3f959-40d1-45df-a82c-3eba2be33859">SetValue</a>
</td>
<td align="left" width="63%">
Sets the given metadata item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/012ef661-c1cf-48fd-a748-223fa965f9a9">SetValueByIndex</a>
</td>
<td align="left" width="63%">
Sets the metadata item to the specified index.

</td>
</tr>
</table> 


## -remarks



A metadata writer can be used to write metadata blocks and items within a metadata block instead of using a query writer. To directly access the metadata writer, query an encoder or its frames for the <a href="https://msdn.microsoft.com/d8e44c64-dd58-4d36-8add-0a0b2e2af5a4">IWICMetadataBlockWriter</a> interface to enumerate each metadata writer.




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/0495ecf1-128a-4576-8420-0e79f1454015">IWICMetadataReader</a>



<a href="https://msdn.microsoft.com/08f1872b-6e4d-44ee-abc7-48685e435acc">Metadata Extensibility Overview</a>



<a href="https://msdn.microsoft.com/5ffa0a69-b53d-4be3-b802-deaaa743e6bd">Metadata Query Language Overview</a>



<a href="https://msdn.microsoft.com/b1e0b936-a13a-42dd-8470-957ba1d90423">Overview of Reading and Writing Image Metadata</a>



<a href="https://msdn.microsoft.com/35727810-3c4c-4c11-a4a2-3ae2cf3b8142">WIC Metadata Overview</a>
 

 

