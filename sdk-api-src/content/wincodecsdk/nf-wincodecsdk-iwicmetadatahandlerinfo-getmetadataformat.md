---
UID: NF:wincodecsdk.IWICMetadataHandlerInfo.GetMetadataFormat
title: IWICMetadataHandlerInfo::GetMetadataFormat
author: windows-sdk-content
description: Retrieves the metadata format of the metadata handler.
old-location: wic\_wic_codec_iwicmetadatahandlerinfo_getmetadataformat.htm
old-project: wic
ms.assetid: 0a54d59a-3fe4-4636-94a0-5ee449d1d5c3
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: GetMetadataFormat, GetMetadataFormat method [Windows Imaging Component], GetMetadataFormat method [Windows Imaging Component],IWICMetadataHandlerInfo interface, IWICMetadataHandlerInfo interface [Windows Imaging Component],GetMetadataFormat method, IWICMetadataHandlerInfo.GetMetadataFormat, IWICMetadataHandlerInfo::GetMetadataFormat, _wic_codec_iwicmetadatahandlerinfo_getmetadataformat, wic._wic_codec_iwicmetadatahandlerinfo_getmetadataformat, wincodecsdk/IWICMetadataHandlerInfo::GetMetadataFormat
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: wincodecsdk.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wincodecsdk.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: WICPersistOptions
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Windowscodecs.dll
api_name:
 - IWICMetadataHandlerInfo.GetMetadataFormat
product: Windows
targetos: Windows
req.lib: Windowscodecs.lib
req.dll: Windowscodecs.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# IWICMetadataHandlerInfo::GetMetadataFormat


## -description


Retrieves the metadata format of the metadata handler.


## -parameters




### -param pguidMetadataFormat [out]

Type: <b>GUID*</b>

Pointer that receives the metadata format GUID.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



