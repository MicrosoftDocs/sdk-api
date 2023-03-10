---
UID: NF:wincodecsdk.IWICMetadataHandlerInfo.GetMetadataFormat
title: IWICMetadataHandlerInfo::GetMetadataFormat (wincodecsdk.h)
description: Retrieves the metadata format of the metadata handler.
helpviewer_keywords: ["GetMetadataFormat","GetMetadataFormat method [Windows Imaging Component]","GetMetadataFormat method [Windows Imaging Component]","IWICMetadataHandlerInfo interface","IWICMetadataHandlerInfo interface [Windows Imaging Component]","GetMetadataFormat method","IWICMetadataHandlerInfo.GetMetadataFormat","IWICMetadataHandlerInfo::GetMetadataFormat","_wic_codec_iwicmetadatahandlerinfo_getmetadataformat","wic._wic_codec_iwicmetadatahandlerinfo_getmetadataformat","wincodecsdk/IWICMetadataHandlerInfo::GetMetadataFormat"]
old-location: wic\_wic_codec_iwicmetadatahandlerinfo_getmetadataformat.htm
tech.root: wic
ms.assetid: 0a54d59a-3fe4-4636-94a0-5ee449d1d5c3
ms.date: 12/05/2018
ms.keywords: GetMetadataFormat, GetMetadataFormat method [Windows Imaging Component], GetMetadataFormat method [Windows Imaging Component],IWICMetadataHandlerInfo interface, IWICMetadataHandlerInfo interface [Windows Imaging Component],GetMetadataFormat method, IWICMetadataHandlerInfo.GetMetadataFormat, IWICMetadataHandlerInfo::GetMetadataFormat, _wic_codec_iwicmetadatahandlerinfo_getmetadataformat, wic._wic_codec_iwicmetadatahandlerinfo_getmetadataformat, wincodecsdk/IWICMetadataHandlerInfo::GetMetadataFormat
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
 - IWICMetadataHandlerInfo::GetMetadataFormat
 - wincodecsdk/IWICMetadataHandlerInfo::GetMetadataFormat
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
 - IWICMetadataHandlerInfo.GetMetadataFormat
---

# IWICMetadataHandlerInfo::GetMetadataFormat


## -description

Retrieves the metadata format of the metadata handler.

## -parameters

### -param pguidMetadataFormat [out]

Type: <b>GUID*</b>

Pointer that receives the metadata format GUID.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

