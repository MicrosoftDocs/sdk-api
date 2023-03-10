---
UID: NF:wincodecsdk.IWICMetadataReader.GetEnumerator
title: IWICMetadataReader::GetEnumerator (wincodecsdk.h)
description: Gets an enumerator of all the metadata items.
helpviewer_keywords: ["GetEnumerator","GetEnumerator method [Windows Imaging Component]","GetEnumerator method [Windows Imaging Component]","IWICMetadataReader interface","IWICMetadataReader interface [Windows Imaging Component]","GetEnumerator method","IWICMetadataReader.GetEnumerator","IWICMetadataReader::GetEnumerator","_wic_codec_iwicmetadatareader_getenumerator","wic._wic_codec_iwicmetadatareader_getenumerator","wincodecsdk/IWICMetadataReader::GetEnumerator"]
old-location: wic\_wic_codec_iwicmetadatareader_getenumerator.htm
tech.root: wic
ms.assetid: 8dfb2b8d-2825-470e-8adc-85437d8fe863
ms.date: 12/05/2018
ms.keywords: GetEnumerator, GetEnumerator method [Windows Imaging Component], GetEnumerator method [Windows Imaging Component],IWICMetadataReader interface, IWICMetadataReader interface [Windows Imaging Component],GetEnumerator method, IWICMetadataReader.GetEnumerator, IWICMetadataReader::GetEnumerator, _wic_codec_iwicmetadatareader_getenumerator, wic._wic_codec_iwicmetadatareader_getenumerator, wincodecsdk/IWICMetadataReader::GetEnumerator
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
 - IWICMetadataReader::GetEnumerator
 - wincodecsdk/IWICMetadataReader::GetEnumerator
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
 - IWICMetadataReader.GetEnumerator
---

# IWICMetadataReader::GetEnumerator


## -description

Gets an enumerator of all the metadata items.

## -parameters

### -param ppIEnumMetadata [out]

Type: <b><a href="/windows/desktop/api/wincodec/nn-wincodec-iwicenummetadataitem">IWICEnumMetadataItem</a>**</b>

Pointer that receives a pointer to the metadata enumerator.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.