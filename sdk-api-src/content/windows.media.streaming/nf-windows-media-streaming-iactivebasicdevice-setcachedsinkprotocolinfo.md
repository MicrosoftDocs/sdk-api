---
UID: NF:windows.media.streaming.IActiveBasicDevice.SetCachedSinkProtocolInfo
title: IActiveBasicDevice::streaming (windows.media.streaming.h)
description: Gets the cached sink protocol info for the device.
helpviewer_keywords: ["IActiveBasicDevice interface [Media Streaming API]","SetCachedSinkProtocolInfo method","IActiveBasicDevice.SetCachedSinkProtocolInfo","IActiveBasicDevice.streaming","IActiveBasicDevice::SetCachedSinkProtocolInfo","IActiveBasicDevice::streaming","SetCachedSinkProtocolInfo","SetCachedSinkProtocolInfo method [Media Streaming API]","SetCachedSinkProtocolInfo method [Media Streaming API]","IActiveBasicDevice interface","mediastreaming.iactivebasicdevice_setcachedsinkprotocolinfo","windows/IActiveBasicDevice::SetCachedSinkProtocolInfo"]
old-location: mediastreaming\iactivebasicdevice_setcachedsinkprotocolinfo.htm
tech.root: mediastreaming
ms.assetid: 210AEE22-0AFD-43B1-8380-8A67D17AB7CB
ms.date: 4/26/2023
ms.keywords: IActiveBasicDevice interface [Media Streaming API],SetCachedSinkProtocolInfo method, IActiveBasicDevice.SetCachedSinkProtocolInfo, IActiveBasicDevice.streaming, IActiveBasicDevice::SetCachedSinkProtocolInfo, IActiveBasicDevice::streaming, SetCachedSinkProtocolInfo, SetCachedSinkProtocolInfo method [Media Streaming API], SetCachedSinkProtocolInfo method [Media Streaming API],IActiveBasicDevice interface, mediastreaming.iactivebasicdevice_setcachedsinkprotocolinfo, windows/IActiveBasicDevice::SetCachedSinkProtocolInfo
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
 - IActiveBasicDevice::SetCachedSinkProtocolInfo
 - windows.media.streaming/IActiveBasicDevice::SetCachedSinkProtocolInfo
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
 - IActiveBasicDevice.SetCachedSinkProtocolInfo
---

# IActiveBasicDevice::streaming


## -description

\[The feature associated with this page, [Windows Media Streaming API](/windows/win32/mediastreaming/media-streaming-api-portal), is a legacy feature. It has been superseded by [Media Casting](/windows/uwp/audio-video-camera/media-casting). **Media Casting** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Media Casting** instead of **Windows Media Streaming API**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

Sets the cached sink protocol info for the device.

## -parameters

### -param value

The cached sink protocol info for the device.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-iactivebasicdevice">IActiveBasicDevice</a>



<a href="/windows/desktop/mediastreaming/ibasicdevice">IBasicDevice</a>