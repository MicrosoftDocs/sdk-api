---
UID: NF:wincodecsdk.IWICMetadataBlockReader.GetContainerFormat
title: IWICMetadataBlockReader::GetContainerFormat (wincodecsdk.h)
description: Retrieves the container format of the decoder.
helpviewer_keywords: ["GetContainerFormat","GetContainerFormat method [Windows Imaging Component]","GetContainerFormat method [Windows Imaging Component]","IWICMetadataBlockReader interface","IWICMetadataBlockReader interface [Windows Imaging Component]","GetContainerFormat method","IWICMetadataBlockReader.GetContainerFormat","IWICMetadataBlockReader::GetContainerFormat","_wic_codec_iwicmetadatablockreader_getcontainerformat","wic._wic_codec_iwicmetadatablockreader_getcontainerformat","wincodecsdk/IWICMetadataBlockReader::GetContainerFormat"]
old-location: wic\_wic_codec_iwicmetadatablockreader_getcontainerformat.htm
tech.root: wic
ms.assetid: b53e6b4e-e5b9-4e4a-b10b-443e3ca2d689
ms.date: 12/05/2018
ms.keywords: GetContainerFormat, GetContainerFormat method [Windows Imaging Component], GetContainerFormat method [Windows Imaging Component],IWICMetadataBlockReader interface, IWICMetadataBlockReader interface [Windows Imaging Component],GetContainerFormat method, IWICMetadataBlockReader.GetContainerFormat, IWICMetadataBlockReader::GetContainerFormat, _wic_codec_iwicmetadatablockreader_getcontainerformat, wic._wic_codec_iwicmetadatablockreader_getcontainerformat, wincodecsdk/IWICMetadataBlockReader::GetContainerFormat
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
 - IWICMetadataBlockReader::GetContainerFormat
 - wincodecsdk/IWICMetadataBlockReader::GetContainerFormat
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
 - IWICMetadataBlockReader.GetContainerFormat
---

# IWICMetadataBlockReader::GetContainerFormat


## -description

Retrieves the container format of the decoder.

## -parameters

### -param pguidContainerFormat [out]

Type: <b>GUID*</b>

The container format of the decoder. The native container format GUIDs are listed in <a href="/windows/desktop/wic/-wic-guids-clsids">WIC GUIDs and CLSIDs</a>.

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