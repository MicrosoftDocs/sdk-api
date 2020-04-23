---
UID: NN:windows.media.streaming.IActiveBasicDevice
title: IActiveBasicDevice (windows.media.streaming.h)
description: Represents an active IBasicDevice that is associated with a UPnP device.helpviewer_keywords: ["IActiveBasicDevice","IActiveBasicDevice interface [Media Streaming API]","IActiveBasicDevice interface [Media Streaming API]","described","mediastreaming.iactivebasicdevice","windows/IActiveBasicDevice"]
old-location: mediastreaming\iactivebasicdevice.htm
tech.root: mediastreaming
ms.assetid: 97544BF4-188F-4CE3-9436-EB7F3E706E94
ms.date: 12/05/2018
ms.keywords: IActiveBasicDevice, IActiveBasicDevice interface [Media Streaming API], IActiveBasicDevice interface [Media Streaming API],described, mediastreaming.iactivebasicdevice, windows/IActiveBasicDevice
f1_keywords:
- windows.media.streaming/IActiveBasicDevice
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
- IActiveBasicDevice
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IActiveBasicDevice interface


## -description


Represents an active <a href="https://docs.microsoft.com/windows/desktop/mediastreaming/ibasicdevice">IBasicDevice</a> that is associated with a UPnP device. 


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IActiveBasicDevice</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/mediastreaming/ibasicdevice">IBasicDevice</a>. <b>IActiveBasicDevice</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IActiveBasicDevice</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-iactivebasicdevice-getcachedbitratemeasurement">GetCachedBitrateMeasurement</a>
</td>
<td align="left" width="63%">
Gets the cached bitrate.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-iactivebasicdevice-getcachedextrasinkprotocolinfo">GetCachedExtraSinkProtocolInfo</a>
</td>
<td align="left" width="63%">
Gets additional cached sink protocol info for the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-iactivebasicdevice-getcachedsinkprotocolinfo">GetCachedSinkProtocolInfo</a>
</td>
<td align="left" width="63%">
Gets the cached sink protocol info for the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-iactivebasicdevice-geteffectivebandwidth">GetEffectiveBandwidth</a>
</td>
<td align="left" width="63%">
Gets the current effective bandwidth for the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/dn385785(v=vs.85)">IsAudioSupported</a>
</td>
<td align="left" width="63%">
Gets a value that indicates if the device supports audio.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/dn385786(v=vs.85)">IsImageSupported</a>
</td>
<td align="left" width="63%">
Gets a value that indicates if the devices supports images.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/dn385787(v=vs.85)">IsMuteSupported</a>
</td>
<td align="left" width="63%">
Gets a value that indicates if the device supports muting.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/dn385788(v=vs.85)">IsSearchSupported</a>
</td>
<td align="left" width="63%">
Gets a value that indicates if the device supports search.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/dn385789(v=vs.85)">IsSetNextSourceSupported</a>
</td>
<td align="left" width="63%">
Gets a value that indicates if setting the next source is supported. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/dn385790(v=vs.85)">IsVideoSupported</a>
</td>
<td align="left" width="63%">
Gets a value that indicates if the device supports video.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/dn385791(v=vs.85)">LogicalNetworkInterface</a>
</td>
<td align="left" width="63%">
Gets the id of the logical network interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/dn385792(v=vs.85)">MaxVolume</a>
</td>
<td align="left" width="63%">
Gets the maximum volume  supported by the device. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-iactivebasicdevice-notifystreamingstatus">NotifyStreamingStatus</a>
</td>
<td align="left" width="63%">
Called by the application to indicate  that  the device is being used for active streaming. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/dn385793(v=vs.85)">PhysicalNetworkInterface</a>
</td>
<td align="left" width="63%">
Gets the id of the physical network interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-iactivebasicdevice-setcachedbitratemeasurement">SetCachedBitrateMeasurement</a>
</td>
<td align="left" width="63%">
Sets the cached bitrate.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-iactivebasicdevice-setcachedsinkprotocolinfo">SetCachedSinkProtocolInfo</a>
</td>
<td align="left" width="63%">
Gets the cached sink protocol info for the device.

</td>
</tr>
</table> 


## -remarks



An <b>IActiveBasicDevice</b> is associated with a UPnP device.  To retrieve  a pointer to the underlying <a href="https://docs.microsoft.com/windows/desktop/api/upnp/nn-upnp-iupnpdevice">IUPnPDevice</a>, 	<b>IServiceProvider-&gt;QueryService</b> can be used with <b>GUID_NativeDeviceService</b> to get native interfaces for the device.


 For example, you can retrieve a <a href="https://docs.microsoft.com/windows/desktop/api/upnp/nn-upnp-iupnpdevice">IUPnPDevice</a> pointer as follows: 


```cpp
pActiveBasicDevice->QueryService( GUID_NativeDeviceService, IID_IUPnPDevice, (void **)&spUPnPDevice );
```







## -see-also




<a href="https://docs.microsoft.com/windows/desktop/mediastreaming/ibasicdevice">IBasicDevice</a>
 

 

