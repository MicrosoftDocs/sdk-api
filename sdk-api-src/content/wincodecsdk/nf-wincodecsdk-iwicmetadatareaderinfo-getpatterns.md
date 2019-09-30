---
UID: NF:wincodecsdk.IWICMetadataReaderInfo.GetPatterns
title: IWICMetadataReaderInfo::GetPatterns (wincodecsdk.h)
author: windows-sdk-content
description: Gets the metadata patterns associated with the metadata reader.
old-location: wic\_wic_codec_iwicmetadatareaderinfo_getpatterns.htm
tech.root: wic
ms.assetid: bc0033f7-801d-4ae0-a2cb-bdda25303476
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetPatterns, GetPatterns method [Windows Imaging Component], GetPatterns method [Windows Imaging Component],IWICMetadataReaderInfo interface, IWICMetadataReaderInfo interface [Windows Imaging Component],GetPatterns method, IWICMetadataReaderInfo.GetPatterns, IWICMetadataReaderInfo::GetPatterns, _wic_codec_iwicmetadatareaderinfo_getpatterns, wic._wic_codec_iwicmetadatareaderinfo_getpatterns, wincodecsdk/IWICMetadataReaderInfo::GetPatterns
ms.topic: method
f1_keywords: 
 - "wincodecsdk/IWICMetadataReaderInfo.GetPatterns"
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
 - IWICMetadataReaderInfo.GetPatterns
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWICMetadataReaderInfo::GetPatterns


## -description


Gets the metadata patterns associated with the metadata reader.


## -parameters




### -param guidContainerFormat [in]

Type: <b>REFGUID</b>

The cointainer format GUID.


### -param cbSize [in]

Type: <b>UINT</b>

The size, in bytes, of the <i>pPattern</i> buffer.


### -param pPattern [in, out]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/wincodecsdk/ns-wincodecsdk-wicmetadatapattern">WICMetadataPattern</a>*</b>

Pointer that receives the metadata patterns.


### -param pcCount [in, out]

Type: <b>UINT*</b>

Pointer that receives the number of metadata patterns.


### -param pcbActual [in, out]

Type: <b>UINT*</b>

Pointer that receives the size, in bytes, needed to obtain the metadata patterns.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



