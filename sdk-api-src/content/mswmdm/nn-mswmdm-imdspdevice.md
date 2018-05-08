---
UID: NN:mswmdm.IMDSPDevice
title: IMDSPDevice
author: windows-driver-content
description: The IMDSPDevice interface provides an instance-based association with a media device.
old-location: wmdm\imdspdevice.htm
old-project: WMDM
ms.assetid: 98f16547-4d8a-4422-ba08-c3c678142492
ms.author: windowsdriverdev
ms.date: 4/17/2018
ms.keywords: IMDSPDevice, IMDSPDevice interface [windows Media Device Manager], IMDSPDevice interface [windows Media Device Manager],described, IMDSPDeviceInterface, mswmdm/IMDSPDevice, wmdm.imdspdevice
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: mswmdm.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: MSVidCtlStateList
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	mswmdm.h
api_name:
-	IMDSPDevice
product: Windows
targetos: Windows
req.lib: Mssachlp.lib
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IMDSPDevice interface


## -description



The <b>IMDSPDevice</b> interface provides an instance-based association with a media device. Using this interface, the client can get a storage media enumerator for the device, get information about the device, and send opaque (pass-through) commands to the device. <a href="https://msdn.microsoft.com/d9ffaea8-5616-4bc2-a27c-8b77ea177b6b">IMDServiceProvider2</a> extends <b>IMDSPDevice</b> by providing methods for getting video formats, getting Plug and Play (PnP) device names, enabling the use of property pages, and making it possible to get a pointer to a storage medium from its name. This interface is optional for the service provider but is recommended.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMDSPDevice</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMDSPDevice</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMDSPDevice</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bbf19979-8e09-476e-9401-443ab5e84866">EnumStorage</a>
</td>
<td align="left" width="63%">
Enumerates the top-level storage medium on the device. This method is mandatory.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0a7fcae6-cf7f-4b78-847c-de9db8c32871">GetDeviceIcon</a>
</td>
<td align="left" width="63%">
Retrieves a <b>HICON</b> value that represents the icon that the device service provider indicates must be used to represent this device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ac50ac7d-bd55-4ece-8af8-5c8b2f7736e8">GetFormatSupport</a>
</td>
<td align="left" width="63%">
Enumerates the formats supported by the device. This method is mandatory.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5dc5abe8-f43b-4cff-baa1-cef9e2c1a7a4">GetManufacturer</a>
</td>
<td align="left" width="63%">
Retrieves the name of the manufacturer of the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bc4fef6e-8faf-4114-a68d-bbc30bc18130">GetName</a>
</td>
<td align="left" width="63%">
Retrieves the name of the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/476e25cf-de18-4039-994c-570fa423821f">GetPowerSource</a>
</td>
<td align="left" width="63%">
Reports whether the device is capable of running on batteries, external power, or both, and on which type of power source it is currently running.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/dfff9660-fc74-421c-91d2-3d6be1c753da">GetSerialNumber</a>
</td>
<td align="left" width="63%">
Retrieves the serial number that uniquely identifies the device. This method is mandatory.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh406321">GetStatus</a>
</td>
<td align="left" width="63%">
Retrieves the device status information. This method is mandatory.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/jj991813">GetType</a>
</td>
<td align="left" width="63%">
Retrieves device type information. This method is mandatory.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/88c935ad-dbf0-41bb-8676-ddafe9d1fe0e">GetVersion</a>
</td>
<td align="left" width="63%">
Retrieves the version number of the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d7b60187-84d1-4ff3-ab58-e6b8ea75ee37">SendOpaqueCommand</a>
</td>
<td align="left" width="63%">
Sends a command to a device through Windows Media Device Manager. Windows Media Device Manager transmits the command without acting on it.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/a53052a1-89f4-4571-9eee-031e0049a92e">IMDSPDevice2 Interface</a>



<a href="https://msdn.microsoft.com/919c26f4-6954-462a-8b4a-530e78bb72e6">IMDSPDevice3 Interface</a>



<a href="https://msdn.microsoft.com/bd61c5fa-047c-4d93-bae1-f3433696b95b">Interfaces for Service Providers</a>
 

 

