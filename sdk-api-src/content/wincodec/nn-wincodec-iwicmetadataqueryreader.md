---
UID: NN:wincodec.IWICMetadataQueryReader
title: IWICMetadataQueryReader (wincodec.h)
description: Exposes methods for retrieving metadata blocks and items from a decoder or its image frames using a metadata query expression.helpviewer_keywords: ["IWICMetadataQueryReader","IWICMetadataQueryReader interface [Windows Imaging Component]","IWICMetadataQueryReader interface [Windows Imaging Component]","described","_wic_codec_iwicmetadataqueryreader","wic._wic_codec_iwicmetadataqueryreader","wincodec/IWICMetadataQueryReader"]
old-location: wic\_wic_codec_iwicmetadataqueryreader.htm
tech.root: wic
ms.assetid: 588e00d2-e166-4ce5-bd8a-50ad0d5a3db9
ms.date: 12/05/2018
ms.keywords: IWICMetadataQueryReader, IWICMetadataQueryReader interface [Windows Imaging Component], IWICMetadataQueryReader interface [Windows Imaging Component],described, _wic_codec_iwicmetadataqueryreader, wic._wic_codec_iwicmetadataqueryreader, wincodec/IWICMetadataQueryReader
f1_keywords:
- wincodec/IWICMetadataQueryReader
dev_langs:
- c++
req.header: wincodec.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wincodec.idl
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
- IWICMetadataQueryReader
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWICMetadataQueryReader interface


## -description


Exposes methods for retrieving metadata blocks and items from a decoder or its image frames using a metadata query expression.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWICMetadataQueryReader</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWICMetadataQueryReader</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWICMetadataQueryReader</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nf-wincodec-iwicmetadataqueryreader-getcontainerformat">GetContainerFormat</a>
</td>
<td align="left" width="63%">
Gets the metadata query readers container format.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nf-wincodec-iwicmetadataqueryreader-getenumerator">GetEnumerator</a>
</td>
<td align="left" width="63%">
Gets an enumerator of all metadata items at the current relative location within the metadata hierarchy.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nf-wincodec-iwicmetadataqueryreader-getlocation">GetLocation</a>
</td>
<td align="left" width="63%">
Retrieves the current path relative to the root metadata block.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nf-wincodec-iwicmetadataqueryreader-getmetadatabyname">GetMetadataByName</a>
</td>
<td align="left" width="63%">
Retrieves the metadata block or item identified by a metadata query expression. 

</td>
</tr>
</table> 


## -remarks



A metadata query reader uses metadata query expressions to access embedded metadata. For more information on the metadata query language, see the <a href="https://docs.microsoft.com/windows/desktop/wic/-wic-codec-metadataquerylanguage">Metadata Query Language Overview</a>.

The benefit of the query reader is the ability to access a metadata item in a single step.


The query reader also provides the way to traverse the whole set of metadata hierarchy with the help of the <a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nf-wincodec-iwicmetadataqueryreader-getenumerator">GetEnumerator</a> method.
However, it is not recommended to use this method since <a href="https://docs.microsoft.com/windows/desktop/api/wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader">IWICMetadataBlockReader</a> and <a href="https://docs.microsoft.com/windows/desktop/api/wincodecsdk/nn-wincodecsdk-iwicmetadatareader">IWICMetadataReader</a> provide a more convenient and cheaper way.



#### Examples

The following code demonstrates how to obtain a query reader and use it to retrieve a metadata item.


```
// Get the query reader
if (SUCCEEDED(hr))
{
    hr = pFrameDecode->GetMetadataQueryReader(&pQueryReader);
}

if (SUCCEEDED(hr))
{
    hr = pQueryReader->GetMetadataByName(L"/app1/ifd/{ushort=18249}", &value);
    PropVariantClear(&value);
}
```


The following code demonstrates how to obtain query reader and use it to retrieve a nested metadata block.


```
// Get the query reader
if (SUCCEEDED(hr))
{
    hr = pFrameDecode->GetMetadataQueryReader(&pQueryReader);
}

if (SUCCEEDED(hr))
{
    // Get the embedded IFD reader
    hr = pQueryReader->GetMetadataByName(L"/app1/ifd", &value);
    if (value.vt == VT_UNKNOWN)
    {
        hr = value.punkVal->QueryInterface(IID_IWICMetadataQueryReader, (void **)&pEmbedReader);
    }
    PropVariantClear(&value); // Clear value for new query
}
```





## -see-also




<b>Conceptual</b>



<a href="https://docs.microsoft.com/windows/desktop/wic/-wic-codec-metadataquerylanguage">Metadata Query Language Overview</a>



<a href="https://docs.microsoft.com/windows/desktop/wic/-wic-codec-readingwritingmetadata">Overview of Reading and Writing Image Metadata</a>



<a href="https://docs.microsoft.com/windows/desktop/wic/-wic-about-metadata">WIC Metadata Overview</a>
 

 

