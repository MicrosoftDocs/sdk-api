---
UID: NF:wincodec.IWICImagingFactory.CreateQueryWriterFromReader
title: IWICImagingFactory::CreateQueryWriterFromReader (wincodec.h)
author: windows-sdk-content
description: Creates a new instance of a query writer based on the given query reader. The query writer will be pre-populated with metadata from the query reader.
old-location: wic\_wic_codec_iwicimagingfactory_createquerywriterfromreader.htm
tech.root: wic
ms.assetid: 71c278f8-546f-4351-9e2c-b9cd9806ccfc
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CreateQueryWriterFromReader, CreateQueryWriterFromReader method [Windows Imaging Component], CreateQueryWriterFromReader method [Windows Imaging Component],IWICImagingFactory interface, IWICImagingFactory interface [Windows Imaging Component],CreateQueryWriterFromReader method, IWICImagingFactory.CreateQueryWriterFromReader, IWICImagingFactory::CreateQueryWriterFromReader, _wic_codec_iwicimagingfactory_createquerywriterfromreader, wic._wic_codec_iwicimagingfactory_createquerywriterfromreader, wincodec/IWICImagingFactory::CreateQueryWriterFromReader
ms.topic: method
req.header: wincodec.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wincodec.idl
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
 - IWICImagingFactory.CreateQueryWriterFromReader
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWICImagingFactory::CreateQueryWriterFromReader


## -description


Creates a new instance of a query writer based on the given query reader. The query writer will be pre-populated with metadata from the query reader.


## -parameters




### -param pIQueryReader [in]

Type: <b><a href="https://msdn.microsoft.com/588e00d2-e166-4ce5-bd8a-50ad0d5a3db9">IWICMetadataQueryReader</a>*</b>

The <a href="https://msdn.microsoft.com/588e00d2-e166-4ce5-bd8a-50ad0d5a3db9">IWICMetadataQueryReader</a> to create the <a href="https://msdn.microsoft.com/065cccc3-778f-42c4-823a-354b08bbd1f1">IWICMetadataQueryWriter</a> from.


### -param pguidVendor [in]

Type: <b>const GUID*</b>

The GUID for the preferred metadata writer vendor. Use <b>NULL</b> if no preferred vendor.


### -param ppIQueryWriter [out]

Type: <b><a href="https://msdn.microsoft.com/065cccc3-778f-42c4-823a-354b08bbd1f1">IWICMetadataQueryWriter</a>**</b>

When this method returns, contains a pointer to a new metadata writer.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/30d155b1-a46c-46c4-9f8f-fb56dc6bf0a9">IWICImagingFactory</a>



<a href="https://msdn.microsoft.com/5ffa0a69-b53d-4be3-b802-deaaa743e6bd">Metadata Query Language Overview</a>



<a href="https://msdn.microsoft.com/b1e0b936-a13a-42dd-8470-957ba1d90423">Overview of Reading and Writing Image Metadata</a>



<a href="https://msdn.microsoft.com/35727810-3c4c-4c11-a4a2-3ae2cf3b8142">WIC Metadata Overview</a>
 

 

