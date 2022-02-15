---
UID: NF:wincodecsdk.IWICMetadataBlockWriter.InitializeFromBlockReader
title: IWICMetadataBlockWriter::InitializeFromBlockReader (wincodecsdk.h)
description: Initializes an IWICMetadataBlockWriter from the given IWICMetadataBlockReader. This will prepopulate the metadata block writer with all the metadata in the metadata block reader.
helpviewer_keywords: ["IWICMetadataBlockWriter interface [Windows Imaging Component]","InitializeFromBlockReader method","IWICMetadataBlockWriter.InitializeFromBlockReader","IWICMetadataBlockWriter::InitializeFromBlockReader","InitializeFromBlockReader","InitializeFromBlockReader method [Windows Imaging Component]","InitializeFromBlockReader method [Windows Imaging Component]","IWICMetadataBlockWriter interface","_wic_codec_iwicmetadatablockwriter_initializefromblockreader","wic._wic_codec_iwicmetadatablockwriter_initializefromblockreader","wincodecsdk/IWICMetadataBlockWriter::InitializeFromBlockReader"]
old-location: wic\_wic_codec_iwicmetadatablockwriter_initializefromblockreader.htm
tech.root: wic
ms.assetid: 9ad9d818-7b3e-47eb-bc99-e26e7664383c
ms.date: 12/05/2018
ms.keywords: IWICMetadataBlockWriter interface [Windows Imaging Component],InitializeFromBlockReader method, IWICMetadataBlockWriter.InitializeFromBlockReader, IWICMetadataBlockWriter::InitializeFromBlockReader, InitializeFromBlockReader, InitializeFromBlockReader method [Windows Imaging Component], InitializeFromBlockReader method [Windows Imaging Component],IWICMetadataBlockWriter interface, _wic_codec_iwicmetadatablockwriter_initializefromblockreader, wic._wic_codec_iwicmetadatablockwriter_initializefromblockreader, wincodecsdk/IWICMetadataBlockWriter::InitializeFromBlockReader
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
 - IWICMetadataBlockWriter::InitializeFromBlockReader
 - wincodecsdk/IWICMetadataBlockWriter::InitializeFromBlockReader
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
 - IWICMetadataBlockWriter.InitializeFromBlockReader
---

# IWICMetadataBlockWriter::InitializeFromBlockReader


## -description

Initializes an <a href="/windows/desktop/api/wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter">IWICMetadataBlockWriter</a> from the given <a href="/windows/desktop/api/wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader">IWICMetadataBlockReader</a>. This will prepopulate the metadata block writer with all the metadata in the metadata block reader.

## -parameters

### -param pIMDBlockReader [in]

Type: <b><a href="/windows/desktop/api/wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader">IWICMetadataBlockReader</a>*</b>

Pointer to the <a href="/windows/desktop/api/wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader">IWICMetadataBlockReader</a> used to initialize the block writer.

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