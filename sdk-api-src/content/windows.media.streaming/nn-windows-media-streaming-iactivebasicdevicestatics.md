---
UID: NN:windows.media.streaming.IActiveBasicDeviceStatics
title: IActiveBasicDeviceStatics
author: windows-sdk-content
description: Provides static methods for creating IActiveBasicDevice objects.
old-location: mediastreaming\iactivebasicdevicestatics.htm
tech.root: mediastreaming
ms.assetid: B4D8BAEF-AD30-4FEC-9527-583E88C8B4C7
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IActiveBasicDeviceStatics, IActiveBasicDeviceStatics interface [Media Streaming API], IActiveBasicDeviceStatics interface [Media Streaming API],described, mediastreaming.iactivebasicdevicestatics, windows/IActiveBasicDeviceStatics
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
 - IActiveBasicDeviceStatics
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IActiveBasicDeviceStatics interface


## -description


Provides static methods for creating <a href="https://msdn.microsoft.com/97544BF4-188F-4CE3-9436-EB7F3E706E94">IActiveBasicDevice</a> objects.  


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IActiveBasicDeviceStatics</b> interface inherits from <a href="https://msdn.microsoft.com/0657E51F-D4C0-46C6-927D-B01E54B6846C">IInspectable</a>. <b>IActiveBasicDeviceStatics</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/B79B569D-FADF-437E-A2F5-DB9C176F570C">CloneBasicDeviceAsync</a>
</td>
<td align="left" width="63%">
Asynchronously creates a clone of a basic device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/52342B15-6250-4D46-9188-CC7AD98F09F7">CreateBasicDeviceAsync</a>
</td>
<td align="left" width="63%">
Asynchronously creates an active basic device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/E113C600-1F55-4653-A4FD-A1286699B137">CreateDevicesOnMatchingNetworkAsync</a>
</td>
<td align="left" width="63%">
Asynchronously creates a <a href="https://msdn.microsoft.com/88F63873-9844-4EF9-A868-5CA0330F9242">DevicePair</a> of devices that are on the same network interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9BE3BBD1-F3D3-4EAF-9125-B82AE0DE48AA">GetDevicesOnMatchingNetworkAsync</a>
</td>
<td align="left" width="63%">
Asynchronously gets a <a href="https://msdn.microsoft.com/88F63873-9844-4EF9-A868-5CA0330F9242">DevicePair</a> of devices that are on the same network interface.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/B747505A-7F8F-44F4-A9B3-73A8FE424D5F">ActiveBasicDevice</a>



<a href="https://msdn.microsoft.com/89A080E7-593B-406F-9E9B-4EC5838A619E">BasicDevice</a>



<a href="https://msdn.microsoft.com/97544BF4-188F-4CE3-9436-EB7F3E706E94">IActiveBasicDevice</a>



<a href="https://msdn.microsoft.com/E4F99A11-4ED5-44CB-BE16-CBB558412ED4">IBasicDevice</a>



<a href="https://msdn.microsoft.com/0657E51F-D4C0-46C6-927D-B01E54B6846C">IInspectable</a>
 

 

