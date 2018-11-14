---
UID: NN:portabledeviceapi.IPortableDeviceManager
title: IPortableDeviceManager
author: windows-sdk-content
description: Enumerates devices that are connected to the computer and provides a simple way to request installation information, including manufacturer, friendly name, and description.
old-location: wpdsdk\iportabledevicemanager.htm
tech.root: wpd_sdk
ms.assetid: 11cd5b2b-e8f8-4ba1-8527-f7a403f399d5
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IPortableDeviceManager, IPortableDeviceManager interface [Windows Portable Devices SDK], IPortableDeviceManager interface [Windows Portable Devices SDK],described, IPortableDeviceManagerInterface, portabledeviceapi/IPortableDeviceManager, wpdsdk.iportabledevicemanager
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: PortableDeviceGUIDs.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - PortableDeviceGUIDs.lib
 - PortableDeviceGUIDs.dll
api_name:
 - IPortableDeviceManager
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IPortableDeviceManager interface


## -description



Enumerates devices that are connected to the computer and provides a simple way to request installation information, including manufacturer, friendly name, and description. This is typically the first Windows Portable Devices interface created by an application. To create an instance of this interface, call <b>CoCreateInstance</b> and specify <b>CLSID_PortableDeviceManager</b>.

The properties that are requested using this interface can also be requested by using the <a href="https://msdn.microsoft.com/4555e85b-c667-466c-a527-cc29ca7a6aee">IPortableDeviceProperties</a> interface. However, that interface requires several steps to acquire; using this interface is a much simpler way to request device information.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IPortableDeviceManager</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IPortableDeviceManager</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IPortableDeviceManager</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/16c08c8a-9ce7-455a-9859-6b0be406f642">GetDeviceDescription</a>
</td>
<td align="left" width="63%">
Retrieves the description of a device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/589995bb-fcce-412e-8828-a84e5809af2b">GetDeviceFriendlyName</a>
</td>
<td align="left" width="63%">
Retrieves the user-friendly name for the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2bd64da1-819d-430c-ab66-ab3b8e6c48f6">GetDeviceManufacturer</a>
</td>
<td align="left" width="63%">
Retrieves the name of the device manufacturer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/805a2407-f476-4223-97d9-6d8753380b17">GetDeviceProperty</a>
</td>
<td align="left" width="63%">
Retrieves a property value stored by the device on the computer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5061b3c0-8b93-480d-b1c6-0a6b616a2c8d">GetDevices</a>
</td>
<td align="left" width="63%">
Retrieves a list of portable devices connected to the computer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f25a8eb4-be40-43c0-bb3c-00031b7f08db">GetPrivateDevices</a>
</td>
<td align="left" width="63%">
Retrieves a list of private portable devices connected to the computer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/89163407-7b38-4c79-8171-67a5b7e1d17c">RefreshDeviceList</a>
</td>
<td align="left" width="63%">
Refreshes the list of portable devices that are connected to the computer.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/fbe53f17-940a-485e-82b2-c11ae39b3300">Client Interfaces</a>
 

 

