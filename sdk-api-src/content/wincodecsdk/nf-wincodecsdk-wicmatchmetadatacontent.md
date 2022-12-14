---
UID: NF:wincodecsdk.WICMatchMetadataContent
title: WICMatchMetadataContent function (wincodecsdk.h)
description: Obtains a metadata format GUID for a specified container format and vendor that best matches the content within a given stream.
helpviewer_keywords: ["WICMatchMetadataContent","WICMatchMetadataContent function [Windows Imaging Component]","_wic_codec_wicmatchmetadatacontent","wic._wic_codec_wicmatchmetadatacontent","wincodecsdk/WICMatchMetadataContent"]
old-location: wic\_wic_codec_wicmatchmetadatacontent.htm
tech.root: wic
ms.assetid: 2d1ab317-a77c-4e91-9455-e6738fd40e88
ms.date: 12/05/2018
ms.keywords: WICMatchMetadataContent, WICMatchMetadataContent function [Windows Imaging Component], _wic_codec_wicmatchmetadatacontent, wic._wic_codec_wicmatchmetadatacontent, wincodecsdk/WICMatchMetadataContent
req.header: wincodecsdk.h
req.include-header: Wincodec.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
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
 - WICMatchMetadataContent
 - wincodecsdk/WICMatchMetadataContent
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Windowscodecs.dll
 - Windowscodecs.lib
api_name:
 - WICMatchMetadataContent
---

# WICMatchMetadataContent function


## -description

Obtains a metadata format GUID for a specified container format and vendor that best matches the content within a given stream.

## -parameters

### -param guidContainerFormat [in]

Type: <b>REFGUID</b>

The container format GUID.

### -param pguidVendor [in]

Type: <b>const GUID*</b>

The vendor GUID.

### -param pIStream [in]

Type: <b><a href="/windows/desktop/api/objidl/nn-objidl-istream">IStream</a>*</b>

The content stream in which to match a metadata format.

### -param pguidMetadataFormat [out]

Type: <b>GUID*</b>

A pointer that receives a metadata format GUID for the given parameters.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.