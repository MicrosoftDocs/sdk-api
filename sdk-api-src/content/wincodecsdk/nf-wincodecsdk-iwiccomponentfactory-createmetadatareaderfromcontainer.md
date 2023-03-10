---
UID: NF:wincodecsdk.IWICComponentFactory.CreateMetadataReaderFromContainer
title: IWICComponentFactory::CreateMetadataReaderFromContainer (wincodecsdk.h)
description: Creates an IWICMetadataReader based on the given parameters. (IWICComponentFactory.CreateMetadataReaderFromContainer)
helpviewer_keywords: ["CreateMetadataReaderFromContainer","CreateMetadataReaderFromContainer method [Windows Imaging Component]","CreateMetadataReaderFromContainer method [Windows Imaging Component]","IWICComponentFactory interface","IWICComponentFactory interface [Windows Imaging Component]","CreateMetadataReaderFromContainer method","IWICComponentFactory.CreateMetadataReaderFromContainer","IWICComponentFactory::CreateMetadataReaderFromContainer","_wic_codec_iwiccomponentfactory_createmetadatareaderfromcontainer","wic._wic_codec_iwiccomponentfactory_createmetadatareaderfromcontainer","wincodecsdk/IWICComponentFactory::CreateMetadataReaderFromContainer"]
old-location: wic\_wic_codec_iwiccomponentfactory_createmetadatareaderfromcontainer.htm
tech.root: wic
ms.assetid: 876d2d5a-8247-4e4a-b402-0ee02d9b0158
ms.date: 12/05/2018
ms.keywords: CreateMetadataReaderFromContainer, CreateMetadataReaderFromContainer method [Windows Imaging Component], CreateMetadataReaderFromContainer method [Windows Imaging Component],IWICComponentFactory interface, IWICComponentFactory interface [Windows Imaging Component],CreateMetadataReaderFromContainer method, IWICComponentFactory.CreateMetadataReaderFromContainer, IWICComponentFactory::CreateMetadataReaderFromContainer, _wic_codec_iwiccomponentfactory_createmetadatareaderfromcontainer, wic._wic_codec_iwiccomponentfactory_createmetadatareaderfromcontainer, wincodecsdk/IWICComponentFactory::CreateMetadataReaderFromContainer
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
 - IWICComponentFactory::CreateMetadataReaderFromContainer
 - wincodecsdk/IWICComponentFactory::CreateMetadataReaderFromContainer
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
 - IWICComponentFactory.CreateMetadataReaderFromContainer
---

# IWICComponentFactory::CreateMetadataReaderFromContainer


## -description

Creates an <a href="/windows/desktop/api/wincodecsdk/nn-wincodecsdk-iwicmetadatareader">IWICMetadataReader</a> based on the given parameters.

## -parameters

### -param guidContainerFormat [in]

Type: <b>REFGUID</b>

The container format GUID to base the reader on.

### -param pguidVendor [in]

Type: <b>const GUID*</b>

Pointer to the vendor GUID of the metadata reader.

### -param dwOptions [in]

Type: <b>DWORD</b>

The <a href="/windows/desktop/api/wincodecsdk/ne-wincodecsdk-wicpersistoptions">WICPersistOptions</a> and <a href="/windows/desktop/api/wincodecsdk/ne-wincodecsdk-wicmetadatacreationoptions">WICMetadataCreationOptions</a> options to use when creating the metadata reader.

### -param pIStream [in]

Type: <b><a href="/windows/desktop/api/objidl/nn-objidl-istream">IStream</a>*</b>

Pointer to a stream in which to initialize the reader with. If <b>NULL</b>, the metadata reader will be empty.

### -param ppIReader [out]

Type: <b><a href="/windows/desktop/api/wincodecsdk/nn-wincodecsdk-iwicmetadatareader">IWICMetadataReader</a>**</b>

A pointer that receives a pointer to the new metadata reader

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.
