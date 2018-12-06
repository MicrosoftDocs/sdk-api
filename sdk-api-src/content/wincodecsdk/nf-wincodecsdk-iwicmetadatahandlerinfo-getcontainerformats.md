---
UID: NF:wincodecsdk.IWICMetadataHandlerInfo.GetContainerFormats
title: IWICMetadataHandlerInfo::GetContainerFormats
author: windows-sdk-content
description: Retrieves the container formats supported by the metadata handler.
old-location: wic\_wic_codec_iwicmetadatahandlerinfo_getcontainerformats.htm
tech.root: wic
ms.assetid: 46d5246d-4ef5-457c-b36b-68e0f956952b
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetContainerFormats, GetContainerFormats method [Windows Imaging Component], GetContainerFormats method [Windows Imaging Component],IWICMetadataHandlerInfo interface, IWICMetadataHandlerInfo interface [Windows Imaging Component],GetContainerFormats method, IWICMetadataHandlerInfo.GetContainerFormats, IWICMetadataHandlerInfo::GetContainerFormats, _wic_codec_iwicmetadatahandlerinfo_getcontainerformats, wic._wic_codec_iwicmetadatahandlerinfo_getcontainerformats, wincodecsdk/IWICMetadataHandlerInfo::GetContainerFormats
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IWICMetadataHandlerInfo.GetContainerFormats
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWICMetadataHandlerInfo::GetContainerFormats


## -description


Retrieves the container formats supported by the metadata handler.


## -parameters




### -param cContainerFormats [in]

Type: <b>UINT</b>

The size of the <i>pguidContainerFormats</i> array.


### -param pguidContainerFormats [in, out]

Type: <b>GUID*</b>

Pointer to an array that receives the container formats supported by the metadata handler.


### -param pcchActual [out]

Type: <b>UINT*</b>

The actual number of GUIDs added to the array.
               

To obtain the number of supported container formats, pass <code>NULL</code> to <i>pguidContainerFormats</i>.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



