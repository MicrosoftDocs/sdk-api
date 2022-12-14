---
UID: NF:windows.media.streaming.IActiveBasicDeviceStatics.GetDevicesOnMatchingNetworkAsync
title: IActiveBasicDeviceStatics::streaming (windows.media.streaming.h)
description: Asynchronously gets a DevicePair of devices that are on the same network interface.
helpviewer_keywords: ["GetDevicesOnMatchingNetworkAsync","GetDevicesOnMatchingNetworkAsync method [Media Streaming API]","GetDevicesOnMatchingNetworkAsync method [Media Streaming API]","IActiveBasicDeviceStatics interface","IActiveBasicDeviceStatics interface [Media Streaming API]","GetDevicesOnMatchingNetworkAsync method","IActiveBasicDeviceStatics.GetDevicesOnMatchingNetworkAsync","IActiveBasicDeviceStatics.streaming","IActiveBasicDeviceStatics::GetDevicesOnMatchingNetworkAsync","IActiveBasicDeviceStatics::streaming","mediastreaming.iactivebasicdevicestatics_getdevicesonmatchingnetworkasync","windows/IActiveBasicDeviceStatics::GetDevicesOnMatchingNetworkAsync"]
old-location: mediastreaming\iactivebasicdevicestatics_getdevicesonmatchingnetworkasync.htm
tech.root: mediastreaming
ms.assetid: 9BE3BBD1-F3D3-4EAF-9125-B82AE0DE48AA
ms.date: 12/05/2018
ms.keywords: GetDevicesOnMatchingNetworkAsync, GetDevicesOnMatchingNetworkAsync method [Media Streaming API], GetDevicesOnMatchingNetworkAsync method [Media Streaming API],IActiveBasicDeviceStatics interface, IActiveBasicDeviceStatics interface [Media Streaming API],GetDevicesOnMatchingNetworkAsync method, IActiveBasicDeviceStatics.GetDevicesOnMatchingNetworkAsync, IActiveBasicDeviceStatics.streaming, IActiveBasicDeviceStatics::GetDevicesOnMatchingNetworkAsync, IActiveBasicDeviceStatics::streaming, mediastreaming.iactivebasicdevicestatics_getdevicesonmatchingnetworkasync, windows/IActiveBasicDeviceStatics::GetDevicesOnMatchingNetworkAsync
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
 - IActiveBasicDeviceStatics::GetDevicesOnMatchingNetworkAsync
 - windows.media.streaming/IActiveBasicDeviceStatics::GetDevicesOnMatchingNetworkAsync
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
 - IActiveBasicDeviceStatics.GetDevicesOnMatchingNetworkAsync
---

# IActiveBasicDeviceStatics::streaming


## -description

Asynchronously gets a <a href="/previous-versions/windows/desktop/legacy/dn385771(v=vs.85)">DevicePair</a> of devices that are on the same network interface.

## -parameters

### -param server

The UDN (unique device name) of the server.

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