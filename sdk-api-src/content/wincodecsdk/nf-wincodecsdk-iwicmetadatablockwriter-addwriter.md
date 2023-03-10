---
UID: NF:wincodecsdk.IWICMetadataBlockWriter.AddWriter
title: IWICMetadataBlockWriter::AddWriter (wincodecsdk.h)
description: Adds a top-level metadata block by adding a IWICMetadataWriter for it.
helpviewer_keywords: ["AddWriter","AddWriter method [Windows Imaging Component]","AddWriter method [Windows Imaging Component]","IWICMetadataBlockWriter interface","IWICMetadataBlockWriter interface [Windows Imaging Component]","AddWriter method","IWICMetadataBlockWriter.AddWriter","IWICMetadataBlockWriter::AddWriter","_wic_codec_iwicmetadatablockwriter_addwriter","wic._wic_codec_iwicmetadatablockwriter_addwriter","wincodecsdk/IWICMetadataBlockWriter::AddWriter"]
old-location: wic\_wic_codec_iwicmetadatablockwriter_addwriter.htm
tech.root: wic
ms.assetid: 25a0e662-a249-4218-a77e-37b11e0f8536
ms.date: 12/05/2018
ms.keywords: AddWriter, AddWriter method [Windows Imaging Component], AddWriter method [Windows Imaging Component],IWICMetadataBlockWriter interface, IWICMetadataBlockWriter interface [Windows Imaging Component],AddWriter method, IWICMetadataBlockWriter.AddWriter, IWICMetadataBlockWriter::AddWriter, _wic_codec_iwicmetadatablockwriter_addwriter, wic._wic_codec_iwicmetadatablockwriter_addwriter, wincodecsdk/IWICMetadataBlockWriter::AddWriter
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
 - IWICMetadataBlockWriter::AddWriter
 - wincodecsdk/IWICMetadataBlockWriter::AddWriter
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
 - IWICMetadataBlockWriter.AddWriter
---

# IWICMetadataBlockWriter::AddWriter


## -description

Adds a top-level metadata block by adding a <a href="/windows/desktop/api/wincodecsdk/nn-wincodecsdk-iwicmetadatawriter">IWICMetadataWriter</a> for it.

## -parameters

### -param pIMetadataWriter [in]

Type: <b><a href="/windows/desktop/api/wincodecsdk/nn-wincodecsdk-iwicmetadatawriter">IWICMetadataWriter</a>*</b>

A pointer to the metadata writer to add to the image.

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