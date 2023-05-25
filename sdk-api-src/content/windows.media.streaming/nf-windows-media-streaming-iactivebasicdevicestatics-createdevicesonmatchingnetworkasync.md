---
UID: NF:windows.media.streaming.IActiveBasicDeviceStatics.CreateDevicesOnMatchingNetworkAsync
title: IActiveBasicDeviceStatics::streaming (windows.media.streaming.h)
description: Asynchronously creates a DevicePair of devices that are on the same network interface.
helpviewer_keywords: ["CreateDevicesOnMatchingNetworkAsync","CreateDevicesOnMatchingNetworkAsync method [Media Streaming API]","CreateDevicesOnMatchingNetworkAsync method [Media Streaming API]","IActiveBasicDeviceStatics interface","IActiveBasicDeviceStatics interface [Media Streaming API]","CreateDevicesOnMatchingNetworkAsync method","IActiveBasicDeviceStatics.CreateDevicesOnMatchingNetworkAsync","IActiveBasicDeviceStatics.streaming","IActiveBasicDeviceStatics::CreateDevicesOnMatchingNetworkAsync","IActiveBasicDeviceStatics::streaming","mediastreaming.iactivebasicdevicestatics_createdevicesonmatchingnetworkasync","windows/IActiveBasicDeviceStatics::CreateDevicesOnMatchingNetworkAsync"]
old-location: mediastreaming\iactivebasicdevicestatics_createdevicesonmatchingnetworkasync.htm
tech.root: mediastreaming
ms.assetid: E113C600-1F55-4653-A4FD-A1286699B137
ms.date: 4/26/2023
ms.keywords: CreateDevicesOnMatchingNetworkAsync, CreateDevicesOnMatchingNetworkAsync method [Media Streaming API], CreateDevicesOnMatchingNetworkAsync method [Media Streaming API],IActiveBasicDeviceStatics interface, IActiveBasicDeviceStatics interface [Media Streaming API],CreateDevicesOnMatchingNetworkAsync method, IActiveBasicDeviceStatics.CreateDevicesOnMatchingNetworkAsync, IActiveBasicDeviceStatics.streaming, IActiveBasicDeviceStatics::CreateDevicesOnMatchingNetworkAsync, IActiveBasicDeviceStatics::streaming, mediastreaming.iactivebasicdevicestatics_createdevicesonmatchingnetworkasync, windows/IActiveBasicDeviceStatics::CreateDevicesOnMatchingNetworkAsync
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
 - IActiveBasicDeviceStatics::CreateDevicesOnMatchingNetworkAsync
 - windows.media.streaming/IActiveBasicDeviceStatics::CreateDevicesOnMatchingNetworkAsync
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
 - IActiveBasicDeviceStatics.CreateDevicesOnMatchingNetworkAsync
---

# IActiveBasicDeviceStatics::streaming


## -description

\[The feature associated with this page, [Windows Media Streaming API](/windows/win32/mediastreaming/media-streaming-api-portal), is a legacy feature. It has been superseded by [Media Casting](/windows/uwp/audio-video-camera/media-casting). **Media Casting** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Media Casting** instead of **Windows Media Streaming API**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

Asynchronously creates a <a href="/previous-versions/windows/desktop/legacy/dn385771(v=vs.85)">DevicePair</a> of devices that are on the same network interface.

## -parameters

### -param serverUDN [in]

The basic device server.

### -param renderer [in]

The basic device renderer.

### -param optimizeForProxying [in]

Specifies whether or not to optimize for proxying.

### -param allowChangeRendererNetwork [in]

Specifies whether or not the renderer network can be changed.

### -param operation [out, retval]

The asynchronous operation. Upon completion, <a href="/previous-versions/br205815(v=vs.85)">IAsyncOperation.GetResults</a> returns a <a href="/previous-versions/windows/desktop/legacy/dn385771(v=vs.85)">DevicePair</a> object.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-iactivebasicdevicestatics">IActiveBasicDeviceStatics</a>