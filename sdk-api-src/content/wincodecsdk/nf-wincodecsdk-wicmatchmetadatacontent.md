---
UID: NF:wincodecsdk.WICMatchMetadataContent
title: WICMatchMetadataContent function
author: windows-sdk-content
description: Obtains a metadata format GUID for a specified container format and vendor that best matches the content within a given stream.
old-location: wic\_wic_codec_wicmatchmetadatacontent.htm
tech.root: wic
ms.assetid: 2d1ab317-a77c-4e91-9455-e6738fd40e88
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: WICMatchMetadataContent, WICMatchMetadataContent function [Windows Imaging Component], _wic_codec_wicmatchmetadatacontent, wic._wic_codec_wicmatchmetadatacontent, wincodecsdk/WICMatchMetadataContent
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
 - WICMatchMetadataContent
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- WICMatchMetadataContent
: 
---

# WICMatchMetadataContent function


## -description


Obtains a metadata format GUID for a specified container format and vendor that best matches the content within a given stream.


## -parameters




### -param guidContainerFormat [in]

Type: <b>REFGUID</b>

The container format GUID. 


### -param pguidVendor [in]

Type: <b>const GUID*</b>

The vendor GUID.


### -param pIStream [in]

Type: <b><a href="https://msdn.microsoft.com/c6f60e37-eadc-46a1-94f6-cacc23613531">IStream</a>*</b>

The content stream in which to match a metadata format.


### -param pguidMetadataFormat [out]

Type: <b>GUID*</b>

A pointer that receives a metadata format GUID for the given parameters.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



