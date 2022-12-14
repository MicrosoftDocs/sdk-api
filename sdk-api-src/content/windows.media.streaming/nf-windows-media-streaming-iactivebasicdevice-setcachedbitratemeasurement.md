---
UID: NF:windows.media.streaming.IActiveBasicDevice.SetCachedBitrateMeasurement
title: IActiveBasicDevice::streaming (windows.media.streaming.h)
description: Sets the cached bitrate.
helpviewer_keywords: ["IActiveBasicDevice interface [Media Streaming API]","SetCachedBitrateMeasurement method","IActiveBasicDevice.SetCachedBitrateMeasurement","IActiveBasicDevice.streaming","IActiveBasicDevice::SetCachedBitrateMeasurement","IActiveBasicDevice::streaming","SetCachedBitrateMeasurement","SetCachedBitrateMeasurement method [Media Streaming API]","SetCachedBitrateMeasurement method [Media Streaming API]","IActiveBasicDevice interface","mediastreaming.iactivebasicdevice_setcachedbitratemeasurement","windows/IActiveBasicDevice::SetCachedBitrateMeasurement"]
old-location: mediastreaming\iactivebasicdevice_setcachedbitratemeasurement.htm
tech.root: mediastreaming
ms.assetid: B695D51C-205B-4D45-BEA7-0235FC770C77
ms.date: 12/05/2018
ms.keywords: IActiveBasicDevice interface [Media Streaming API],SetCachedBitrateMeasurement method, IActiveBasicDevice.SetCachedBitrateMeasurement, IActiveBasicDevice.streaming, IActiveBasicDevice::SetCachedBitrateMeasurement, IActiveBasicDevice::streaming, SetCachedBitrateMeasurement, SetCachedBitrateMeasurement method [Media Streaming API], SetCachedBitrateMeasurement method [Media Streaming API],IActiveBasicDevice interface, mediastreaming.iactivebasicdevice_setcachedbitratemeasurement, windows/IActiveBasicDevice::SetCachedBitrateMeasurement
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
 - IActiveBasicDevice::SetCachedBitrateMeasurement
 - windows.media.streaming/IActiveBasicDevice::SetCachedBitrateMeasurement
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
 - IActiveBasicDevice.SetCachedBitrateMeasurement
---

# IActiveBasicDevice::streaming


## -description

Sets the cached bitrate.

## -parameters

### -param physicalNetworkInterface [in]

Specifies the physical network interface.

### -param bitrate [in]

The value to set the bitrate to.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-iactivebasicdevice">IActiveBasicDevice</a>



<a href="/windows/desktop/mediastreaming/ibasicdevice">IBasicDevice</a>