---
UID: NF:wincodecsdk.IWICMetadataReader.GetValue
title: IWICMetadataReader::GetValue (wincodecsdk.h)
description: Gets the metadata item value.
helpviewer_keywords: ["GetValue","GetValue method [Windows Imaging Component]","GetValue method [Windows Imaging Component]","IWICMetadataReader interface","IWICMetadataReader interface [Windows Imaging Component]","GetValue method","IWICMetadataReader.GetValue","IWICMetadataReader::GetValue","_wic_codec_iwicmetadatareader_getvalue","wic._wic_codec_iwicmetadatareader_getvalue","wincodecsdk/IWICMetadataReader::GetValue"]
old-location: wic\_wic_codec_iwicmetadatareader_getvalue.htm
tech.root: wic
ms.assetid: 7ae1328d-cda7-4522-9bcf-2c4b16fd6984
ms.date: 12/05/2018
ms.keywords: GetValue, GetValue method [Windows Imaging Component], GetValue method [Windows Imaging Component],IWICMetadataReader interface, IWICMetadataReader interface [Windows Imaging Component],GetValue method, IWICMetadataReader.GetValue, IWICMetadataReader::GetValue, _wic_codec_iwicmetadatareader_getvalue, wic._wic_codec_iwicmetadatareader_getvalue, wincodecsdk/IWICMetadataReader::GetValue
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
 - IWICMetadataReader::GetValue
 - wincodecsdk/IWICMetadataReader::GetValue
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
 - IWICMetadataReader.GetValue
---

# IWICMetadataReader::GetValue


## -description

Gets the metadata item value.

## -parameters

### -param pvarSchema [in]

Type: <b>const <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a>*</b>

Pointer to the metadata item's schema property.

### -param pvarId [in]

Type: <b>const <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a>*</b>

Pointer to the metadata item's id.

### -param pvarValue [in, out]

Type: <b><a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a>*</b>

Pointer that receives the metadata value.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.