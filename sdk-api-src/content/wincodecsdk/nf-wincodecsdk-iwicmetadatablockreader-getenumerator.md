---
UID: NF:wincodecsdk.IWICMetadataBlockReader.GetEnumerator
title: IWICMetadataBlockReader::GetEnumerator (wincodecsdk.h)
description: Retrieves an enumeration of IWICMetadataReader objects representing each of the top level metadata blocks.
helpviewer_keywords: ["GetEnumerator","GetEnumerator method [Windows Imaging Component]","GetEnumerator method [Windows Imaging Component]","IWICMetadataBlockReader interface","IWICMetadataBlockReader interface [Windows Imaging Component]","GetEnumerator method","IWICMetadataBlockReader.GetEnumerator","IWICMetadataBlockReader::GetEnumerator","_wic_codec_iwicmetadatablockreader_getenumerator","wic._wic_codec_iwicmetadatablockreader_getenumerator","wincodecsdk/IWICMetadataBlockReader::GetEnumerator"]
old-location: wic\_wic_codec_iwicmetadatablockreader_getenumerator.htm
tech.root: wic
ms.assetid: 81441e25-f124-4978-830d-2ade9cde6917
ms.date: 12/05/2018
ms.keywords: GetEnumerator, GetEnumerator method [Windows Imaging Component], GetEnumerator method [Windows Imaging Component],IWICMetadataBlockReader interface, IWICMetadataBlockReader interface [Windows Imaging Component],GetEnumerator method, IWICMetadataBlockReader.GetEnumerator, IWICMetadataBlockReader::GetEnumerator, _wic_codec_iwicmetadatablockreader_getenumerator, wic._wic_codec_iwicmetadatablockreader_getenumerator, wincodecsdk/IWICMetadataBlockReader::GetEnumerator
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
 - IWICMetadataBlockReader::GetEnumerator
 - wincodecsdk/IWICMetadataBlockReader::GetEnumerator
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
 - IWICMetadataBlockReader.GetEnumerator
---

# IWICMetadataBlockReader::GetEnumerator


## -description

Retrieves an enumeration of <a href="/windows/desktop/api/wincodecsdk/nn-wincodecsdk-iwicmetadatareader">IWICMetadataReader</a> objects representing each of the top level metadata blocks.

## -parameters

### -param ppIEnumMetadata [out]

Type: <b><a href="/windows/desktop/api/objidl/nn-objidl-ienumunknown">IEnumUnknown</a>**</b>

When this method returns, contains a pointer to an enumeration of <a href="/windows/desktop/api/wincodecsdk/nn-wincodecsdk-iwicmetadatareader">IWICMetadataReader</a> objects.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/wic/-wic-howtowriteacodec">How to Write a WIC-Enabled CODEC</a>



<a href="/windows/desktop/api/wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader">IWICMetadataBlockReader</a>



<b>Other Resources</b>



<a href="/windows/desktop/wic/-wic-codec-readingwritingmetadata">Overview of Reading and Writing Image Metadata</a>



<a href="/windows/desktop/wic/-wic-about-metadata">WIC Metadata Overview</a>



<a href="/windows/desktop/wic/-wic-about-windows-imaging-codec">Windows Imaging Component Overview</a>