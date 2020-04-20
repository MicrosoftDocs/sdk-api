---
UID: NF:wincodecsdk.IWICMetadataReader.GetEnumerator
title: IWICMetadataReader::GetEnumerator (wincodecsdk.h)
description: Gets an enumerator of all the metadata items.helpviewer_keywords: ["GetEnumerator","GetEnumerator method [Windows Imaging Component]","GetEnumerator method [Windows Imaging Component]","IWICMetadataReader interface","IWICMetadataReader interface [Windows Imaging Component]","GetEnumerator method","IWICMetadataReader.GetEnumerator","IWICMetadataReader::GetEnumerator","_wic_codec_iwicmetadatareader_getenumerator","wic._wic_codec_iwicmetadatareader_getenumerator","wincodecsdk/IWICMetadataReader::GetEnumerator"]
old-location: wic\_wic_codec_iwicmetadatareader_getenumerator.htm
tech.root: wic
ms.assetid: 8dfb2b8d-2825-470e-8adc-85437d8fe863
ms.date: 12/05/2018
ms.keywords: GetEnumerator, GetEnumerator method [Windows Imaging Component], GetEnumerator method [Windows Imaging Component],IWICMetadataReader interface, IWICMetadataReader interface [Windows Imaging Component],GetEnumerator method, IWICMetadataReader.GetEnumerator, IWICMetadataReader::GetEnumerator, _wic_codec_iwicmetadatareader_getenumerator, wic._wic_codec_iwicmetadatareader_getenumerator, wincodecsdk/IWICMetadataReader::GetEnumerator
f1_keywords:
- wincodecsdk/IWICMetadataReader.GetEnumerator
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
- IWICMetadataReader.GetEnumerator
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWICMetadataReader::GetEnumerator


## -description


Gets an enumerator of all the metadata items.


## -parameters




### -param ppIEnumMetadata [out]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/wincodec/nn-wincodec-iwicenummetadataitem">IWICEnumMetadataItem</a>**</b>

Pointer that receives a pointer to the metadata enumerator.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



