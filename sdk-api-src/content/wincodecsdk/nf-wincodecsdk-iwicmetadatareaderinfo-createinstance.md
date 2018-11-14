---
UID: NF:wincodecsdk.IWICMetadataReaderInfo.CreateInstance
title: IWICMetadataReaderInfo::CreateInstance
author: windows-sdk-content
description: Creates an instance of an IWICMetadataReader.
old-location: wic\_wic_codec_iwicmetadatareaderinfo_createinstance.htm
tech.root: wic
ms.assetid: e6ee4ee9-8d9d-44f7-aab8-8e8ccfa7f942
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: CreateInstance, CreateInstance method [Windows Imaging Component], CreateInstance method [Windows Imaging Component],IWICMetadataReaderInfo interface, IWICMetadataReaderInfo interface [Windows Imaging Component],CreateInstance method, IWICMetadataReaderInfo.CreateInstance, IWICMetadataReaderInfo::CreateInstance, _wic_codec_iwicmetadatareaderinfo_createinstance, wic._wic_codec_iwicmetadatareaderinfo_createinstance, wincodecsdk/IWICMetadataReaderInfo::CreateInstance
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Windowscodecs.dll
api_name:
 - IWICMetadataReaderInfo.CreateInstance
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- wincodecsdk.h
: 
- IWICMetadataReaderInfo.CreateInstance
: 
---

# IWICMetadataReaderInfo::CreateInstance


## -description


Creates an instance of an <a href="https://msdn.microsoft.com/0495ecf1-128a-4576-8420-0e79f1454015">IWICMetadataReader</a>.


## -parameters




### -param ppIReader [out]

Type: <b><a href="https://msdn.microsoft.com/0495ecf1-128a-4576-8420-0e79f1454015">IWICMetadataReader</a>**</b>

Pointer that receives a pointer to a metadata reader.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



