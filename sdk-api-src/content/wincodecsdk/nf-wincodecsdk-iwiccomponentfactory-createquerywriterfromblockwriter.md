---
UID: NF:wincodecsdk.IWICComponentFactory.CreateQueryWriterFromBlockWriter
title: IWICComponentFactory::CreateQueryWriterFromBlockWriter
author: windows-sdk-content
description: Creates a IWICMetadataQueryWriter from the given IWICMetadataBlockWriter.
old-location: wic\_wic_codec_iwiccomponentfactory_createquerywriterfromblockwriter.htm
old-project: wic
ms.assetid: 1ad15754-c180-43e0-a307-6ff84f7eebd6
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: CreateQueryWriterFromBlockWriter, CreateQueryWriterFromBlockWriter method [Windows Imaging Component], CreateQueryWriterFromBlockWriter method [Windows Imaging Component],IWICComponentFactory interface, IWICComponentFactory interface [Windows Imaging Component],CreateQueryWriterFromBlockWriter method, IWICComponentFactory.CreateQueryWriterFromBlockWriter, IWICComponentFactory::CreateQueryWriterFromBlockWriter, _wic_codec_iwiccomponentfactory_createquerywriterfromblockwriter, wic._wic_codec_iwiccomponentfactory_createquerywriterfromblockwriter, wincodecsdk/IWICComponentFactory::CreateQueryWriterFromBlockWriter
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
req.typenames: WICPersistOptions
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Windowscodecs.dll
api_name:
-	IWICComponentFactory.CreateQueryWriterFromBlockWriter
product: Windows
targetos: Windows
req.lib: Windowscodecs.lib
req.dll: Windowscodecs.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# IWICComponentFactory::CreateQueryWriterFromBlockWriter


## -description


Creates a <a href="https://msdn.microsoft.com/065cccc3-778f-42c4-823a-354b08bbd1f1">IWICMetadataQueryWriter</a> from the given <a href="https://msdn.microsoft.com/d8e44c64-dd58-4d36-8add-0a0b2e2af5a4">IWICMetadataBlockWriter</a>.


## -parameters




### -param pIBlockWriter [in]

Type: <b><a href="https://msdn.microsoft.com/d8e44c64-dd58-4d36-8add-0a0b2e2af5a4">IWICMetadataBlockWriter</a>*</b>

Pointer to the metadata block reader to base the metadata query writer on.


### -param ppIQueryWriter [out]

Type: <b><a href="https://msdn.microsoft.com/065cccc3-778f-42c4-823a-354b08bbd1f1">IWICMetadataQueryWriter</a>**</b>

A pointer that receives a pointer to the new metadata query writer.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



