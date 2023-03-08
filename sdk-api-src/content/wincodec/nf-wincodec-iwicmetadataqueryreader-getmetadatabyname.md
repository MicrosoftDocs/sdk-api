---
UID: NF:wincodec.IWICMetadataQueryReader.GetMetadataByName
title: IWICMetadataQueryReader::GetMetadataByName (wincodec.h)
description: Retrieves the metadata block or item identified by a metadata query expression.
helpviewer_keywords: ["GetMetadataByName","GetMetadataByName method [Windows Imaging Component]","GetMetadataByName method [Windows Imaging Component]","IWICMetadataQueryReader interface","IWICMetadataQueryReader interface [Windows Imaging Component]","GetMetadataByName method","IWICMetadataQueryReader.GetMetadataByName","IWICMetadataQueryReader::GetMetadataByName","_wic_codec_iwicmetadataqueryreader_getmetadatabyname","wic._wic_codec_iwicmetadataqueryreader_getmetadatabyname","wincodec/IWICMetadataQueryReader::GetMetadataByName"]
old-location: wic\_wic_codec_iwicmetadataqueryreader_getmetadatabyname.htm
tech.root: wic
ms.assetid: 29d53a14-0509-4a96-9b8b-59952770559a
ms.date: 12/05/2018
ms.keywords: GetMetadataByName, GetMetadataByName method [Windows Imaging Component], GetMetadataByName method [Windows Imaging Component],IWICMetadataQueryReader interface, IWICMetadataQueryReader interface [Windows Imaging Component],GetMetadataByName method, IWICMetadataQueryReader.GetMetadataByName, IWICMetadataQueryReader::GetMetadataByName, _wic_codec_iwicmetadataqueryreader_getmetadatabyname, wic._wic_codec_iwicmetadataqueryreader_getmetadatabyname, wincodec/IWICMetadataQueryReader::GetMetadataByName
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
 - IWICMetadataQueryReader::GetMetadataByName
 - wincodec/IWICMetadataQueryReader::GetMetadataByName
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
 - IWICMetadataQueryReader.GetMetadataByName
---

# IWICMetadataQueryReader::GetMetadataByName


## -description

Retrieves the metadata block or item identified by a metadata query expression.

## -parameters

### -param wzName [in]

Type: <b>LPCWSTR</b>

The query expression to the requested metadata block or item.

### -param pvarValue [in, out]

Type: <b><a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a>*</b>

When this method returns, contains the metadata block or item requested.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

<b>GetMetadataByName</b> uses metadata query expressions to access embedded metadata. For more information on the metadata query language, see the <a href="/windows/desktop/wic/-wic-codec-metadataquerylanguage">Metadata Query Language Overview</a>.

If multiple blocks or items exist that are expressed by the same query expression, the first metadata block or item found will be returned.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/wincodec/nn-wincodec-iwicmetadataqueryreader">IWICMetadataQueryReader</a>



<a href="/windows/desktop/wic/-wic-codec-metadataquerylanguage">Metadata Query Language Overview</a>



<b>Other Resources</b>



<a href="/windows/desktop/wic/-wic-codec-readingwritingmetadata">Overview of Reading and Writing Image Metadata</a>



<a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a>



<a href="/windows/desktop/wic/-wic-about-metadata">WIC Metadata Overview</a>