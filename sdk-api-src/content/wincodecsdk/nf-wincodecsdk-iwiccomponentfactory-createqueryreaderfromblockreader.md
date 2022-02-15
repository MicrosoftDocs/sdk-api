---
UID: NF:wincodecsdk.IWICComponentFactory.CreateQueryReaderFromBlockReader
title: IWICComponentFactory::CreateQueryReaderFromBlockReader (wincodecsdk.h)
description: Creates a IWICMetadataQueryReader from the given IWICMetadataBlockReader.
helpviewer_keywords: ["CreateQueryReaderFromBlockReader","CreateQueryReaderFromBlockReader method [Windows Imaging Component]","CreateQueryReaderFromBlockReader method [Windows Imaging Component]","IWICComponentFactory interface","IWICComponentFactory interface [Windows Imaging Component]","CreateQueryReaderFromBlockReader method","IWICComponentFactory.CreateQueryReaderFromBlockReader","IWICComponentFactory::CreateQueryReaderFromBlockReader","_wic_codec_iwiccomponentfactory_createqueryreaderfromblockreader","wic._wic_codec_iwiccomponentfactory_createqueryreaderfromblockreader","wincodecsdk/IWICComponentFactory::CreateQueryReaderFromBlockReader"]
old-location: wic\_wic_codec_iwiccomponentfactory_createqueryreaderfromblockreader.htm
tech.root: wic
ms.assetid: 638d7c29-9c13-4a4b-ac60-8bccd01c65d5
ms.date: 12/05/2018
ms.keywords: CreateQueryReaderFromBlockReader, CreateQueryReaderFromBlockReader method [Windows Imaging Component], CreateQueryReaderFromBlockReader method [Windows Imaging Component],IWICComponentFactory interface, IWICComponentFactory interface [Windows Imaging Component],CreateQueryReaderFromBlockReader method, IWICComponentFactory.CreateQueryReaderFromBlockReader, IWICComponentFactory::CreateQueryReaderFromBlockReader, _wic_codec_iwiccomponentfactory_createqueryreaderfromblockreader, wic._wic_codec_iwiccomponentfactory_createqueryreaderfromblockreader, wincodecsdk/IWICComponentFactory::CreateQueryReaderFromBlockReader
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
 - IWICComponentFactory::CreateQueryReaderFromBlockReader
 - wincodecsdk/IWICComponentFactory::CreateQueryReaderFromBlockReader
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
 - IWICComponentFactory.CreateQueryReaderFromBlockReader
---

# IWICComponentFactory::CreateQueryReaderFromBlockReader


## -description

Creates a <a href="/windows/desktop/api/wincodec/nn-wincodec-iwicmetadataqueryreader">IWICMetadataQueryReader</a> from the given <a href="/windows/desktop/api/wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader">IWICMetadataBlockReader</a>.

## -parameters

### -param pIBlockReader [in]

Type: <b><a href="/windows/desktop/api/wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader">IWICMetadataBlockReader</a>*</b>

Pointer to the block reader to base the query reader on.

### -param ppIQueryReader [out]

Type: <b><a href="/windows/desktop/api/wincodec/nn-wincodec-iwicmetadataqueryreader">IWICMetadataQueryReader</a>**</b>

A pointer that receives a pointer to the new metadata query reader.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.