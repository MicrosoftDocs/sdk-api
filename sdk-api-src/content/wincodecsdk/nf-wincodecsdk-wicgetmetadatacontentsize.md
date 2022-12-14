---
UID: NF:wincodecsdk.WICGetMetadataContentSize
title: WICGetMetadataContentSize function (wincodecsdk.h)
description: Returns the size of the metadata content contained by the specified IWICMetadataWriter. The returned size accounts for the header and the length of the metadata.
helpviewer_keywords: ["WICGetMetadataContentSize","WICGetMetadataContentSize function [Windows Imaging Component]","_wic_codec_wicgetmetadatacontentsize","wic._wic_codec_wicgetmetadatacontentsize","wincodecsdk/WICGetMetadataContentSize"]
old-location: wic\_wic_codec_wicgetmetadatacontentsize.htm
tech.root: wic
ms.assetid: 57daa7a5-d0a0-46ae-a009-7f4ee3752088
ms.date: 12/05/2018
ms.keywords: WICGetMetadataContentSize, WICGetMetadataContentSize function [Windows Imaging Component], _wic_codec_wicgetmetadatacontentsize, wic._wic_codec_wicgetmetadatacontentsize, wincodecsdk/WICGetMetadataContentSize
req.header: wincodecsdk.h
req.include-header: Wincodec.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
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
 - WICGetMetadataContentSize
 - wincodecsdk/WICGetMetadataContentSize
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Windowscodecs.dll
 - Windowscodecs.lib
api_name:
 - WICGetMetadataContentSize
---

# WICGetMetadataContentSize function


## -description

Returns the size of the metadata content contained by the specified <a href="/windows/desktop/api/wincodecsdk/nn-wincodecsdk-iwicmetadatawriter">IWICMetadataWriter</a>. The returned size accounts for the header and the length of the metadata.

## -parameters

### -param guidContainerFormat [in]

Type: <b>REFGUID</b>

The container GUID.

### -param pIWriter [in]

Type: <b><a href="/windows/desktop/api/wincodecsdk/nn-wincodecsdk-iwicmetadatawriter">IWICMetadataWriter</a>*</b>

The <a href="/windows/desktop/api/wincodecsdk/nn-wincodecsdk-iwicmetadatawriter">IWICMetadataWriter</a> that contains the content.

### -param pcbSize [out]

Type: <b>ULARGE_INTEGER*</b>

A pointer that receives the size of the metadata content.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.