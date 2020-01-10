---
UID: NN:windows.media.streaming.IActiveBasicDeviceStatics
title: IActiveBasicDeviceStatics (windows.media.streaming.h)
description: Provides static methods for creating IActiveBasicDevice objects.
old-location: mediastreaming\iactivebasicdevicestatics.htm
tech.root: mediastreaming
ms.assetid: B4D8BAEF-AD30-4FEC-9527-583E88C8B4C7
ms.date: 12/05/2018
ms.keywords: IActiveBasicDeviceStatics, IActiveBasicDeviceStatics interface [Media Streaming API], IActiveBasicDeviceStatics interface [Media Streaming API],described, mediastreaming.iactivebasicdevicestatics, windows/IActiveBasicDeviceStatics
f1_keywords:
- windows.media.streaming/IActiveBasicDeviceStatics
dev_langs:
- c++
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
- IActiveBasicDeviceStatics
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IActiveBasicDeviceStatics interface


## -description


Provides static methods for creating <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-iactivebasicdevice">IActiveBasicDevice</a> objects.  


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IActiveBasicDeviceStatics</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/inspectable/nn-inspectable-iinspectable">IInspectable</a>. <b>IActiveBasicDeviceStatics</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IActiveBasicDeviceStatics</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-iactivebasicdevicestatics-clonebasicdeviceasync">CloneBasicDeviceAsync</a>
</td>
<td align="left" width="63%">
Asynchronously creates a clone of a basic device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-iactivebasicdevicestatics-createbasicdeviceasync">CreateBasicDeviceAsync</a>
</td>
<td align="left" width="63%">
Asynchronously creates an active basic device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-iactivebasicdevicestatics-createdevicesonmatchingnetworkasync">CreateDevicesOnMatchingNetworkAsync</a>
</td>
<td align="left" width="63%">
Asynchronously creates a <a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/dn385771(v=vs.85)">DevicePair</a> of devices that are on the same network interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-iactivebasicdevicestatics-getdevicesonmatchingnetworkasync">GetDevicesOnMatchingNetworkAsync</a>
</td>
<td align="left" width="63%">
Asynchronously gets a <a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/dn385771(v=vs.85)">DevicePair</a> of devices that are on the same network interface.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/dn385755(v=vs.85)">ActiveBasicDevice</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/hh828813(v=vs.85)">BasicDevice</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-iactivebasicdevice">IActiveBasicDevice</a>



<a href="https://docs.microsoft.com/windows/desktop/mediastreaming/ibasicdevice">IBasicDevice</a>



<a href="https://docs.microsoft.com/windows/desktop/api/inspectable/nn-inspectable-iinspectable">IInspectable</a>
 

 

