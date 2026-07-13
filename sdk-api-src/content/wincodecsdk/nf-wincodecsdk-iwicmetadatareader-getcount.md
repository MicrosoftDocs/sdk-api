---
UID: NF:wincodecsdk.IWICMetadataReader.GetCount
title: IWICMetadataReader::GetCount (wincodecsdk.h)
description: Gets the number of metadata items within the reader.
helpviewer_keywords: ["GetCount","GetCount method [Windows Imaging Component]","GetCount method [Windows Imaging Component]","IWICMetadataReader interface","IWICMetadataReader interface [Windows Imaging Component]","GetCount method","IWICMetadataReader.GetCount","IWICMetadataReader::GetCount","_wic_codec_iwicmetadatareader_getcount","wic._wic_codec_iwicmetadatareader_getcount","wincodecsdk/IWICMetadataReader::GetCount"]
old-location: wic\_wic_codec_iwicmetadatareader_getcount.htm
tech.root: wic
ms.assetid: ce9b0267-112a-4aa9-8786-272ee4da4d8b
ms.date: 12/05/2018
ms.keywords: GetCount, GetCount method [Windows Imaging Component], GetCount method [Windows Imaging Component],IWICMetadataReader interface, IWICMetadataReader interface [Windows Imaging Component],GetCount method, IWICMetadataReader.GetCount, IWICMetadataReader::GetCount, _wic_codec_iwicmetadatareader_getcount, wic._wic_codec_iwicmetadatareader_getcount, wincodecsdk/IWICMetadataReader::GetCount
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
 - IWICMetadataReader::GetCount
 - wincodecsdk/IWICMetadataReader::GetCount
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
 - IWICMetadataReader.GetCount
---

# IWICMetadataReader::GetCount


## -description

Gets the number of metadata items within the reader.

## -parameters

### -param pcCount [out]

Type: <b>UINT*</b>

Pointer that receives the number of metadata items within the reader.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

