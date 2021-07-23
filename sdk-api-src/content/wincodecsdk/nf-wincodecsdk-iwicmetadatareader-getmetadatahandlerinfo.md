---
UID: NF:wincodecsdk.IWICMetadataReader.GetMetadataHandlerInfo
title: IWICMetadataReader::GetMetadataHandlerInfo (wincodecsdk.h)
description: Gets the metadata handler info associated with the reader.
helpviewer_keywords: ["GetMetadataHandlerInfo","GetMetadataHandlerInfo method [Windows Imaging Component]","GetMetadataHandlerInfo method [Windows Imaging Component]","IWICMetadataReader interface","IWICMetadataReader interface [Windows Imaging Component]","GetMetadataHandlerInfo method","IWICMetadataReader.GetMetadataHandlerInfo","IWICMetadataReader::GetMetadataHandlerInfo","_wic_codec_iwicmetadatareader_getmetadatahandlerinfo","wic._wic_codec_iwicmetadatareader_getmetadatahandlerinfo","wincodecsdk/IWICMetadataReader::GetMetadataHandlerInfo"]
old-location: wic\_wic_codec_iwicmetadatareader_getmetadatahandlerinfo.htm
tech.root: wic
ms.assetid: f3843044-4963-4e9f-8b5d-69d0201c9ec9
ms.date: 12/05/2018
ms.keywords: GetMetadataHandlerInfo, GetMetadataHandlerInfo method [Windows Imaging Component], GetMetadataHandlerInfo method [Windows Imaging Component],IWICMetadataReader interface, IWICMetadataReader interface [Windows Imaging Component],GetMetadataHandlerInfo method, IWICMetadataReader.GetMetadataHandlerInfo, IWICMetadataReader::GetMetadataHandlerInfo, _wic_codec_iwicmetadatareader_getmetadatahandlerinfo, wic._wic_codec_iwicmetadatareader_getmetadatahandlerinfo, wincodecsdk/IWICMetadataReader::GetMetadataHandlerInfo
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
 - IWICMetadataReader::GetMetadataHandlerInfo
 - wincodecsdk/IWICMetadataReader::GetMetadataHandlerInfo
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
 - IWICMetadataReader.GetMetadataHandlerInfo
---

# IWICMetadataReader::GetMetadataHandlerInfo


## -description

Gets the metadata handler info associated with the reader.

## -parameters

### -param ppIHandler [out]

Type: <b><a href="/windows/desktop/api/wincodecsdk/nn-wincodecsdk-iwicmetadatahandlerinfo">IWICMetadataHandlerInfo</a>**</b>

Pointer that receives a pointer to the <a href="/windows/desktop/api/wincodecsdk/nn-wincodecsdk-iwicmetadatahandlerinfo">IWICMetadataHandlerInfo</a>.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.