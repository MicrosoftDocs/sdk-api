---
UID: NF:wincodecsdk.WICGetMetadataContentSize
title: WICGetMetadataContentSize function (wincodecsdk.h)
author: windows-sdk-content
description: Returns the size of the metadata content contained by the specified IWICMetadataWriter. The returned size accounts for the header and the length of the metadata.
old-location: wic\_wic_codec_wicgetmetadatacontentsize.htm
tech.root: wic
ms.assetid: 57daa7a5-d0a0-46ae-a009-7f4ee3752088
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: WICGetMetadataContentSize, WICGetMetadataContentSize function [Windows Imaging Component], _wic_codec_wicgetmetadatacontentsize, wic._wic_codec_wicgetmetadatacontentsize, wincodecsdk/WICGetMetadataContentSize
ms.topic: function
f1_keywords: 
 - "wincodecsdk/WICGetMetadataContentSize"
dev_langs:
 - c++
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
req.lib: 
req.dll: Windowscodecs.dll; Wincodec.lib
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Windowscodecs.dll
 - Wincodec.lib
api_name:
 - WICGetMetadataContentSize
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# WICGetMetadataContentSize function


## -description


Returns the size of the metadata content contained by the specified <a href="https://docs.microsoft.com/windows/desktop/api/wincodecsdk/nn-wincodecsdk-iwicmetadatawriter">IWICMetadataWriter</a>. The returned size accounts for the header and the length of the metadata.


## -parameters




### -param guidContainerFormat [in]

Type: <b>REFGUID</b>

The container GUID.


### -param pIWriter [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/wincodecsdk/nn-wincodecsdk-iwicmetadatawriter">IWICMetadataWriter</a>*</b>

The <a href="https://docs.microsoft.com/windows/desktop/api/wincodecsdk/nn-wincodecsdk-iwicmetadatawriter">IWICMetadataWriter</a> that contains the content.


### -param pcbSize [out]

Type: <b>ULARGE_INTEGER*</b>

A pointer that receives the size of the metadata content.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



