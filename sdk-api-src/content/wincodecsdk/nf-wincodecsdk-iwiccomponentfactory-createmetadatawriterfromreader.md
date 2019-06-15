---
UID: NF:wincodecsdk.IWICComponentFactory.CreateMetadataWriterFromReader
title: IWICComponentFactory::CreateMetadataWriterFromReader (wincodecsdk.h)
author: windows-sdk-content
description: Creates an IWICMetadataWriter from the given IWICMetadataReader.
old-location: wic\_wic_codec_iwiccomponentfactory_createmetadatawriterfromreader.htm
tech.root: wic
ms.assetid: f321483c-186b-4405-84f6-f58fddf6b60f
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CreateMetadataWriterFromReader, CreateMetadataWriterFromReader method [Windows Imaging Component], CreateMetadataWriterFromReader method [Windows Imaging Component],IWICComponentFactory interface, IWICComponentFactory interface [Windows Imaging Component],CreateMetadataWriterFromReader method, IWICComponentFactory.CreateMetadataWriterFromReader, IWICComponentFactory::CreateMetadataWriterFromReader, _wic_codec_iwiccomponentfactory_createmetadatawriterfromreader, wic._wic_codec_iwiccomponentfactory_createmetadatawriterfromreader, wincodecsdk/IWICComponentFactory::CreateMetadataWriterFromReader
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
 - IWICComponentFactory.CreateMetadataWriterFromReader
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWICComponentFactory::CreateMetadataWriterFromReader


## -description


Creates an <a href="https://docs.microsoft.com/windows/desktop/api/wincodecsdk/nn-wincodecsdk-iwicmetadatawriter">IWICMetadataWriter</a> from the given <a href="https://docs.microsoft.com/windows/desktop/api/wincodecsdk/nn-wincodecsdk-iwicmetadatareader">IWICMetadataReader</a>.


## -parameters




### -param pIReader [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/wincodecsdk/nn-wincodecsdk-iwicmetadatareader">IWICMetadataReader</a>*</b>

Pointer to the metadata reader to base the metadata writer on.


### -param pguidVendor [in]

Type: <b>const GUID*</b>

Pointer to the GUID of the desired metadata reader vendor.


### -param ppIWriter [out]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/wincodecsdk/nn-wincodecsdk-iwicmetadatawriter">IWICMetadataWriter</a>**</b>

A pointer that receives a pointer to the new metadata writer.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



