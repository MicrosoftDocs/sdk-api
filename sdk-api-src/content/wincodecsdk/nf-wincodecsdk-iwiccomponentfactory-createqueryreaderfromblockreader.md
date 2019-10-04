---
UID: NF:wincodecsdk.IWICComponentFactory.CreateQueryReaderFromBlockReader
title: IWICComponentFactory::CreateQueryReaderFromBlockReader (wincodecsdk.h)
author: windows-sdk-content
description: Creates a IWICMetadataQueryReader from the given IWICMetadataBlockReader.
old-location: wic\_wic_codec_iwiccomponentfactory_createqueryreaderfromblockreader.htm
tech.root: wic
ms.assetid: 638d7c29-9c13-4a4b-ac60-8bccd01c65d5
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CreateQueryReaderFromBlockReader, CreateQueryReaderFromBlockReader method [Windows Imaging Component], CreateQueryReaderFromBlockReader method [Windows Imaging Component],IWICComponentFactory interface, IWICComponentFactory interface [Windows Imaging Component],CreateQueryReaderFromBlockReader method, IWICComponentFactory.CreateQueryReaderFromBlockReader, IWICComponentFactory::CreateQueryReaderFromBlockReader, _wic_codec_iwiccomponentfactory_createqueryreaderfromblockreader, wic._wic_codec_iwiccomponentfactory_createqueryreaderfromblockreader, wincodecsdk/IWICComponentFactory::CreateQueryReaderFromBlockReader
ms.topic: method
f1_keywords: 
 - "wincodecsdk/IWICComponentFactory.CreateQueryReaderFromBlockReader"
dev_langs:
 - c++
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
 - IWICComponentFactory.CreateQueryReaderFromBlockReader
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWICComponentFactory::CreateQueryReaderFromBlockReader


## -description


Creates a <a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nn-wincodec-iwicmetadataqueryreader">IWICMetadataQueryReader</a> from the given <a href="https://docs.microsoft.com/windows/desktop/api/wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader">IWICMetadataBlockReader</a>.


## -parameters




### -param pIBlockReader [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader">IWICMetadataBlockReader</a>*</b>

Pointer to the block reader to base the query reader on.


### -param ppIQueryReader [out]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nn-wincodec-iwicmetadataqueryreader">IWICMetadataQueryReader</a>**</b>

A pointer that receives a pointer to the new metadata query reader.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



