---
UID: NN:portabledeviceapi.IPortableDeviceCapabilities
title: IPortableDeviceCapabilities
author: windows-sdk-content
description: The IPortableDeviceCapabilities interface a variety of device capabilities, including supported formats, commands, and functional objects. You can retrieve this interface from a device by calling IPortableDevice::Capabilities.
old-location: wpdsdk\iportabledevicecapabilities.htm
old-project: wpd_sdk
ms.assetid: c292a509-f202-4136-bbf7-b4e82ef2b936
ms.author: windowssdkdev
ms.date: 04/11/2018
ms.keywords: IPortableDeviceCapabilities, IPortableDeviceCapabilities interface [Windows Portable Devices SDK], IPortableDeviceCapabilities interface [Windows Portable Devices SDK],described, portabledeviceapi/IPortableDeviceCapabilities, wpdsdk.iportabledevicecapabilities
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: portabledeviceapi.h
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
req.typenames: PNRPINFO_V2, *PPNRPINFO_V2
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	portabledeviceapi.h
api_name:
-	IPortableDeviceCapabilities
product: Windows
targetos: Windows
req.lib: PortableDeviceGUIDs.lib
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IPortableDeviceCapabilities interface


## -description



The <b>IPortableDeviceCapabilities</b> interface a variety of device capabilities, including supported formats, commands, and functional objects. You can retrieve this interface from a device by calling <b>IPortableDevice::Capabilities</b>.





## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IPortableDeviceCapabilities</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IPortableDeviceCapabilities</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IPortableDeviceCapabilities</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh406716">Cancel</a>
</td>
<td align="left" width="63%">
Cancels a pending call on this interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d222968f-3ca7-4a4d-bdc6-89a6ca98c7b0">GetCommandOptions</a>
</td>
<td align="left" width="63%">
Retrieves all the supported options for the specified command on the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b4d3495b-b2d3-4d0d-8dc6-df030a52ab3f">GetEventOptions</a>
</td>
<td align="left" width="63%">
Retrieves all the supported options for the specified event on the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/94e4e9f4-5858-4e12-bcd7-561fb3636fc8">GetFixedPropertyAttributes</a>
</td>
<td align="left" width="63%">
Retrieves the standard property attributes for a specified property and format.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c444f9d6-7bef-4e0a-bcd8-6a6110986208">GetFunctionalCategories</a>
</td>
<td align="left" width="63%">
Retrieves all functional categories supported by the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/46657e4d-c2fe-42bf-9a3d-5075d4f3ee91">GetFunctionalObjects</a>
</td>
<td align="left" width="63%">
 Retrieves all functional objects that match a specified category on the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/974b16c7-27a0-40a6-8941-e93293a69b48">GetSupportedCommands</a>
</td>
<td align="left" width="63%">
Retrieves a list of all the supported commands for this device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5f56ca91-552f-4a52-8a68-225601c5f6f4">GetSupportedContentTypes</a>
</td>
<td align="left" width="63%">
Retrieves all supported content types for a specified functional object type on a device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f5082b2b-d925-4f9d-bbfd-edcf4553a6fa">GetSupportedEvents</a>
</td>
<td align="left" width="63%">
Retrieves the supported events for this device.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/34ea5f04-9cb8-49a2-8d49-14688383c4a6">GetSupportedFormatProperties</a>
</td>
<td align="left" width="63%">
Retrieves the properties supported by objects of a specified format on the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7568f5cf-2f9e-459c-ae08-d23b9e37ce4e">GetSupportedFormats</a>
</td>
<td align="left" width="63%">
Retrieves the supported formats for a specified object type on the device.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/fbe53f17-940a-485e-82b2-c11ae39b3300">Client Interfaces</a>
 

 

