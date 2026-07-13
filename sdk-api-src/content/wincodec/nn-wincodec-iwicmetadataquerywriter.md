---
UID: NN:wincodec.IWICMetadataQueryWriter
title: IWICMetadataQueryWriter (wincodec.h)
description: Exposes methods for setting or removing metadata blocks and items to an encoder or its image frames using a metadata query expression.
helpviewer_keywords: ["IWICMetadataQueryWriter","IWICMetadataQueryWriter interface [Windows Imaging Component]","IWICMetadataQueryWriter interface [Windows Imaging Component]","described","_wic_codec_iwicmetadataquerywriter","wic._wic_codec_iwicmetadataquerywriter","wincodec/IWICMetadataQueryWriter"]
old-location: wic\_wic_codec_iwicmetadataquerywriter.htm
tech.root: wic
ms.assetid: 065cccc3-778f-42c4-823a-354b08bbd1f1
ms.date: 12/05/2018
ms.keywords: IWICMetadataQueryWriter, IWICMetadataQueryWriter interface [Windows Imaging Component], IWICMetadataQueryWriter interface [Windows Imaging Component],described, _wic_codec_iwicmetadataquerywriter, wic._wic_codec_iwicmetadataquerywriter, wincodec/IWICMetadataQueryWriter
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
 - IWICMetadataQueryWriter
 - wincodec/IWICMetadataQueryWriter
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
 - IWICMetadataQueryWriter
---

# IWICMetadataQueryWriter interface


## -description

Exposes methods for setting or removing metadata blocks and items to an encoder or its image frames using a metadata query expression.

## -inheritance

The <b>IWICMetadataQueryWriter</b> interface inherits from <a href="/windows/desktop/api/wincodec/nn-wincodec-iwicmetadataqueryreader">IWICMetadataQueryReader</a>. <b>IWICMetadataQueryWriter</b> also has these types of members:

## -remarks

A metadata query writer uses metadata query expressions to set or remove metadata. For more information on the metadata query language, see the <a href="/windows/desktop/wic/-wic-codec-metadataquerylanguage">Metadata Query Language Overview</a>.


#### Examples

The following code demonstrates how to create an XMP query writer and add a new metadata item to it.


```
// Create XMP block
IWICMetadataQueryWriter *pXMPWriter = NULL;

if (SUCCEEDED(hr))
{
    hr = pFactory->CreateQueryWriter(GUID_MetadataFormatXMP, NULL, &pXMPWriter);
}

// Write metadata to the XMP writer
if (SUCCEEDED(hr))
{
    PROPVARIANT value;
    PropVariantInit(&value);

    value.vt = VT_LPWSTR;
    value.pwszVal = L"Metadata Test Image.";
	
    hr = pXMPWriter->SetMetadataByName(L"/dc:title", &value);

    PropVariantClear(&value);
}
```

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/wic/-wic-codec-jpegmetadataencoding">How-to: Re-encode a JPEG Image with Metadata</a>



<a href="/windows/desktop/api/wincodec/nn-wincodec-iwicmetadataqueryreader">IWICMetadataQueryReader</a>



<a href="/windows/desktop/wic/-wic-codec-metadataquerylanguage">Metadata Query Language Overview</a>



<a href="/windows/desktop/wic/-wic-codec-readingwritingmetadata">Overview of Reading and Writing Image Metadata</a>



<a href="/windows/desktop/wic/-wic-about-metadata">WIC Metadata Overview</a>
