---
UID: NF:wincodec.IWICMetadataQueryReader.GetContainerFormat
title: IWICMetadataQueryReader::GetContainerFormat (wincodec.h)
description: Gets the metadata query readers container format.
helpviewer_keywords: ["GetContainerFormat","GetContainerFormat method [Windows Imaging Component]","GetContainerFormat method [Windows Imaging Component]","IWICMetadataQueryReader interface","IWICMetadataQueryReader interface [Windows Imaging Component]","GetContainerFormat method","IWICMetadataQueryReader.GetContainerFormat","IWICMetadataQueryReader::GetContainerFormat","_wic_codec_iwicmetadataqueryreader_getcontainerformat","wic._wic_codec_iwicmetadataqueryreader_getcontainerformat","wincodec/IWICMetadataQueryReader::GetContainerFormat"]
old-location: wic\_wic_codec_iwicmetadataqueryreader_getcontainerformat.htm
tech.root: wic
ms.assetid: f27c576a-3ff8-42bd-bad9-f7df18351a7f
ms.date: 12/05/2018
ms.keywords: GetContainerFormat, GetContainerFormat method [Windows Imaging Component], GetContainerFormat method [Windows Imaging Component],IWICMetadataQueryReader interface, IWICMetadataQueryReader interface [Windows Imaging Component],GetContainerFormat method, IWICMetadataQueryReader.GetContainerFormat, IWICMetadataQueryReader::GetContainerFormat, _wic_codec_iwicmetadataqueryreader_getcontainerformat, wic._wic_codec_iwicmetadataqueryreader_getcontainerformat, wincodec/IWICMetadataQueryReader::GetContainerFormat
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
 - IWICMetadataQueryReader::GetContainerFormat
 - wincodec/IWICMetadataQueryReader::GetContainerFormat
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
 - IWICMetadataQueryReader.GetContainerFormat
---

# IWICMetadataQueryReader::GetContainerFormat


## -description

Gets the metadata query readers container format.

## -parameters

### -param pguidContainerFormat [out]

Type: <b>GUID*</b>

Pointer that receives the cointainer format GUID.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/wincodec/nn-wincodec-iwicmetadataqueryreader">IWICMetadataQueryReader</a>



<a href="/windows/desktop/wic/-wic-codec-readingwritingmetadata">Overview of Reading and Writing Image Metadata</a>



<a href="/windows/desktop/wic/-wic-about-metadata">WIC Metadata Overview</a>