---
UID: NF:wincodecsdk.IWICMetadataReader.GetMetadataHandlerInfo
title: IWICMetadataReader::GetMetadataHandlerInfo (wincodecsdk.h)
author: windows-sdk-content
description: Gets the metadata handler info associated with the reader.
old-location: wic\_wic_codec_iwicmetadatareader_getmetadatahandlerinfo.htm
tech.root: wic
ms.assetid: f3843044-4963-4e9f-8b5d-69d0201c9ec9
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetMetadataHandlerInfo, GetMetadataHandlerInfo method [Windows Imaging Component], GetMetadataHandlerInfo method [Windows Imaging Component],IWICMetadataReader interface, IWICMetadataReader interface [Windows Imaging Component],GetMetadataHandlerInfo method, IWICMetadataReader.GetMetadataHandlerInfo, IWICMetadataReader::GetMetadataHandlerInfo, _wic_codec_iwicmetadatareader_getmetadatahandlerinfo, wic._wic_codec_iwicmetadatareader_getmetadatahandlerinfo, wincodecsdk/IWICMetadataReader::GetMetadataHandlerInfo
ms.topic: method
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
 - IWICMetadataReader.GetMetadataHandlerInfo
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWICMetadataReader::GetMetadataHandlerInfo


## -description


Gets the metadata handler info associated with the reader.


## -parameters




### -param ppIHandler [out]

Type: <b><a href="https://msdn.microsoft.com/505105c2-de50-4b5f-9089-e9a3cea2f464">IWICMetadataHandlerInfo</a>**</b>

Pointer that receives a pointer to the <a href="https://msdn.microsoft.com/505105c2-de50-4b5f-9089-e9a3cea2f464">IWICMetadataHandlerInfo</a>.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



