---
UID: NF:windows.media.streaming.IActiveBasicDeviceStatics.CreateDevicesOnMatchingNetworkAsync
title: IActiveBasicDeviceStatics::streaming (windows.media.streaming.h)
author: windows-sdk-content
description: Asynchronously creates a DevicePair of devices that are on the same network interface.
old-location: mediastreaming\iactivebasicdevicestatics_createdevicesonmatchingnetworkasync.htm
tech.root: mediastreaming
ms.assetid: E113C600-1F55-4653-A4FD-A1286699B137
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CreateDevicesOnMatchingNetworkAsync, CreateDevicesOnMatchingNetworkAsync method [Media Streaming API], CreateDevicesOnMatchingNetworkAsync method [Media Streaming API],IActiveBasicDeviceStatics interface, IActiveBasicDeviceStatics interface [Media Streaming API],CreateDevicesOnMatchingNetworkAsync method, IActiveBasicDeviceStatics.CreateDevicesOnMatchingNetworkAsync, IActiveBasicDeviceStatics.streaming, IActiveBasicDeviceStatics::CreateDevicesOnMatchingNetworkAsync, IActiveBasicDeviceStatics::streaming, mediastreaming.iactivebasicdevicestatics_createdevicesonmatchingnetworkasync, windows/IActiveBasicDeviceStatics::CreateDevicesOnMatchingNetworkAsync
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
 - IActiveBasicDeviceStatics.CreateDevicesOnMatchingNetworkAsync
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IActiveBasicDeviceStatics::streaming


## -description


Asynchronously creates a <a href="https://msdn.microsoft.com/88F63873-9844-4EF9-A868-5CA0330F9242">DevicePair</a> of devices that are on the same network interface.


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

The asynchronous operation. Upon completion, <a href="https://msdn.microsoft.com/1E40AEED-8D57-4FBC-AF25-11B27399477C">IAsyncOperation.GetResults</a> returns a <a href="https://msdn.microsoft.com/88F63873-9844-4EF9-A868-5CA0330F9242">DevicePair</a> object.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/B4D8BAEF-AD30-4FEC-9527-583E88C8B4C7">IActiveBasicDeviceStatics</a>
 

 

