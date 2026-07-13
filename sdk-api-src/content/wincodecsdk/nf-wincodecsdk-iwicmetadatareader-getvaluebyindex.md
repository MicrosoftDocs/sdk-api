---
UID: NF:wincodecsdk.IWICMetadataReader.GetValueByIndex
title: IWICMetadataReader::GetValueByIndex (wincodecsdk.h)
description: Gets the metadata item at the given index.
helpviewer_keywords: ["GetValueByIndex","GetValueByIndex method [Windows Imaging Component]","GetValueByIndex method [Windows Imaging Component]","IWICMetadataReader interface","IWICMetadataReader interface [Windows Imaging Component]","GetValueByIndex method","IWICMetadataReader.GetValueByIndex","IWICMetadataReader::GetValueByIndex","_wic_codec_iwicmetadatareader_getvaluebyindex","wic._wic_codec_iwicmetadatareader_getvaluebyindex","wincodecsdk/IWICMetadataReader::GetValueByIndex"]
old-location: wic\_wic_codec_iwicmetadatareader_getvaluebyindex.htm
tech.root: wic
ms.assetid: dd22e0e6-d607-48ae-a51c-b49003004f1f
ms.date: 12/05/2018
ms.keywords: GetValueByIndex, GetValueByIndex method [Windows Imaging Component], GetValueByIndex method [Windows Imaging Component],IWICMetadataReader interface, IWICMetadataReader interface [Windows Imaging Component],GetValueByIndex method, IWICMetadataReader.GetValueByIndex, IWICMetadataReader::GetValueByIndex, _wic_codec_iwicmetadatareader_getvaluebyindex, wic._wic_codec_iwicmetadatareader_getvaluebyindex, wincodecsdk/IWICMetadataReader::GetValueByIndex
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
 - IWICMetadataReader::GetValueByIndex
 - wincodecsdk/IWICMetadataReader::GetValueByIndex
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
 - IWICMetadataReader.GetValueByIndex
---

# IWICMetadataReader::GetValueByIndex


## -description

Gets the metadata item at the given index.

## -parameters

### -param nIndex [in]

Type: <b>UINT</b>

The index of the metadata item to retrieve.

### -param pvarSchema [in, out]

Type: <b><a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a>*</b>

Pointer that receives the schema property.

### -param pvarId [in, out]

Type: <b><a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a>*</b>

Pointer that receives the id property.

### -param pvarValue [in, out]

Type: <b><a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a>*</b>

Pointer that receives the metadata value.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.