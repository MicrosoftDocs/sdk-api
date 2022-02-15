---
UID: NF:wincodecsdk.IWICMetadataBlockWriter.SetWriterByIndex
title: IWICMetadataBlockWriter::SetWriterByIndex (wincodecsdk.h)
description: Replaces the metadata writer at the specified index location.
helpviewer_keywords: ["IWICMetadataBlockWriter interface [Windows Imaging Component]","SetWriterByIndex method","IWICMetadataBlockWriter.SetWriterByIndex","IWICMetadataBlockWriter::SetWriterByIndex","SetWriterByIndex","SetWriterByIndex method [Windows Imaging Component]","SetWriterByIndex method [Windows Imaging Component]","IWICMetadataBlockWriter interface","_wic_codec_iwicmetadatablockwriter_setwriterbyindex","wic._wic_codec_iwicmetadatablockwriter_setwriterbyindex","wincodecsdk/IWICMetadataBlockWriter::SetWriterByIndex"]
old-location: wic\_wic_codec_iwicmetadatablockwriter_setwriterbyindex.htm
tech.root: wic
ms.assetid: cf8f45ee-44ca-431c-b9c2-1b00c5574afe
ms.date: 12/05/2018
ms.keywords: IWICMetadataBlockWriter interface [Windows Imaging Component],SetWriterByIndex method, IWICMetadataBlockWriter.SetWriterByIndex, IWICMetadataBlockWriter::SetWriterByIndex, SetWriterByIndex, SetWriterByIndex method [Windows Imaging Component], SetWriterByIndex method [Windows Imaging Component],IWICMetadataBlockWriter interface, _wic_codec_iwicmetadatablockwriter_setwriterbyindex, wic._wic_codec_iwicmetadatablockwriter_setwriterbyindex, wincodecsdk/IWICMetadataBlockWriter::SetWriterByIndex
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
 - IWICMetadataBlockWriter::SetWriterByIndex
 - wincodecsdk/IWICMetadataBlockWriter::SetWriterByIndex
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
 - IWICMetadataBlockWriter.SetWriterByIndex
---

# IWICMetadataBlockWriter::SetWriterByIndex


## -description

Replaces the metadata writer at the specified index location.

## -parameters

### -param nIndex [in]

Type: <b>UINT</b>

The index position at which to place the metadata writer. This index is zero-based.

### -param pIMetadataWriter [in]

Type: <b><a href="/windows/desktop/api/wincodecsdk/nn-wincodecsdk-iwicmetadatawriter">IWICMetadataWriter</a>*</b>

A pointer to the <a href="/windows/desktop/api/wincodecsdk/nn-wincodecsdk-iwicmetadatawriter">IWICMetadataWriter</a>.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Typically, the current metadata writer at the specified index will be replaced with the new writer. However, the App0 metadata writer cannot be replaced within a JPEG stream. 

This function cannot be used to add metadata writers. If no metadata writer exists at the specified index, the function will fail.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/wic/-wic-howtowriteacodec">How to Write a WIC-Enabled CODEC</a>



<a href="/windows/desktop/wic/-wic-codec-jpegmetadataencoding">How-to: Re-encode a JPEG Image with Metadata</a>



<a href="/windows/desktop/api/wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter">IWICMetadataBlockWriter</a>



<b>Other Resources</b>



<a href="/windows/desktop/wic/-wic-codec-readingwritingmetadata">Overview of Reading and Writing Image Metadata</a>



<a href="/windows/desktop/wic/-wic-about-metadata">WIC Metadata Overview</a>