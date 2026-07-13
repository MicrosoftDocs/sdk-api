---
UID: NF:wincodecsdk.WICSerializeMetadataContent
title: WICSerializeMetadataContent function (wincodecsdk.h)
description: Writes metadata into a given stream.
helpviewer_keywords: ["WICSerializeMetadataContent","WICSerializeMetadataContent function [Windows Imaging Component]","_wic_codec_wicserializemetadatacontent","wic._wic_codec_wicserializemetadatacontent","wincodecsdk/WICSerializeMetadataContent"]
old-location: wic\_wic_codec_wicserializemetadatacontent.htm
tech.root: wic
ms.assetid: 726b5e83-d5ab-4053-8f4c-34826fc0db55
ms.date: 12/05/2018
ms.keywords: WICSerializeMetadataContent, WICSerializeMetadataContent function [Windows Imaging Component], _wic_codec_wicserializemetadatacontent, wic._wic_codec_wicserializemetadatacontent, wincodecsdk/WICSerializeMetadataContent
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
 - WICSerializeMetadataContent
 - wincodecsdk/WICSerializeMetadataContent
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
 - WICSerializeMetadataContent
---

# WICSerializeMetadataContent function


## -description

Writes metadata into a given stream.

## -parameters

### -param guidContainerFormat [in]

Type: <b>REFGUID</b>

The container format GUID.

### -param pIWriter [in]

Type: <b><a href="/windows/desktop/api/wincodecsdk/nn-wincodecsdk-iwicmetadatawriter">IWICMetadataWriter</a>*</b>

The metadata writer to write metadata to the stream.

### -param dwPersistOptions [in]

Type: <b>DWORD</b>

The <a href="/windows/desktop/api/wincodecsdk/ne-wincodecsdk-wicpersistoptions">WICPersistOptions</a> options to use when writing the metadata.

### -param pIStream [in]

Type: <b><a href="/windows/desktop/api/objidl/nn-objidl-istream">IStream</a>*</b>

A pointer to the stream in which to write the metadata.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.