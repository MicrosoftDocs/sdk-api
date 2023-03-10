---
UID: NF:windows.media.streaming.IActiveBasicDevice.GetEffectiveBandwidth
title: IActiveBasicDevice::streaming (windows.media.streaming.h)
description: Gets the current effective bandwidth for the device.
helpviewer_keywords: ["GetEffectiveBandwidth","GetEffectiveBandwidth method [Media Streaming API]","GetEffectiveBandwidth method [Media Streaming API]","IActiveBasicDevice interface","IActiveBasicDevice interface [Media Streaming API]","GetEffectiveBandwidth method","IActiveBasicDevice.GetEffectiveBandwidth","IActiveBasicDevice.streaming","IActiveBasicDevice::GetEffectiveBandwidth","IActiveBasicDevice::streaming","mediastreaming.iactivebasicdevice_geteffectivebandwidth","windows/IActiveBasicDevice::GetEffectiveBandwidth"]
old-location: mediastreaming\iactivebasicdevice_geteffectivebandwidth.htm
tech.root: mediastreaming
ms.assetid: 894EC907-E578-4F1E-A0AB-1FDE2FA67B6C
ms.date: 12/05/2018
ms.keywords: GetEffectiveBandwidth, GetEffectiveBandwidth method [Media Streaming API], GetEffectiveBandwidth method [Media Streaming API],IActiveBasicDevice interface, IActiveBasicDevice interface [Media Streaming API],GetEffectiveBandwidth method, IActiveBasicDevice.GetEffectiveBandwidth, IActiveBasicDevice.streaming, IActiveBasicDevice::GetEffectiveBandwidth, IActiveBasicDevice::streaming, mediastreaming.iactivebasicdevice_geteffectivebandwidth, windows/IActiveBasicDevice::GetEffectiveBandwidth
req.header: windows.media.streaming.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Windows.Media.Streaming.Devices.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: PlayToDevice.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IActiveBasicDevice::GetEffectiveBandwidth
 - windows.media.streaming/IActiveBasicDevice::GetEffectiveBandwidth
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - PlayToDevice.dll
api_name:
 - IActiveBasicDevice.GetEffectiveBandwidth
---

# IActiveBasicDevice::streaming


## -description

Gets the current effective bandwidth for the device.

## -parameters

### -param transmitSpeed [in, retval]

Specifies whether the transmit speed is retrieved or the receive speed is retrieved. 

<b>true</b> to retrieve the transmit speed. <b>false</b> to retrieve the receive speed.

### -param currentSpeed [out]

Receives the current effective bandwidth.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-iactivebasicdevice">IActiveBasicDevice</a>



<a href="/windows/desktop/mediastreaming/ibasicdevice">IBasicDevice</a>