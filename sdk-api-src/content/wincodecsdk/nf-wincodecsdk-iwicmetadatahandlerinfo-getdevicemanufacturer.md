---
UID: NF:wincodecsdk.IWICMetadataHandlerInfo.GetDeviceManufacturer
title: IWICMetadataHandlerInfo::GetDeviceManufacturer
author: windows-sdk-content
description: Retrieves the device manufacturer of the metadata handler.
old-location: wic\_wic_codec_iwicmetadatahandlerinfo_getdevicemanufacturer.htm
old-project: wic
ms.assetid: ab3cd583-055d-4414-a615-600e4c67dcc4
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: GetDeviceManufacturer, GetDeviceManufacturer method [Windows Imaging Component], GetDeviceManufacturer method [Windows Imaging Component],IWICMetadataHandlerInfo interface, IWICMetadataHandlerInfo interface [Windows Imaging Component],GetDeviceManufacturer method, IWICMetadataHandlerInfo.GetDeviceManufacturer, IWICMetadataHandlerInfo::GetDeviceManufacturer, _wic_codec_iwicmetadatahandlerinfo_getdevicemanufacturer, wic._wic_codec_iwicmetadatahandlerinfo_getdevicemanufacturer, wincodecsdk/IWICMetadataHandlerInfo::GetDeviceManufacturer
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
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Windowscodecs.dll
api_name:
-	IWICMetadataHandlerInfo.GetDeviceManufacturer
product: Windows
targetos: Windows
req.lib: Windowscodecs.lib
req.dll: Windowscodecs.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# IWICMetadataHandlerInfo::GetDeviceManufacturer


## -description


Retrieves the device manufacturer of the metadata handler.


## -parameters




### -param cchDeviceManufacturer [in]

Type: <b>UINT</b>

The size of the <i>wzDeviceManufacturer</i> buffer.


### -param wzDeviceManufacturer [in, out]

Type: <b>WCHAR*</b>

Pointer to the buffer that receives the name of the device manufacturer.


### -param pcchActual [out]

Type: <b>UINT*</b>

The actual string buffer length needed to obtain the entire name of the device manufacturer.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



