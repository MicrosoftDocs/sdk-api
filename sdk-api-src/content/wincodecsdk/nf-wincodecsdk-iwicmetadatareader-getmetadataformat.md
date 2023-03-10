---
UID: NF:wincodecsdk.IWICMetadataReader.GetMetadataFormat
title: IWICMetadataReader::GetMetadataFormat (wincodecsdk.h)
description: Gets the metadata format associated with the reader.
helpviewer_keywords: ["GetMetadataFormat","GetMetadataFormat method [Windows Imaging Component]","GetMetadataFormat method [Windows Imaging Component]","IWICMetadataReader interface","IWICMetadataReader interface [Windows Imaging Component]","GetMetadataFormat method","IWICMetadataReader.GetMetadataFormat","IWICMetadataReader::GetMetadataFormat","_wic_codec_iwicmetadatareader_getmetadataformat","wic._wic_codec_iwicmetadatareader_getmetadataformat","wincodecsdk/IWICMetadataReader::GetMetadataFormat"]
old-location: wic\_wic_codec_iwicmetadatareader_getmetadataformat.htm
tech.root: wic
ms.assetid: 5dcbfac4-9a77-4453-be1e-3c42e94d548e
ms.date: 12/05/2018
ms.keywords: GetMetadataFormat, GetMetadataFormat method [Windows Imaging Component], GetMetadataFormat method [Windows Imaging Component],IWICMetadataReader interface, IWICMetadataReader interface [Windows Imaging Component],GetMetadataFormat method, IWICMetadataReader.GetMetadataFormat, IWICMetadataReader::GetMetadataFormat, _wic_codec_iwicmetadatareader_getmetadataformat, wic._wic_codec_iwicmetadatareader_getmetadataformat, wincodecsdk/IWICMetadataReader::GetMetadataFormat
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
 - IWICMetadataReader::GetMetadataFormat
 - wincodecsdk/IWICMetadataReader::GetMetadataFormat
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
 - IWICMetadataReader.GetMetadataFormat
---

# IWICMetadataReader::GetMetadataFormat


## -description

Gets the metadata format associated with the reader.

## -parameters

### -param pguidMetadataFormat [out]

Type: <b>GUID*</b>

Pointer that receives the metadata format GUID.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

