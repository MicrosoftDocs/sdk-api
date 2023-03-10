---
UID: NN:wincodecsdk.IWICMetadataWriter
title: IWICMetadataWriter (wincodecsdk.h)
description: Exposes methods that provide access to writing metadata content. This is implemented by independent software vendors (ISVs) to create new metadata writers.
helpviewer_keywords: ["IWICMetadataWriter","IWICMetadataWriter interface [Windows Imaging Component]","IWICMetadataWriter interface [Windows Imaging Component]","described","_wic_codec_iwicmetadatawriter","wic._wic_codec_iwicmetadatawriter","wincodecsdk/IWICMetadataWriter"]
old-location: wic\_wic_codec_iwicmetadatawriter.htm
tech.root: wic
ms.assetid: 7e742a96-f9d0-49e1-80e4-31ec90680e60
ms.date: 12/05/2018
ms.keywords: IWICMetadataWriter, IWICMetadataWriter interface [Windows Imaging Component], IWICMetadataWriter interface [Windows Imaging Component],described, _wic_codec_iwicmetadatawriter, wic._wic_codec_iwicmetadatawriter, wincodecsdk/IWICMetadataWriter
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
 - IWICMetadataWriter
 - wincodecsdk/IWICMetadataWriter
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
 - IWICMetadataWriter
---

# IWICMetadataWriter interface


## -description

Exposes methods that provide access to writing metadata content. This is implemented by independent software vendors (ISVs) to create new metadata writers.

## -inheritance

The <b>IWICMetadataWriter</b> interface inherits from <a href="/windows/desktop/api/wincodecsdk/nn-wincodecsdk-iwicmetadatareader">IWICMetadataReader</a>. <b>IWICMetadataWriter</b> also has these types of members:

## -remarks

A metadata writer can be used to write metadata blocks and items within a metadata block instead of using a query writer. To directly access the metadata writer, query an encoder or its frames for the <a href="/windows/desktop/api/wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter">IWICMetadataBlockWriter</a> interface to enumerate each metadata writer.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/wincodecsdk/nn-wincodecsdk-iwicmetadatareader">IWICMetadataReader</a>



<a href="/windows/desktop/wic/-wic-codec-metadatahandlers">Metadata Extensibility Overview</a>



<a href="/windows/desktop/wic/-wic-codec-metadataquerylanguage">Metadata Query Language Overview</a>



<a href="/windows/desktop/wic/-wic-codec-readingwritingmetadata">Overview of Reading and Writing Image Metadata</a>



<a href="/windows/desktop/wic/-wic-about-metadata">WIC Metadata Overview</a>
