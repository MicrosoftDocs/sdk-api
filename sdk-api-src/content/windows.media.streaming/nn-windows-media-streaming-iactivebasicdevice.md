---
UID: NN:windows.media.streaming.IActiveBasicDevice
title: IActiveBasicDevice (windows.media.streaming.h)
description: Represents an active IBasicDevice that is associated with a UPnP device.
helpviewer_keywords: ["IActiveBasicDevice","IActiveBasicDevice interface [Media Streaming API]","IActiveBasicDevice interface [Media Streaming API]","described","mediastreaming.iactivebasicdevice","windows/IActiveBasicDevice"]
old-location: mediastreaming\iactivebasicdevice.htm
tech.root: mediastreaming
ms.assetid: 97544BF4-188F-4CE3-9436-EB7F3E706E94
ms.date: 12/05/2018
ms.keywords: IActiveBasicDevice, IActiveBasicDevice interface [Media Streaming API], IActiveBasicDevice interface [Media Streaming API],described, mediastreaming.iactivebasicdevice, windows/IActiveBasicDevice
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
 - IActiveBasicDevice
 - windows.media.streaming/IActiveBasicDevice
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
 - IActiveBasicDevice
---

# IActiveBasicDevice interface


## -description

Represents an active <a href="/windows/desktop/mediastreaming/ibasicdevice">IBasicDevice</a> that is associated with a UPnP device.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IActiveBasicDevice</b> interface inherits from <a href="/windows/desktop/mediastreaming/ibasicdevice">IBasicDevice</a>. <b>IActiveBasicDevice</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -remarks

An <b>IActiveBasicDevice</b> is associated with a UPnP device.  To retrieve  a pointer to the underlying <a href="/windows/desktop/api/upnp/nn-upnp-iupnpdevice">IUPnPDevice</a>, 	<b>IServiceProvider-&gt;QueryService</b> can be used with <b>GUID_NativeDeviceService</b> to get native interfaces for the device.


 For example, you can retrieve a <a href="/windows/desktop/api/upnp/nn-upnp-iupnpdevice">IUPnPDevice</a> pointer as follows: 


```cpp
pActiveBasicDevice->QueryService( GUID_NativeDeviceService, IID_IUPnPDevice, (void **)&spUPnPDevice );
```

## -see-also

<a href="/windows/desktop/mediastreaming/ibasicdevice">IBasicDevice</a>
