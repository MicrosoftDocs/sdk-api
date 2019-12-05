---
UID: NF:wincodecsdk.IWICComponentFactory.CreateQueryWriterFromBlockWriter
title: IWICComponentFactory::CreateQueryWriterFromBlockWriter (wincodecsdk.h)
description: Creates a IWICMetadataQueryWriter from the given IWICMetadataBlockWriter.
old-location: wic\_wic_codec_iwiccomponentfactory_createquerywriterfromblockwriter.htm
tech.root: wic
ms.assetid: 1ad15754-c180-43e0-a307-6ff84f7eebd6
ms.date: 12/05/2018
ms.keywords: CreateQueryWriterFromBlockWriter, CreateQueryWriterFromBlockWriter method [Windows Imaging Component], CreateQueryWriterFromBlockWriter method [Windows Imaging Component],IWICComponentFactory interface, IWICComponentFactory interface [Windows Imaging Component],CreateQueryWriterFromBlockWriter method, IWICComponentFactory.CreateQueryWriterFromBlockWriter, IWICComponentFactory::CreateQueryWriterFromBlockWriter, _wic_codec_iwiccomponentfactory_createquerywriterfromblockwriter, wic._wic_codec_iwiccomponentfactory_createquerywriterfromblockwriter, wincodecsdk/IWICComponentFactory::CreateQueryWriterFromBlockWriter
ms.topic: method
f1_keywords:
- wincodecsdk/IWICComponentFactory.CreateQueryWriterFromBlockWriter
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
- IWICComponentFactory.CreateQueryWriterFromBlockWriter
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWICComponentFactory::CreateQueryWriterFromBlockWriter


## -description


Creates a <a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nn-wincodec-iwicmetadataquerywriter">IWICMetadataQueryWriter</a> from the given <a href="https://docs.microsoft.com/windows/desktop/api/wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter">IWICMetadataBlockWriter</a>.


## -parameters




### -param pIBlockWriter [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter">IWICMetadataBlockWriter</a>*</b>

Pointer to the metadata block reader to base the metadata query writer on.


### -param ppIQueryWriter [out]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nn-wincodec-iwicmetadataquerywriter">IWICMetadataQueryWriter</a>**</b>

A pointer that receives a pointer to the new metadata query writer.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



