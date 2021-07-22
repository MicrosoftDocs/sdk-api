---
UID: NN:wincodec.IWICMetadataQueryReader
title: IWICMetadataQueryReader (wincodec.h)
description: Exposes methods for retrieving metadata blocks and items from a decoder or its image frames using a metadata query expression.
helpviewer_keywords: ["IWICMetadataQueryReader","IWICMetadataQueryReader interface [Windows Imaging Component]","IWICMetadataQueryReader interface [Windows Imaging Component]","described","_wic_codec_iwicmetadataqueryreader","wic._wic_codec_iwicmetadataqueryreader","wincodec/IWICMetadataQueryReader"]
old-location: wic\_wic_codec_iwicmetadataqueryreader.htm
tech.root: wic
ms.assetid: 588e00d2-e166-4ce5-bd8a-50ad0d5a3db9
ms.date: 12/05/2018
ms.keywords: IWICMetadataQueryReader, IWICMetadataQueryReader interface [Windows Imaging Component], IWICMetadataQueryReader interface [Windows Imaging Component],described, _wic_codec_iwicmetadataqueryreader, wic._wic_codec_iwicmetadataqueryreader, wincodec/IWICMetadataQueryReader
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWICMetadataQueryReader
 - wincodec/IWICMetadataQueryReader
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
 - IWICMetadataQueryReader
---

# IWICMetadataQueryReader interface


## -description

Exposes methods for retrieving metadata blocks and items from a decoder or its image frames using a metadata query expression.

## -inheritance

The <b>IWICMetadataQueryReader</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWICMetadataQueryReader</b> also has these types of members:

## -remarks

A metadata query reader uses metadata query expressions to access embedded metadata. For more information on the metadata query language, see the <a href="/windows/desktop/wic/-wic-codec-metadataquerylanguage">Metadata Query Language Overview</a>.

The benefit of the query reader is the ability to access a metadata item in a single step.


The query reader also provides the way to traverse the whole set of metadata hierarchy with the help of the <a href="/windows/desktop/api/wincodec/nf-wincodec-iwicmetadataqueryreader-getenumerator">GetEnumerator</a> method.
However, it is not recommended to use this method since <a href="/windows/desktop/api/wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader">IWICMetadataBlockReader</a> and <a href="/windows/desktop/api/wincodecsdk/nn-wincodecsdk-iwicmetadatareader">IWICMetadataReader</a> provide a more convenient and cheaper way.



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



<a href="/windows/desktop/wic/-wic-codec-metadataquerylanguage">Metadata Query Language Overview</a>



<a href="/windows/desktop/wic/-wic-codec-readingwritingmetadata">Overview of Reading and Writing Image Metadata</a>



<a href="/windows/desktop/wic/-wic-about-metadata">WIC Metadata Overview</a>
