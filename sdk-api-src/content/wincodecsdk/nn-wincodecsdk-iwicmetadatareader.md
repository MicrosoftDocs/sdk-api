---
UID: NN:wincodecsdk.IWICMetadataReader
title: IWICMetadataReader (wincodecsdk.h)
description: Exposes methods that provide access to underlining metadata content. This interface is implemented by independent software vendors (ISVs) to create new metadata readers.
helpviewer_keywords: ["IWICMetadataReader","IWICMetadataReader interface [Windows Imaging Component]","IWICMetadataReader interface [Windows Imaging Component]","described","_wic_codec_iwicmetadatareader","wic._wic_codec_iwicmetadatareader","wincodecsdk/IWICMetadataReader"]
old-location: wic\_wic_codec_iwicmetadatareader.htm
tech.root: wic
ms.assetid: 0495ecf1-128a-4576-8420-0e79f1454015
ms.date: 12/05/2018
ms.keywords: IWICMetadataReader, IWICMetadataReader interface [Windows Imaging Component], IWICMetadataReader interface [Windows Imaging Component],described, _wic_codec_iwicmetadatareader, wic._wic_codec_iwicmetadatareader, wincodecsdk/IWICMetadataReader
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
 - IWICMetadataReader
 - wincodecsdk/IWICMetadataReader
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
 - IWICMetadataReader
---

# IWICMetadataReader interface


## -description

Exposes methods that provide access to underlining metadata content. This interface is implemented by independent software vendors (ISVs) to create new metadata readers.

## -inheritance

The <b>IWICMetadataReader</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWICMetadataReader</b> also has these types of members:

## -remarks

A metadata reader can be used to access metadata blocks and items within a metadata block instead of using a query reader. To directly access the metadata reader, query a decoder or its frames for the <a href="/windows/desktop/api/wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader">IWICMetadataBlockReader</a> interface to enumerate each metadata reader.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/wic/-wic-codec-metadatahandlers">Metadata Extensibility Overview</a>



<a href="/windows/desktop/wic/-wic-codec-metadataquerylanguage">Metadata Query Language Overview</a>



<a href="/windows/desktop/wic/-wic-codec-readingwritingmetadata">Overview of Reading and Writing Image Metadata</a>



<a href="/windows/desktop/wic/-wic-about-metadata">WIC Metadata Overview</a>
