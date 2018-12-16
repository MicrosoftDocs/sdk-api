---
UID: NN:windows.media.streaming.IActiveBasicDevice
title: IActiveBasicDevice
author: windows-sdk-content
description: Represents an active IBasicDevice that is associated with a UPnP device.
old-location: mediastreaming\iactivebasicdevice.htm
tech.root: mediastreaming
ms.assetid: 97544BF4-188F-4CE3-9436-EB7F3E706E94
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IActiveBasicDevice, IActiveBasicDevice interface [Media Streaming API], IActiveBasicDevice interface [Media Streaming API],described, mediastreaming.iactivebasicdevice, windows/IActiveBasicDevice
ms.topic: interface
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IActiveBasicDevice interface


## -description


Represents an active <a href="https://msdn.microsoft.com/E4F99A11-4ED5-44CB-BE16-CBB558412ED4">IBasicDevice</a> that is associated with a UPnP device. 


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IActiveBasicDevice</b> interface inherits from <a href="https://msdn.microsoft.com/E4F99A11-4ED5-44CB-BE16-CBB558412ED4">IBasicDevice</a>. <b>IActiveBasicDevice</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/342F5240-E29D-4CC4-AA49-B039EBFC4D0B">GetCachedBitrateMeasurement</a>
</td>
<td align="left" width="63%">
Gets the cached bitrate.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/AEBB181A-CF30-4BAE-8316-76B2E8FF3A81">GetCachedExtraSinkProtocolInfo</a>
</td>
<td align="left" width="63%">
Gets additional cached sink protocol info for the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/A4FF565E-0CB1-456B-A4C1-436EFA209FA2">GetCachedSinkProtocolInfo</a>
</td>
<td align="left" width="63%">
Gets the cached sink protocol info for the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/894EC907-E578-4F1E-A0AB-1FDE2FA67B6C">GetEffectiveBandwidth</a>
</td>
<td align="left" width="63%">
Gets the current effective bandwidth for the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/71CC39DC-B8FB-4E93-8C01-E099B1F95B11">IsAudioSupported</a>
</td>
<td align="left" width="63%">
Gets a value that indicates if the device supports audio.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4E6CFF0E-0A84-4527-8184-ECF78503A463">IsImageSupported</a>
</td>
<td align="left" width="63%">
Gets a value that indicates if the devices supports images.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/B45C71E8-75EF-46CD-BE05-3FB828B70061">IsMuteSupported</a>
</td>
<td align="left" width="63%">
Gets a value that indicates if the device supports muting.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9B31B188-C896-4F01-A2BD-03A43FB399F8">IsSearchSupported</a>
</td>
<td align="left" width="63%">
Gets a value that indicates if the device supports search.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8A764C13-C790-4FE7-8161-2AB486D2D8D3">IsSetNextSourceSupported</a>
</td>
<td align="left" width="63%">
Gets a value that indicates if setting the next source is supported. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6EBB6951-A1B4-4598-9E81-7EDD6556DF4E">IsVideoSupported</a>
</td>
<td align="left" width="63%">
Gets a value that indicates if the device supports video.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/24F93A51-7E4B-46C8-B381-E81B6E31F654">LogicalNetworkInterface</a>
</td>
<td align="left" width="63%">
Gets the id of the logical network interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6E52FBB1-6822-4D68-9C45-1EFEF1808CD0">MaxVolume</a>
</td>
<td align="left" width="63%">
Gets the maximum volume  supported by the device. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/D62E8571-1DE9-4BAB-A291-415FD6E9F9C8">NotifyStreamingStatus</a>
</td>
<td align="left" width="63%">
Called by the application to indicate  that  the device is being used for active streaming. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/CEF49E0D-E6C6-4208-A6F3-1689C1CD6186">PhysicalNetworkInterface</a>
</td>
<td align="left" width="63%">
Gets the id of the physical network interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/B695D51C-205B-4D45-BEA7-0235FC770C77">SetCachedBitrateMeasurement</a>
</td>
<td align="left" width="63%">
Sets the cached bitrate.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/210AEE22-0AFD-43B1-8380-8A67D17AB7CB">SetCachedSinkProtocolInfo</a>
</td>
<td align="left" width="63%">
Gets the cached sink protocol info for the device.

</td>
</tr>
</table> 


## -remarks



An <b>IActiveBasicDevice</b> is associated with a UPnP device.  To retrieve  a pointer to the underlying <a href="https://msdn.microsoft.com/566cc606-3dfb-4052-93b0-3c922bf30f84">IUPnPDevice</a>, 	<b>IServiceProvider-&gt;QueryService</b> can be used with <b>GUID_NativeDeviceService</b> to get native interfaces for the device.


 For example, you can retrieve a <a href="https://msdn.microsoft.com/566cc606-3dfb-4052-93b0-3c922bf30f84">IUPnPDevice</a> pointer as follows: 


```cpp
pActiveBasicDevice->QueryService( GUID_NativeDeviceService, IID_IUPnPDevice, (void **)&spUPnPDevice );
```







## -see-also




<a href="https://msdn.microsoft.com/E4F99A11-4ED5-44CB-BE16-CBB558412ED4">IBasicDevice</a>
 

 

