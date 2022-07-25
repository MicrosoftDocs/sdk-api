---
UID: NF:wincodecsdk.IWICMetadataBlockWriter.GetWriterByIndex
title: IWICMetadataBlockWriter::GetWriterByIndex (wincodecsdk.h)
description: Retrieves the IWICMetadataWriter that resides at the specified index.
helpviewer_keywords: ["GetWriterByIndex","GetWriterByIndex method [Windows Imaging Component]","GetWriterByIndex method [Windows Imaging Component]","IWICMetadataBlockWriter interface","IWICMetadataBlockWriter interface [Windows Imaging Component]","GetWriterByIndex method","IWICMetadataBlockWriter.GetWriterByIndex","IWICMetadataBlockWriter::GetWriterByIndex","_wic_codec_iwicmetadatablockwriter_getwriterbyindex","wic._wic_codec_iwicmetadatablockwriter_getwriterbyindex","wincodecsdk/IWICMetadataBlockWriter::GetWriterByIndex"]
old-location: wic\_wic_codec_iwicmetadatablockwriter_getwriterbyindex.htm
tech.root: wic
ms.assetid: 14c8acb1-484a-46ad-8a38-79a4b1cfe0d1
ms.date: 12/05/2018
ms.keywords: GetWriterByIndex, GetWriterByIndex method [Windows Imaging Component], GetWriterByIndex method [Windows Imaging Component],IWICMetadataBlockWriter interface, IWICMetadataBlockWriter interface [Windows Imaging Component],GetWriterByIndex method, IWICMetadataBlockWriter.GetWriterByIndex, IWICMetadataBlockWriter::GetWriterByIndex, _wic_codec_iwicmetadatablockwriter_getwriterbyindex, wic._wic_codec_iwicmetadatablockwriter_getwriterbyindex, wincodecsdk/IWICMetadataBlockWriter::GetWriterByIndex
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWICMetadataBlockWriter::GetWriterByIndex
 - wincodecsdk/IWICMetadataBlockWriter::GetWriterByIndex
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
 - IWICMetadataBlockWriter.GetWriterByIndex
---

# IWICMetadataBlockWriter::GetWriterByIndex


## -description

Retrieves the <a href="/windows/desktop/api/wincodecsdk/nn-wincodecsdk-iwicmetadatawriter">IWICMetadataWriter</a> that resides at the specified index.

## -parameters

### -param nIndex [in]

Type: <b>UINT</b>

The index of the metadata writer to be retrieved. This index is zero-based.

### -param ppIMetadataWriter [out]

Type: <b><a href="/windows/desktop/api/wincodecsdk/nn-wincodecsdk-iwicmetadatawriter">IWICMetadataWriter</a>**</b>

When this method returns, contains a pointer to the metadata writer that resides at the specified index.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/wic/-wic-howtowriteacodec">How to Write a WIC-Enabled CODEC</a>



<a href="/windows/desktop/wic/-wic-codec-jpegmetadataencoding">How-to: Re-encode a JPEG Image with Metadata</a>



<a href="/windows/desktop/api/wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter">IWICMetadataBlockWriter</a>



<b>Other Resources</b>



<a href="/windows/desktop/wic/-wic-codec-readingwritingmetadata">Overview of Reading and Writing Image Metadata</a>



<a href="/windows/desktop/wic/-wic-about-metadata">WIC Metadata Overview</a>