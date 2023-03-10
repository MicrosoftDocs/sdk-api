---
UID: NF:wincodecsdk.IWICMetadataWriterInfo.CreateInstance
title: IWICMetadataWriterInfo::CreateInstance (wincodecsdk.h)
description: Creates an instance of an IWICMetadataWriter.
helpviewer_keywords: ["CreateInstance","CreateInstance method [Windows Imaging Component]","CreateInstance method [Windows Imaging Component]","IWICMetadataWriterInfo interface","IWICMetadataWriterInfo interface [Windows Imaging Component]","CreateInstance method","IWICMetadataWriterInfo.CreateInstance","IWICMetadataWriterInfo::CreateInstance","_wic_codec_iwicmetadatawriterinfo_createinstance","wic._wic_codec_iwicmetadatawriterinfo_createinstance","wincodecsdk/IWICMetadataWriterInfo::CreateInstance"]
old-location: wic\_wic_codec_iwicmetadatawriterinfo_createinstance.htm
tech.root: wic
ms.assetid: d4c701f7-7f79-41d8-864e-41e044b0ea09
ms.date: 12/05/2018
ms.keywords: CreateInstance, CreateInstance method [Windows Imaging Component], CreateInstance method [Windows Imaging Component],IWICMetadataWriterInfo interface, IWICMetadataWriterInfo interface [Windows Imaging Component],CreateInstance method, IWICMetadataWriterInfo.CreateInstance, IWICMetadataWriterInfo::CreateInstance, _wic_codec_iwicmetadatawriterinfo_createinstance, wic._wic_codec_iwicmetadatawriterinfo_createinstance, wincodecsdk/IWICMetadataWriterInfo::CreateInstance
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
 - IWICMetadataWriterInfo::CreateInstance
 - wincodecsdk/IWICMetadataWriterInfo::CreateInstance
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
 - IWICMetadataWriterInfo.CreateInstance
---

# IWICMetadataWriterInfo::CreateInstance


## -description

Creates an instance of an <a href="/windows/desktop/api/wincodecsdk/nn-wincodecsdk-iwicmetadatawriter">IWICMetadataWriter</a>.

## -parameters

### -param ppIWriter [out]

Type: <b><a href="/windows/desktop/api/wincodecsdk/nn-wincodecsdk-iwicmetadatawriter">IWICMetadataWriter</a>**</b>

Pointer that receives a pointer to a metadata writer.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.