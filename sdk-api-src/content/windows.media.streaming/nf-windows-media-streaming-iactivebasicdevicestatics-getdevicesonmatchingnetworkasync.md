---
UID: NF:windows.media.streaming.IActiveBasicDeviceStatics.GetDevicesOnMatchingNetworkAsync
title: IActiveBasicDeviceStatics::streaming (windows.media.streaming.h)
author: windows-sdk-content
description: Asynchronously gets a DevicePair of devices that are on the same network interface.
old-location: mediastreaming\iactivebasicdevicestatics_getdevicesonmatchingnetworkasync.htm
tech.root: mediastreaming
ms.assetid: 9BE3BBD1-F3D3-4EAF-9125-B82AE0DE48AA
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetDevicesOnMatchingNetworkAsync, GetDevicesOnMatchingNetworkAsync method [Media Streaming API], GetDevicesOnMatchingNetworkAsync method [Media Streaming API],IActiveBasicDeviceStatics interface, IActiveBasicDeviceStatics interface [Media Streaming API],GetDevicesOnMatchingNetworkAsync method, IActiveBasicDeviceStatics.GetDevicesOnMatchingNetworkAsync, IActiveBasicDeviceStatics.streaming, IActiveBasicDeviceStatics::GetDevicesOnMatchingNetworkAsync, IActiveBasicDeviceStatics::streaming, mediastreaming.iactivebasicdevicestatics_getdevicesonmatchingnetworkasync, windows/IActiveBasicDeviceStatics::GetDevicesOnMatchingNetworkAsync
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - PlayToDevice.dll
api_name:
 - IActiveBasicDeviceStatics.GetDevicesOnMatchingNetworkAsync
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IActiveBasicDeviceStatics::streaming


## -description


Asynchronously gets a <a href="https://msdn.microsoft.com/88F63873-9844-4EF9-A868-5CA0330F9242">DevicePair</a> of devices that are on the same network interface.


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

The asynchronous operation. Upon completion, <a href="https://msdn.microsoft.com/1E40AEED-8D57-4FBC-AF25-11B27399477C">IAsyncOperation.GetResults</a> returns a <a href="https://msdn.microsoft.com/88F63873-9844-4EF9-A868-5CA0330F9242">DevicePair</a> object.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/B4D8BAEF-AD30-4FEC-9527-583E88C8B4C7">IActiveBasicDeviceStatics</a>
 

 

