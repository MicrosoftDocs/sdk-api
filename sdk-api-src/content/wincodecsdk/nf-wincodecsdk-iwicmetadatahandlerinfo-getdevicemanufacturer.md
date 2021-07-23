---
UID: NF:wincodecsdk.IWICMetadataHandlerInfo.GetDeviceManufacturer
title: IWICMetadataHandlerInfo::GetDeviceManufacturer (wincodecsdk.h)
description: Retrieves the device manufacturer of the metadata handler.
helpviewer_keywords: ["GetDeviceManufacturer","GetDeviceManufacturer method [Windows Imaging Component]","GetDeviceManufacturer method [Windows Imaging Component]","IWICMetadataHandlerInfo interface","IWICMetadataHandlerInfo interface [Windows Imaging Component]","GetDeviceManufacturer method","IWICMetadataHandlerInfo.GetDeviceManufacturer","IWICMetadataHandlerInfo::GetDeviceManufacturer","_wic_codec_iwicmetadatahandlerinfo_getdevicemanufacturer","wic._wic_codec_iwicmetadatahandlerinfo_getdevicemanufacturer","wincodecsdk/IWICMetadataHandlerInfo::GetDeviceManufacturer"]
old-location: wic\_wic_codec_iwicmetadatahandlerinfo_getdevicemanufacturer.htm
tech.root: wic
ms.assetid: ab3cd583-055d-4414-a615-600e4c67dcc4
ms.date: 12/05/2018
ms.keywords: GetDeviceManufacturer, GetDeviceManufacturer method [Windows Imaging Component], GetDeviceManufacturer method [Windows Imaging Component],IWICMetadataHandlerInfo interface, IWICMetadataHandlerInfo interface [Windows Imaging Component],GetDeviceManufacturer method, IWICMetadataHandlerInfo.GetDeviceManufacturer, IWICMetadataHandlerInfo::GetDeviceManufacturer, _wic_codec_iwicmetadatahandlerinfo_getdevicemanufacturer, wic._wic_codec_iwicmetadatahandlerinfo_getdevicemanufacturer, wincodecsdk/IWICMetadataHandlerInfo::GetDeviceManufacturer
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
 - IWICMetadataHandlerInfo::GetDeviceManufacturer
 - wincodecsdk/IWICMetadataHandlerInfo::GetDeviceManufacturer
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
 - IWICMetadataHandlerInfo.GetDeviceManufacturer
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

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

