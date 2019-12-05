---
UID: NN:wincodecsdk.IWICMetadataWriter
title: IWICMetadataWriter (wincodecsdk.h)
description: Exposes methods that provide access to writing metadata content. This is implemented by independent software vendors (ISVs) to create new metadata writers.
old-location: wic\_wic_codec_iwicmetadatawriter.htm
tech.root: wic
ms.assetid: 7e742a96-f9d0-49e1-80e4-31ec90680e60
ms.date: 12/05/2018
ms.keywords: IWICMetadataWriter, IWICMetadataWriter interface [Windows Imaging Component], IWICMetadataWriter interface [Windows Imaging Component],described, _wic_codec_iwicmetadatawriter, wic._wic_codec_iwicmetadatawriter, wincodecsdk/IWICMetadataWriter
ms.topic: interface
f1_keywords:
- wincodecsdk/IWICMetadataWriter
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
- IWICMetadataWriter
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWICMetadataWriter interface


## -description


Exposes methods that provide access to writing metadata content. This is implemented by independent software vendors (ISVs) to create new metadata writers.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWICMetadataWriter</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/wincodecsdk/nn-wincodecsdk-iwicmetadatareader">IWICMetadataReader</a>. <b>IWICMetadataWriter</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/wincodecsdk/nf-wincodecsdk-iwicmetadatawriter-removevalue">RemoveValue</a>
</td>
<td align="left" width="63%">
Removes the metadata item that matches the given parameters.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wincodecsdk/nf-wincodecsdk-iwicmetadatawriter-removevaluebyindex">RemoveValueByIndex</a>
</td>
<td align="left" width="63%">
Removes the metadata item at the specified index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wincodecsdk/nf-wincodecsdk-iwicmetadatawriter-setvalue">SetValue</a>
</td>
<td align="left" width="63%">
Sets the given metadata item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wincodecsdk/nf-wincodecsdk-iwicmetadatawriter-setvaluebyindex">SetValueByIndex</a>
</td>
<td align="left" width="63%">
Sets the metadata item to the specified index.

</td>
</tr>
</table> 


## -remarks



A metadata writer can be used to write metadata blocks and items within a metadata block instead of using a query writer. To directly access the metadata writer, query an encoder or its frames for the <a href="https://docs.microsoft.com/windows/desktop/api/wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter">IWICMetadataBlockWriter</a> interface to enumerate each metadata writer.




## -see-also




<b>Conceptual</b>



<a href="https://docs.microsoft.com/windows/desktop/api/wincodecsdk/nn-wincodecsdk-iwicmetadatareader">IWICMetadataReader</a>



<a href="https://docs.microsoft.com/windows/desktop/wic/-wic-codec-metadatahandlers">Metadata Extensibility Overview</a>



<a href="https://docs.microsoft.com/windows/desktop/wic/-wic-codec-metadataquerylanguage">Metadata Query Language Overview</a>



<a href="https://docs.microsoft.com/windows/desktop/wic/-wic-codec-readingwritingmetadata">Overview of Reading and Writing Image Metadata</a>



<a href="https://docs.microsoft.com/windows/desktop/wic/-wic-about-metadata">WIC Metadata Overview</a>
 

 

