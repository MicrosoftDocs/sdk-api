---
UID: NF:wincodec.IWICImagingFactory.CreateQueryWriterFromReader
title: IWICImagingFactory::CreateQueryWriterFromReader (wincodec.h)
description: Creates a new instance of a query writer based on the given query reader. The query writer will be pre-populated with metadata from the query reader.
helpviewer_keywords: ["CreateQueryWriterFromReader","CreateQueryWriterFromReader method [Windows Imaging Component]","CreateQueryWriterFromReader method [Windows Imaging Component]","IWICImagingFactory interface","IWICImagingFactory interface [Windows Imaging Component]","CreateQueryWriterFromReader method","IWICImagingFactory.CreateQueryWriterFromReader","IWICImagingFactory::CreateQueryWriterFromReader","_wic_codec_iwicimagingfactory_createquerywriterfromreader","wic._wic_codec_iwicimagingfactory_createquerywriterfromreader","wincodec/IWICImagingFactory::CreateQueryWriterFromReader"]
old-location: wic\_wic_codec_iwicimagingfactory_createquerywriterfromreader.htm
tech.root: wic
ms.assetid: 71c278f8-546f-4351-9e2c-b9cd9806ccfc
ms.date: 12/05/2018
ms.keywords: CreateQueryWriterFromReader, CreateQueryWriterFromReader method [Windows Imaging Component], CreateQueryWriterFromReader method [Windows Imaging Component],IWICImagingFactory interface, IWICImagingFactory interface [Windows Imaging Component],CreateQueryWriterFromReader method, IWICImagingFactory.CreateQueryWriterFromReader, IWICImagingFactory::CreateQueryWriterFromReader, _wic_codec_iwicimagingfactory_createquerywriterfromreader, wic._wic_codec_iwicimagingfactory_createquerywriterfromreader, wincodec/IWICImagingFactory::CreateQueryWriterFromReader
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWICImagingFactory::CreateQueryWriterFromReader
 - wincodec/IWICImagingFactory::CreateQueryWriterFromReader
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
 - IWICImagingFactory.CreateQueryWriterFromReader
---

# IWICImagingFactory::CreateQueryWriterFromReader


## -description

Creates a new instance of a query writer based on the given query reader. The query writer will be pre-populated with metadata from the query reader.

## -parameters

### -param pIQueryReader [in]

Type: <b><a href="/windows/desktop/api/wincodec/nn-wincodec-iwicmetadataqueryreader">IWICMetadataQueryReader</a>*</b>

The <a href="/windows/desktop/api/wincodec/nn-wincodec-iwicmetadataqueryreader">IWICMetadataQueryReader</a> to create the <a href="/windows/desktop/api/wincodec/nn-wincodec-iwicmetadataquerywriter">IWICMetadataQueryWriter</a> from.

### -param pguidVendor [in]

Type: <b>const GUID*</b>

The GUID for the preferred metadata writer vendor. Use <b>NULL</b> if no preferred vendor.

### -param ppIQueryWriter [out]

Type: <b><a href="/windows/desktop/api/wincodec/nn-wincodec-iwicmetadataquerywriter">IWICMetadataQueryWriter</a>**</b>

When this method returns, contains a pointer to a new metadata writer.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/wincodec/nn-wincodec-iwicimagingfactory">IWICImagingFactory</a>



<a href="/windows/desktop/wic/-wic-codec-metadataquerylanguage">Metadata Query Language Overview</a>



<a href="/windows/desktop/wic/-wic-codec-readingwritingmetadata">Overview of Reading and Writing Image Metadata</a>



<a href="/windows/desktop/wic/-wic-about-metadata">WIC Metadata Overview</a>