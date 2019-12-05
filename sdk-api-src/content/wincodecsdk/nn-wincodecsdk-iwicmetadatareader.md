---
UID: NN:wincodecsdk.IWICMetadataReader
title: IWICMetadataReader (wincodecsdk.h)
description: Exposes methods that provide access to underlining metadata content. This interface is implemented by independent software vendors (ISVs) to create new metadata readers.
old-location: wic\_wic_codec_iwicmetadatareader.htm
tech.root: wic
ms.assetid: 0495ecf1-128a-4576-8420-0e79f1454015
ms.date: 12/05/2018
ms.keywords: IWICMetadataReader, IWICMetadataReader interface [Windows Imaging Component], IWICMetadataReader interface [Windows Imaging Component],described, _wic_codec_iwicmetadatareader, wic._wic_codec_iwicmetadatareader, wincodecsdk/IWICMetadataReader
ms.topic: interface
f1_keywords:
- wincodecsdk/IWICMetadataReader
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
- IWICMetadataReader
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWICMetadataReader interface


## -description


Exposes methods that provide access to underlining metadata content. This interface is implemented by independent software vendors (ISVs) to create new metadata readers.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWICMetadataReader</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWICMetadataReader</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/wincodecsdk/nf-wincodecsdk-iwicmetadatareader-getcount">GetCount</a>
</td>
<td align="left" width="63%">
Gets the number of metadata items within the reader.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wincodecsdk/nf-wincodecsdk-iwicmetadatareader-getenumerator">GetEnumerator</a>
</td>
<td align="left" width="63%">
Gets an enumerator of all the metadata items.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wincodecsdk/nf-wincodecsdk-iwicmetadatareader-getmetadataformat">GetMetadataFormat</a>
</td>
<td align="left" width="63%">
Gets the metadata format associated with the reader.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wincodecsdk/nf-wincodecsdk-iwicmetadatareader-getmetadatahandlerinfo">GetMetadataHandlerInfo</a>
</td>
<td align="left" width="63%">
Gets the metadata handler info associated with the reader.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wincodecsdk/nf-wincodecsdk-iwicmetadatareader-getvalue">GetValue</a>
</td>
<td align="left" width="63%">
Gets the metadata item value.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wincodecsdk/nf-wincodecsdk-iwicmetadatareader-getvaluebyindex">GetValueByIndex</a>
</td>
<td align="left" width="63%">
Gets the metadata item at the given index.

</td>
</tr>
</table> 


## -remarks



A metadata reader can be used to access metadata blocks and items within a metadata block instead of using a query reader. To directly access the metadata reader, query a decoder or its frames for the <a href="https://docs.microsoft.com/windows/desktop/api/wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader">IWICMetadataBlockReader</a> interface to enumerate each metadata reader.




## -see-also




<b>Conceptual</b>



<a href="https://docs.microsoft.com/windows/desktop/wic/-wic-codec-metadatahandlers">Metadata Extensibility Overview</a>



<a href="https://docs.microsoft.com/windows/desktop/wic/-wic-codec-metadataquerylanguage">Metadata Query Language Overview</a>



<a href="https://docs.microsoft.com/windows/desktop/wic/-wic-codec-readingwritingmetadata">Overview of Reading and Writing Image Metadata</a>



<a href="https://docs.microsoft.com/windows/desktop/wic/-wic-about-metadata">WIC Metadata Overview</a>
 

 

