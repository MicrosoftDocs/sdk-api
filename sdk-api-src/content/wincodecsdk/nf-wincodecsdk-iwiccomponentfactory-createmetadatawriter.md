---
UID: NF:wincodecsdk.IWICComponentFactory.CreateMetadataWriter
title: IWICComponentFactory::CreateMetadataWriter (wincodecsdk.h)
description: Creates an IWICMetadataWriter based on the given parameters.
helpviewer_keywords: ["CreateMetadataWriter","CreateMetadataWriter method [Windows Imaging Component]","CreateMetadataWriter method [Windows Imaging Component]","IWICComponentFactory interface","IWICComponentFactory interface [Windows Imaging Component]","CreateMetadataWriter method","IWICComponentFactory.CreateMetadataWriter","IWICComponentFactory::CreateMetadataWriter","_wic_codec_iwiccomponentfactory_createmetadatawriter","wic._wic_codec_iwiccomponentfactory_createmetadatawriter","wincodecsdk/IWICComponentFactory::CreateMetadataWriter"]
old-location: wic\_wic_codec_iwiccomponentfactory_createmetadatawriter.htm
tech.root: wic
ms.assetid: e4e82125-bdaa-44c5-a370-22390764753b
ms.date: 12/05/2018
ms.keywords: CreateMetadataWriter, CreateMetadataWriter method [Windows Imaging Component], CreateMetadataWriter method [Windows Imaging Component],IWICComponentFactory interface, IWICComponentFactory interface [Windows Imaging Component],CreateMetadataWriter method, IWICComponentFactory.CreateMetadataWriter, IWICComponentFactory::CreateMetadataWriter, _wic_codec_iwiccomponentfactory_createmetadatawriter, wic._wic_codec_iwiccomponentfactory_createmetadatawriter, wincodecsdk/IWICComponentFactory::CreateMetadataWriter
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
 - IWICComponentFactory::CreateMetadataWriter
 - wincodecsdk/IWICComponentFactory::CreateMetadataWriter
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
 - IWICComponentFactory.CreateMetadataWriter
---

# IWICComponentFactory::CreateMetadataWriter


## -description

Creates an <a href="/windows/desktop/api/wincodecsdk/nn-wincodecsdk-iwicmetadatawriter">IWICMetadataWriter</a> based on the given parameters.

## -parameters

### -param guidMetadataFormat [in]

Type: <b>REFGUID</b>

The GUID of the desired metadata format.

### -param pguidVendor [in]

Type: <b>const GUID*</b>

Pointer to the GUID of the desired metadata reader vendor.

### -param dwMetadataOptions [in]

Type: <b>DWORD</b>

The <a href="/windows/desktop/api/wincodecsdk/ne-wincodecsdk-wicpersistoptions">WICPersistOptions</a> and <a href="/windows/desktop/api/wincodecsdk/ne-wincodecsdk-wicmetadatacreationoptions">WICMetadataCreationOptions</a> options to use when creating the metadata reader.

### -param ppIWriter [out]

Type: <b><a href="/windows/desktop/api/wincodecsdk/nn-wincodecsdk-iwicmetadatawriter">IWICMetadataWriter</a>**</b>

A pointer that receives a pointer to the new metadata writer.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.