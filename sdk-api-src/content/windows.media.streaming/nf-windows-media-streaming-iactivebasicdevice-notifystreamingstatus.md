---
UID: NF:windows.media.streaming.IActiveBasicDevice.NotifyStreamingStatus
title: IActiveBasicDevice::streaming (windows.media.streaming.h)
description: Called by the application to indicate that the device is being used for active streaming.
helpviewer_keywords: ["IActiveBasicDevice interface [Media Streaming API]","NotifyStreamingStatus method","IActiveBasicDevice.NotifyStreamingStatus","IActiveBasicDevice.streaming","IActiveBasicDevice::NotifyStreamingStatus","IActiveBasicDevice::streaming","NotifyStreamingStatus","NotifyStreamingStatus method [Media Streaming API]","NotifyStreamingStatus method [Media Streaming API]","IActiveBasicDevice interface","mediastreaming.iactivebasicdevice_notifystreamingstatus","windows/IActiveBasicDevice::NotifyStreamingStatus"]
old-location: mediastreaming\iactivebasicdevice_notifystreamingstatus.htm
tech.root: mediastreaming
ms.assetid: D62E8571-1DE9-4BAB-A291-415FD6E9F9C8
ms.date: 4/26/2023
ms.keywords: IActiveBasicDevice interface [Media Streaming API],NotifyStreamingStatus method, IActiveBasicDevice.NotifyStreamingStatus, IActiveBasicDevice.streaming, IActiveBasicDevice::NotifyStreamingStatus, IActiveBasicDevice::streaming, NotifyStreamingStatus, NotifyStreamingStatus method [Media Streaming API], NotifyStreamingStatus method [Media Streaming API],IActiveBasicDevice interface, mediastreaming.iactivebasicdevice_notifystreamingstatus, windows/IActiveBasicDevice::NotifyStreamingStatus
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
 - IActiveBasicDevice::NotifyStreamingStatus
 - windows.media.streaming/IActiveBasicDevice::NotifyStreamingStatus
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
 - IActiveBasicDevice.NotifyStreamingStatus
---

# IActiveBasicDevice::streaming


## -description

\[The feature associated with this page, [Windows Media Streaming API](/windows/win32/mediastreaming/media-streaming-api-portal), is a legacy feature. It has been superseded by [Media Casting](/windows/uwp/audio-video-camera/media-casting). **Media Casting** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Media Casting** instead of **Windows Media Streaming API**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

Called by the application to indicate  that  the device is being used for active streaming.

## -parameters

### -param fIsStreaming

<b>true</b> indicates that streaming is on.  <b>false</b> indicates that streaming if off.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This method is  called by the application to indicate that the device is being used for active streaming. A value of <b>true</b> means that streaming is on. A value of <b>false</b> means that streaming is off.  

The on/off calls must be matching calls from the application.

In response to this notification, the <a href="/previous-versions/windows/desktop/legacy/dn385755(v=vs.85)">ActiveBasicDevice</a> object can take actions to keep the connection to the device active.

## -see-also

<a href="/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-iactivebasicdevice">IActiveBasicDevice</a>