---
UID: NF:windows.media.streaming.IActiveBasicDevice.GetCachedBitrateMeasurement
title: IActiveBasicDevice::streaming (windows.media.streaming.h)
description: Gets the cached bitrate.
helpviewer_keywords: ["GetCachedBitrateMeasurement","GetCachedBitrateMeasurement method [Media Streaming API]","GetCachedBitrateMeasurement method [Media Streaming API]","IActiveBasicDevice interface","IActiveBasicDevice interface [Media Streaming API]","GetCachedBitrateMeasurement method","IActiveBasicDevice.GetCachedBitrateMeasurement","IActiveBasicDevice.streaming","IActiveBasicDevice::GetCachedBitrateMeasurement","IActiveBasicDevice::streaming","mediastreaming.iactivebasicdevice_getcachedbitratemeasurement","windows/IActiveBasicDevice::GetCachedBitrateMeasurement"]
old-location: mediastreaming\iactivebasicdevice_getcachedbitratemeasurement.htm
tech.root: mediastreaming
ms.assetid: 342F5240-E29D-4CC4-AA49-B039EBFC4D0B
ms.date: 12/05/2018
ms.keywords: GetCachedBitrateMeasurement, GetCachedBitrateMeasurement method [Media Streaming API], GetCachedBitrateMeasurement method [Media Streaming API],IActiveBasicDevice interface, IActiveBasicDevice interface [Media Streaming API],GetCachedBitrateMeasurement method, IActiveBasicDevice.GetCachedBitrateMeasurement, IActiveBasicDevice.streaming, IActiveBasicDevice::GetCachedBitrateMeasurement, IActiveBasicDevice::streaming, mediastreaming.iactivebasicdevice_getcachedbitratemeasurement, windows/IActiveBasicDevice::GetCachedBitrateMeasurement
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
 - IActiveBasicDevice::GetCachedBitrateMeasurement
 - windows.media.streaming/IActiveBasicDevice::GetCachedBitrateMeasurement
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
 - IActiveBasicDevice.GetCachedBitrateMeasurement
---

# IActiveBasicDevice::streaming


## -description

Gets the cached bitrate.

## -parameters

### -param physicalNetworkInterface [in]

Specifies the physical network interface.

### -param bitrate [out, retval]

Receives the bitrate value.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-iactivebasicdevice">IActiveBasicDevice</a>



<a href="/windows/desktop/mediastreaming/ibasicdevice">IBasicDevice</a>