---
UID: NF:wincodec.IWICMetadataQueryReader.GetEnumerator
title: IWICMetadataQueryReader::GetEnumerator (wincodec.h)
description: Gets an enumerator of all metadata items at the current relative location within the metadata hierarchy.
helpviewer_keywords: ["GetEnumerator","GetEnumerator method [Windows Imaging Component]","GetEnumerator method [Windows Imaging Component]","IWICMetadataQueryReader interface","IWICMetadataQueryReader interface [Windows Imaging Component]","GetEnumerator method","IWICMetadataQueryReader.GetEnumerator","IWICMetadataQueryReader::GetEnumerator","_wic_codec_iwicmetadataqueryreader_getenumerator","wic._wic_codec_iwicmetadataqueryreader_getenumerator","wincodec/IWICMetadataQueryReader::GetEnumerator"]
old-location: wic\_wic_codec_iwicmetadataqueryreader_getenumerator.htm
tech.root: wic
ms.assetid: 8e9b0da5-90e3-4398-9113-0fb86a94cb0c
ms.date: 12/05/2018
ms.keywords: GetEnumerator, GetEnumerator method [Windows Imaging Component], GetEnumerator method [Windows Imaging Component],IWICMetadataQueryReader interface, IWICMetadataQueryReader interface [Windows Imaging Component],GetEnumerator method, IWICMetadataQueryReader.GetEnumerator, IWICMetadataQueryReader::GetEnumerator, _wic_codec_iwicmetadataqueryreader_getenumerator, wic._wic_codec_iwicmetadataqueryreader_getenumerator, wincodec/IWICMetadataQueryReader::GetEnumerator
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
 - IWICMetadataQueryReader::GetEnumerator
 - wincodec/IWICMetadataQueryReader::GetEnumerator
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
 - IWICMetadataQueryReader.GetEnumerator
---

# IWICMetadataQueryReader::GetEnumerator


## -description

Gets an enumerator of all metadata items at the current relative location within the metadata hierarchy.

## -parameters

### -param ppIEnumString [out]

Type: <b><a href="/windows/desktop/api/objidl/nn-objidl-ienumstring">IEnumString</a>**</b>

A pointer to a variable that receives a pointer to the <a href="/windows/desktop/api/objidl/nn-objidl-ienumstring">IEnumString</a> interface for the enumerator that contains query strings that can be used in the current <a href="/windows/desktop/api/wincodec/nn-wincodec-iwicmetadataqueryreader">IWICMetadataQueryReader</a>.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The retrieved enumerator only contains query strings for the metadata blocks and items in the current level of the hierarchy.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/wincodec/nn-wincodec-iwicmetadataqueryreader">IWICMetadataQueryReader</a>



<a href="/windows/desktop/wic/-wic-codec-readingwritingmetadata">Overview of Reading and Writing Image Metadata</a>



<a href="/windows/desktop/wic/-wic-about-metadata">WIC Metadata Overview</a>