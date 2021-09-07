---
UID: NF:wincodecsdk.IWICMetadataWriter.SetValueByIndex
title: IWICMetadataWriter::SetValueByIndex (wincodecsdk.h)
description: Sets the metadata item to the specified index.
helpviewer_keywords: ["IWICMetadataWriter interface [Windows Imaging Component]","SetValueByIndex method","IWICMetadataWriter.SetValueByIndex","IWICMetadataWriter::SetValueByIndex","SetValueByIndex","SetValueByIndex method [Windows Imaging Component]","SetValueByIndex method [Windows Imaging Component]","IWICMetadataWriter interface","_wic_codec_iwicmetadatawriter_setvaluebyindex","wic._wic_codec_iwicmetadatawriter_setvaluebyindex","wincodecsdk/IWICMetadataWriter::SetValueByIndex"]
old-location: wic\_wic_codec_iwicmetadatawriter_setvaluebyindex.htm
tech.root: wic
ms.assetid: 012ef661-c1cf-48fd-a748-223fa965f9a9
ms.date: 12/05/2018
ms.keywords: IWICMetadataWriter interface [Windows Imaging Component],SetValueByIndex method, IWICMetadataWriter.SetValueByIndex, IWICMetadataWriter::SetValueByIndex, SetValueByIndex, SetValueByIndex method [Windows Imaging Component], SetValueByIndex method [Windows Imaging Component],IWICMetadataWriter interface, _wic_codec_iwicmetadatawriter_setvaluebyindex, wic._wic_codec_iwicmetadatawriter_setvaluebyindex, wincodecsdk/IWICMetadataWriter::SetValueByIndex
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
 - IWICMetadataWriter::SetValueByIndex
 - wincodecsdk/IWICMetadataWriter::SetValueByIndex
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
 - IWICMetadataWriter.SetValueByIndex
---

# IWICMetadataWriter::SetValueByIndex


## -description

Sets the metadata item to the specified index.

## -parameters

### -param nIndex [in]

Type: <b>UINT</b>

The index to place the metadata item.

### -param pvarSchema [in]

Type: <b>const <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a>*</b>

Pointer to the schema property of the metadata item.

### -param pvarId [in]

Type: <b>const <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a>*</b>

Pointer to the id property of the metadata item.

### -param pvarValue [in]

Type: <b>const <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a>*</b>

Pointer to the metadata value to set at the given index.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

After removing an item, expect the remaining metadata items to move up to occupy the vacated metadata item location.  Therefore indices for remaining metadata items as well as the count will change.