---
UID: NF:wincodecsdk.IWICMetadataHandlerInfo.GetDeviceModels
title: IWICMetadataHandlerInfo::GetDeviceModels
author: windows-sdk-content
description: Retrieves the device models that support the metadata handler.
old-location: wic\_wic_codec_iwicmetadatahandlerinfo_getdevicemodels.htm
old-project: wic
ms.assetid: 8ab47616-8097-441f-9d8e-6f1518246759
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: GetDeviceModels, GetDeviceModels method [Windows Imaging Component], GetDeviceModels method [Windows Imaging Component],IWICMetadataHandlerInfo interface, IWICMetadataHandlerInfo interface [Windows Imaging Component],GetDeviceModels method, IWICMetadataHandlerInfo.GetDeviceModels, IWICMetadataHandlerInfo::GetDeviceModels, _wic_codec_iwicmetadatahandlerinfo_getdevicemodels, wic._wic_codec_iwicmetadatahandlerinfo_getdevicemodels, wincodecsdk/IWICMetadataHandlerInfo::GetDeviceModels
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
-	IWICMetadataHandlerInfo.GetDeviceModels
product: Windows
targetos: Windows
req.lib: Windowscodecs.lib
req.dll: Windowscodecs.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# IWICMetadataHandlerInfo::GetDeviceModels


## -description


Retrieves the device models that support the metadata handler.


## -parameters




### -param cchDeviceModels [in]

Type: <b>UINT</b>

The length of the <i>wzDeviceModels</i> buffer.


### -param wzDeviceModels [in, out]

Type: <b>WCHAR*</b>

Pointer that receives the device models supported by the metadata handler.


### -param pcchActual [out]

Type: <b>UINT*</b>

The actual length needed to retrieve the device models.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



