---
UID: NF:wincodecsdk.IWICMetadataBlockReader.GetReaderByIndex
title: IWICMetadataBlockReader::GetReaderByIndex (wincodecsdk.h)
description: Retrieves an IWICMetadataReader for a specified top level metadata block.
helpviewer_keywords: ["GetReaderByIndex","GetReaderByIndex method [Windows Imaging Component]","GetReaderByIndex method [Windows Imaging Component]","IWICMetadataBlockReader interface","IWICMetadataBlockReader interface [Windows Imaging Component]","GetReaderByIndex method","IWICMetadataBlockReader.GetReaderByIndex","IWICMetadataBlockReader::GetReaderByIndex","_wic_codec_iwicmetadatablockreader_getreaderbyindex","wic._wic_codec_iwicmetadatablockreader_getreaderbyindex","wincodecsdk/IWICMetadataBlockReader::GetReaderByIndex"]
old-location: wic\_wic_codec_iwicmetadatablockreader_getreaderbyindex.htm
tech.root: wic
ms.assetid: fb0d0951-7bb1-4bf7-9bfb-50f522929baf
ms.date: 12/05/2018
ms.keywords: GetReaderByIndex, GetReaderByIndex method [Windows Imaging Component], GetReaderByIndex method [Windows Imaging Component],IWICMetadataBlockReader interface, IWICMetadataBlockReader interface [Windows Imaging Component],GetReaderByIndex method, IWICMetadataBlockReader.GetReaderByIndex, IWICMetadataBlockReader::GetReaderByIndex, _wic_codec_iwicmetadatablockreader_getreaderbyindex, wic._wic_codec_iwicmetadatablockreader_getreaderbyindex, wincodecsdk/IWICMetadataBlockReader::GetReaderByIndex
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
 - IWICMetadataBlockReader::GetReaderByIndex
 - wincodecsdk/IWICMetadataBlockReader::GetReaderByIndex
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
 - IWICMetadataBlockReader.GetReaderByIndex
---

# IWICMetadataBlockReader::GetReaderByIndex


## -description

Retrieves an <a href="/windows/desktop/api/wincodecsdk/nn-wincodecsdk-iwicmetadatareader">IWICMetadataReader</a> for a specified top level metadata block.

## -parameters

### -param nIndex [in]

Type: <b>UINT</b>

The index of the desired top level metadata block to retrieve.

### -param ppIMetadataReader [out]

Type: <b><a href="/windows/desktop/api/wincodecsdk/nn-wincodecsdk-iwicmetadatareader">IWICMetadataReader</a>**</b>

When this method returns, contains a pointer to the <a href="/windows/desktop/api/wincodecsdk/nn-wincodecsdk-iwicmetadatareader">IWICMetadataReader</a> specified by <i>nIndex</i>.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/wic/-wic-howtowriteacodec">How to Write a WIC-Enabled CODEC</a>



<a href="/windows/desktop/api/wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader">IWICMetadataBlockReader</a>



<b>Other Resources</b>



<a href="/windows/desktop/wic/-wic-codec-readingwritingmetadata">Overview of Reading and Writing Image Metadata</a>



<a href="/windows/desktop/wic/-wic-about-metadata">WIC Metadata Overview</a>



<a href="/windows/desktop/wic/-wic-about-windows-imaging-codec">Windows Imaging Component Overview</a>