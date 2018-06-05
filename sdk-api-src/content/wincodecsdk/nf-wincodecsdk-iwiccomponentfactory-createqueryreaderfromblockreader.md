---
UID: NF:wincodecsdk.IWICComponentFactory.CreateQueryReaderFromBlockReader
title: IWICComponentFactory::CreateQueryReaderFromBlockReader
author: windows-sdk-content
description: Creates a IWICMetadataQueryReader from the given IWICMetadataBlockReader.
old-location: wic\_wic_codec_iwiccomponentfactory_createqueryreaderfromblockreader.htm
old-project: wic
ms.assetid: 638d7c29-9c13-4a4b-ac60-8bccd01c65d5
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: CreateQueryReaderFromBlockReader, CreateQueryReaderFromBlockReader method [Windows Imaging Component], CreateQueryReaderFromBlockReader method [Windows Imaging Component],IWICComponentFactory interface, IWICComponentFactory interface [Windows Imaging Component],CreateQueryReaderFromBlockReader method, IWICComponentFactory.CreateQueryReaderFromBlockReader, IWICComponentFactory::CreateQueryReaderFromBlockReader, _wic_codec_iwiccomponentfactory_createqueryreaderfromblockreader, wic._wic_codec_iwiccomponentfactory_createqueryreaderfromblockreader, wincodecsdk/IWICComponentFactory::CreateQueryReaderFromBlockReader
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
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Windowscodecs.dll
api_name:
-	IWICComponentFactory.CreateQueryReaderFromBlockReader
product: Windows
targetos: Windows
req.lib: Windowscodecs.lib
req.dll: Windowscodecs.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# IWICComponentFactory::CreateQueryReaderFromBlockReader


## -description


Creates a <a href="https://msdn.microsoft.com/588e00d2-e166-4ce5-bd8a-50ad0d5a3db9">IWICMetadataQueryReader</a> from the given <a href="https://msdn.microsoft.com/09614b44-ebc2-44f4-9755-9df62f1b2178">IWICMetadataBlockReader</a>.


## -parameters




### -param pIBlockReader [in]

Type: <b><a href="https://msdn.microsoft.com/09614b44-ebc2-44f4-9755-9df62f1b2178">IWICMetadataBlockReader</a>*</b>

Pointer to the block reader to base the query reader on.


### -param ppIQueryReader [out]

Type: <b><a href="https://msdn.microsoft.com/588e00d2-e166-4ce5-bd8a-50ad0d5a3db9">IWICMetadataQueryReader</a>**</b>

A pointer that receives a pointer to the new metadata query reader.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



