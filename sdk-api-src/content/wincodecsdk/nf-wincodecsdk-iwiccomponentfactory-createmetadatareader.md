---
UID: NF:wincodecsdk.IWICComponentFactory.CreateMetadataReader
title: IWICComponentFactory::CreateMetadataReader (wincodecsdk.h)
author: windows-sdk-content
description: Creates an IWICMetadataReader based on the given parameters.
old-location: wic\_wic_codec_iwiccomponentfactory_createmetadatareader.htm
tech.root: wic
ms.assetid: 3fc94831-1743-4269-97af-48116e2a4e1a
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CreateMetadataReader, CreateMetadataReader method [Windows Imaging Component], CreateMetadataReader method [Windows Imaging Component],IWICComponentFactory interface, IWICComponentFactory interface [Windows Imaging Component],CreateMetadataReader method, IWICComponentFactory.CreateMetadataReader, IWICComponentFactory::CreateMetadataReader, _wic_codec_iwiccomponentfactory_createmetadatareader, wic._wic_codec_iwiccomponentfactory_createmetadatareader, wincodecsdk/IWICComponentFactory::CreateMetadataReader
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
 - IWICComponentFactory.CreateMetadataReader
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWICComponentFactory::CreateMetadataReader


## -description


Creates an <a href="https://msdn.microsoft.com/0495ecf1-128a-4576-8420-0e79f1454015">IWICMetadataReader</a> based on the given parameters.


## -parameters




### -param guidMetadataFormat [in]

Type: <b>REFGUID</b>

The GUID of the desired metadata format.


### -param pguidVendor [in]

Type: <b>const GUID*</b>

Pointer to the GUID of the desired metadata reader vendor.


### -param dwOptions [in]

Type: <b>DWORD</b>

The <a href="https://msdn.microsoft.com/8c17cfcc-4f09-4cb5-a3fa-4eb865123ad6">WICPersistOptions</a> and <a href="https://msdn.microsoft.com/41fece55-1ce4-455a-99b5-5ff0ecd27e07">WICMetadataCreationOptions</a> options to use when creating the metadata reader.


### -param pIStream [in]

Type: <b><a href="https://msdn.microsoft.com/c6f60e37-eadc-46a1-94f6-cacc23613531">IStream</a>*</b>

Pointer to a stream in which to initialize the reader with. If <b>NULL</b>, the metadata reader will be empty.


### -param ppIReader [out]

Type: <b><a href="https://msdn.microsoft.com/0495ecf1-128a-4576-8420-0e79f1454015">IWICMetadataReader</a>**</b>

A pointer that receives a pointer to the new metadata reader. 


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



