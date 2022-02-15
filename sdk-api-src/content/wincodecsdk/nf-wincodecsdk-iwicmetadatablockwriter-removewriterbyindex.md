---
UID: NF:wincodecsdk.IWICMetadataBlockWriter.RemoveWriterByIndex
title: IWICMetadataBlockWriter::RemoveWriterByIndex (wincodecsdk.h)
description: Removes the metadata writer from the specified index location.
helpviewer_keywords: ["IWICMetadataBlockWriter interface [Windows Imaging Component]","RemoveWriterByIndex method","IWICMetadataBlockWriter.RemoveWriterByIndex","IWICMetadataBlockWriter::RemoveWriterByIndex","RemoveWriterByIndex","RemoveWriterByIndex method [Windows Imaging Component]","RemoveWriterByIndex method [Windows Imaging Component]","IWICMetadataBlockWriter interface","_wic_codec_iwicmetadatablockwriter_removewriterbyindex","wic._wic_codec_iwicmetadatablockwriter_removewriterbyindex","wincodecsdk/IWICMetadataBlockWriter::RemoveWriterByIndex"]
old-location: wic\_wic_codec_iwicmetadatablockwriter_removewriterbyindex.htm
tech.root: wic
ms.assetid: 030c5b0e-5db7-40ae-889c-2e1335d2c50b
ms.date: 12/05/2018
ms.keywords: IWICMetadataBlockWriter interface [Windows Imaging Component],RemoveWriterByIndex method, IWICMetadataBlockWriter.RemoveWriterByIndex, IWICMetadataBlockWriter::RemoveWriterByIndex, RemoveWriterByIndex, RemoveWriterByIndex method [Windows Imaging Component], RemoveWriterByIndex method [Windows Imaging Component],IWICMetadataBlockWriter interface, _wic_codec_iwicmetadatablockwriter_removewriterbyindex, wic._wic_codec_iwicmetadatablockwriter_removewriterbyindex, wincodecsdk/IWICMetadataBlockWriter::RemoveWriterByIndex
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
 - IWICMetadataBlockWriter::RemoveWriterByIndex
 - wincodecsdk/IWICMetadataBlockWriter::RemoveWriterByIndex
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
 - IWICMetadataBlockWriter.RemoveWriterByIndex
---

# IWICMetadataBlockWriter::RemoveWriterByIndex


## -description

Removes the metadata writer from the specified index location.

## -parameters

### -param nIndex [in]

Type: <b>UINT</b>

The index of the metadata writer to remove.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

 After removing a metadata writer, remaining metadata writers can be expected to move up to occupy the vacated location. Indexes for remaining metadata items as well as the count will change.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/wic/-wic-howtowriteacodec">How to Write a WIC-Enabled CODEC</a>



<a href="/windows/desktop/wic/-wic-codec-jpegmetadataencoding">How-to: Re-encode a JPEG Image with Metadata</a>



<a href="/windows/desktop/api/wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter">IWICMetadataBlockWriter</a>



<b>Other Resources</b>



<a href="/windows/desktop/wic/-wic-codec-readingwritingmetadata">Overview of Reading and Writing Image Metadata</a>



<a href="/windows/desktop/wic/-wic-about-metadata">WIC Metadata Overview</a>