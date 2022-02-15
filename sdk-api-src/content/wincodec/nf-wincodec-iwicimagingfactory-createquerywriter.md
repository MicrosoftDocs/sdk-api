---
UID: NF:wincodec.IWICImagingFactory.CreateQueryWriter
title: IWICImagingFactory::CreateQueryWriter (wincodec.h)
description: Creates a new instance of a query writer.
helpviewer_keywords: ["CreateQueryWriter","CreateQueryWriter method [Windows Imaging Component]","CreateQueryWriter method [Windows Imaging Component]","IWICImagingFactory interface","IWICImagingFactory interface [Windows Imaging Component]","CreateQueryWriter method","IWICImagingFactory.CreateQueryWriter","IWICImagingFactory::CreateQueryWriter","_wic_codec_iwicimagingfactory_createquerywriter","wic._wic_codec_iwicimagingfactory_createquerywriter","wincodec/IWICImagingFactory::CreateQueryWriter"]
old-location: wic\_wic_codec_iwicimagingfactory_createquerywriter.htm
tech.root: wic
ms.assetid: c2998d22-68c5-45de-a651-6f67c6f5234a
ms.date: 12/05/2018
ms.keywords: CreateQueryWriter, CreateQueryWriter method [Windows Imaging Component], CreateQueryWriter method [Windows Imaging Component],IWICImagingFactory interface, IWICImagingFactory interface [Windows Imaging Component],CreateQueryWriter method, IWICImagingFactory.CreateQueryWriter, IWICImagingFactory::CreateQueryWriter, _wic_codec_iwicimagingfactory_createquerywriter, wic._wic_codec_iwicimagingfactory_createquerywriter, wincodec/IWICImagingFactory::CreateQueryWriter
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
 - IWICImagingFactory::CreateQueryWriter
 - wincodec/IWICImagingFactory::CreateQueryWriter
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
 - IWICImagingFactory.CreateQueryWriter
---

# IWICImagingFactory::CreateQueryWriter


## -description

Creates a new instance of a query writer.

## -parameters

### -param guidMetadataFormat [in]

Type: <b>REFGUID</b>

The GUID for the desired metadata format.

### -param pguidVendor [in]

Type: <b>const GUID*</b>

The GUID for the preferred metadata writer vendor. Use <b>NULL</b> if no preferred vendor.

### -param ppIQueryWriter [out]

Type: <b><a href="/windows/desktop/api/wincodec/nn-wincodec-iwicmetadataquerywriter">IWICMetadataQueryWriter</a>**</b>

When this method returns, contains a pointer to a new <a href="/windows/desktop/api/wincodec/nn-wincodec-iwicmetadataquerywriter">IWICMetadataQueryWriter</a>.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/wincodec/nn-wincodec-iwicimagingfactory">IWICImagingFactory</a>



<a href="/windows/desktop/wic/-wic-codec-metadataquerylanguage">Metadata Query Language Overview</a>



<a href="/windows/desktop/wic/-wic-codec-readingwritingmetadata">Overview of Reading and Writing Image Metadata</a>



<a href="/windows/desktop/wic/-wic-guids-clsids">WIC GUIDs and CLSIDs</a>



<a href="/windows/desktop/wic/-wic-about-metadata">WIC Metadata Overview</a>