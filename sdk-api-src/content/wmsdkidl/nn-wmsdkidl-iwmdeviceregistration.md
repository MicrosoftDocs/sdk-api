---
UID: NN:wmsdkidl.IWMDeviceRegistration
title: IWMDeviceRegistration
author: windows-sdk-content
description: The IWMDeviceRegistration interface registers playback devices for secure data delivery.You can create a device registration object and retrieve a pointer to its IWMDeviceRegistration interface by calling the WMCreateDeviceRegistration function.
old-location: wmformat\iwmdeviceregistration.htm
old-project: wmformat
ms.assetid: fb08ddae-2abf-4a86-a5d8-ea745ae35aa8
ms.author: windowssdkdev
ms.date: 06/04/2018
ms.keywords: IWMDeviceRegistration, IWMDeviceRegistration interface [windows Media Format], IWMDeviceRegistration interface [windows Media Format],described, IWMDeviceRegistrationInterface, wmformat.iwmdeviceregistration, wmsdkidl/IWMDeviceRegistration
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: wmsdkidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: WM_AETYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wmsdkidl.h
api_name:
 - IWMDeviceRegistration
product: Windows
targetos: Windows
req.lib: Wmvcore.lib
req.dll: Wmvcore.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMDeviceRegistration interface


## -description


<p class="CCE_Message">[<b>IWMDeviceRegistration</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="http://go.microsoft.com/fwlink/p/?linkid=325240">Microsoft PlayReady</a>.
]


The <b>IWMDeviceRegistration</b> interface registers playback devices for secure data delivery.

You can create a device registration object and retrieve a pointer to its <b>IWMDeviceRegistration</b> interface by calling the <a href="https://msdn.microsoft.com/0e318691-07dc-421b-951d-9e65e9160bb0">WMCreateDeviceRegistration</a> function.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMDeviceRegistration</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWMDeviceRegistration</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMDeviceRegistration</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a11249f5-0604-4de7-9dd2-152d570183c3">GetFirstRegisteredDevice</a>
</td>
<td align="left" width="63%">
Retrieves information for the first device in the device registration database.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/396e60a8-5845-45fa-8393-6f0defbd38bb">GetNextRegisteredDevice</a>
</td>
<td align="left" width="63%">
Retrieves information for the second and subsequent devices in the device registration database.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/26ded37b-1169-4c47-8880-bd19c977171e">GetRegisteredDeviceByID</a>
</td>
<td align="left" width="63%">
Retrieves information about a device specified by the device identifier.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/56c5b2c7-46c2-42e4-a7d4-f1b3e56ffbcb">GetRegistrationStats</a>
</td>
<td align="left" width="63%">
Retrieves the number of devices of a specified type that exist in the device registration database.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cdce6941-dac9-4de5-8230-904c26e82642">RegisterDevice</a>
</td>
<td align="left" width="63%">
Adds a device to the device registration database.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5cb1282a-5744-4264-8f73-ecad2854a125">UnregisterDevice</a>
</td>
<td align="left" width="63%">
Removes a device from the device registration database.

</td>
</tr>
</table> 


## -remarks



The primary purpose of the device registration database is to store data about connected devices that can receive streaming media encoded for the Windows Media DRM 10 for Network Devices protocol. You can enter other devices in the database if desired.

The device registration database is a secure database on the client computer. All interactions with the database are managed internally; your application does not have direct access to it.

The same device registration database is used by all applications.

Devices in the database are registered by type. Devices that support Windows Media DRM 10 for Network Devices use the DRM_DEVICE_REGISTER_TYPE_STREAMING register type. Other types may be supported in future versions.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/dn965732">Interfaces</a>
 

 

