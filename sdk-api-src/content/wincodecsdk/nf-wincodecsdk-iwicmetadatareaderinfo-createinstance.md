---
UID: NF:wincodecsdk.IWICMetadataReaderInfo.CreateInstance
title: IWICMetadataReaderInfo::CreateInstance (wincodecsdk.h)
description: Creates an instance of an IWICMetadataReader.
helpviewer_keywords: ["CreateInstance","CreateInstance method [Windows Imaging Component]","CreateInstance method [Windows Imaging Component]","IWICMetadataReaderInfo interface","IWICMetadataReaderInfo interface [Windows Imaging Component]","CreateInstance method","IWICMetadataReaderInfo.CreateInstance","IWICMetadataReaderInfo::CreateInstance","_wic_codec_iwicmetadatareaderinfo_createinstance","wic._wic_codec_iwicmetadatareaderinfo_createinstance","wincodecsdk/IWICMetadataReaderInfo::CreateInstance"]
old-location: wic\_wic_codec_iwicmetadatareaderinfo_createinstance.htm
tech.root: wic
ms.assetid: e6ee4ee9-8d9d-44f7-aab8-8e8ccfa7f942
ms.date: 12/05/2018
ms.keywords: CreateInstance, CreateInstance method [Windows Imaging Component], CreateInstance method [Windows Imaging Component],IWICMetadataReaderInfo interface, IWICMetadataReaderInfo interface [Windows Imaging Component],CreateInstance method, IWICMetadataReaderInfo.CreateInstance, IWICMetadataReaderInfo::CreateInstance, _wic_codec_iwicmetadatareaderinfo_createinstance, wic._wic_codec_iwicmetadatareaderinfo_createinstance, wincodecsdk/IWICMetadataReaderInfo::CreateInstance
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
 - IWICMetadataReaderInfo::CreateInstance
 - wincodecsdk/IWICMetadataReaderInfo::CreateInstance
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
 - IWICMetadataReaderInfo.CreateInstance
---

# IWICMetadataReaderInfo::CreateInstance


## -description

Creates an instance of an <a href="/windows/desktop/api/wincodecsdk/nn-wincodecsdk-iwicmetadatareader">IWICMetadataReader</a>.

## -parameters

### -param ppIReader [out]

Type: <b><a href="/windows/desktop/api/wincodecsdk/nn-wincodecsdk-iwicmetadatareader">IWICMetadataReader</a>**</b>

Pointer that receives a pointer to a metadata reader.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.