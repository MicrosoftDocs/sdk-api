---
UID: NF:wincodecsdk.IWICComponentFactory.CreateMetadataWriter
title: IWICComponentFactory::CreateMetadataWriter
author: windows-sdk-content
description: Creates an IWICMetadataWriter based on the given parameters.
old-location: wic\_wic_codec_iwiccomponentfactory_createmetadatawriter.htm
old-project: wic
ms.assetid: e4e82125-bdaa-44c5-a370-22390764753b
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: CreateMetadataWriter, CreateMetadataWriter method [Windows Imaging Component], CreateMetadataWriter method [Windows Imaging Component],IWICComponentFactory interface, IWICComponentFactory interface [Windows Imaging Component],CreateMetadataWriter method, IWICComponentFactory.CreateMetadataWriter, IWICComponentFactory::CreateMetadataWriter, _wic_codec_iwiccomponentfactory_createmetadatawriter, wic._wic_codec_iwiccomponentfactory_createmetadatawriter, wincodecsdk/IWICComponentFactory::CreateMetadataWriter
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: wincodecsdk.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wincodecsdk.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: WICPersistOptions
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Windowscodecs.dll
api_name:
 - IWICComponentFactory.CreateMetadataWriter
product: Windows
targetos: Windows
req.lib: Windowscodecs.lib
req.dll: Windowscodecs.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# IWICComponentFactory::CreateMetadataWriter


## -description


Creates an <a href="https://msdn.microsoft.com/7e742a96-f9d0-49e1-80e4-31ec90680e60">IWICMetadataWriter</a> based on the given parameters.


## -parameters




### -param guidMetadataFormat [in]

Type: <b>REFGUID</b>

The GUID of the desired metadata format.


### -param pguidVendor [in]

Type: <b>const GUID*</b>

Pointer to the GUID of the desired metadata reader vendor.


### -param dwMetadataOptions [in]

Type: <b>DWORD</b>

The <a href="https://msdn.microsoft.com/8c17cfcc-4f09-4cb5-a3fa-4eb865123ad6">WICPersistOptions</a> and <a href="https://msdn.microsoft.com/41fece55-1ce4-455a-99b5-5ff0ecd27e07">WICMetadataCreationOptions</a> options to use when creating the metadata reader.


### -param ppIWriter [out]

Type: <b><a href="https://msdn.microsoft.com/7e742a96-f9d0-49e1-80e4-31ec90680e60">IWICMetadataWriter</a>**</b>

A pointer that receives a pointer to the new metadata writer.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



