---
UID: NN:mswmdm.IWMDMDevice
title: IWMDMDevice
author: windows-sdk-content
description: The IWMDMDevice interface provides methods to examine and explore a single portable device. The interface can be used to get information about a device and enumerate its storages. IWMDMDevice2 extends the capabilities of this interface.
old-location: wmdm\iwmdmdevice.htm
tech.root: WMDM
ms.assetid: 44212da9-a38a-4ed5-86af-cf60b40bb54d
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IWMDMDevice, IWMDMDevice interface [windows Media Device Manager], IWMDMDevice interface [windows Media Device Manager],described, IWMDMDeviceInterface, mswmdm/IWMDMDevice, wmdm.iwmdmdevice
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mswmdm.h
api_name:
 - IWMDMDevice
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMDMDevice interface


## -description



The <b>IWMDMDevice</b> interface provides methods to examine and explore a single portable device. The interface can be used to get information about a device and enumerate its storages. <a href="https://msdn.microsoft.com/d8dcbde1-24ae-4ca6-aaf4-2d1511102ae9">IWMDMDevice2</a> extends the capabilities of this interface.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMDMDevice</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWMDMDevice</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMDMDevice</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ffd3c51a-7ec2-4ce5-9260-2b08bfa88a99">EnumStorage</a>
</td>
<td align="left" width="63%">
Retrieves an <a href="https://msdn.microsoft.com/6ea80ab2-718b-464e-a805-9910460931bb">IWMDMEnumStorage</a> interface to enumerate the storages on a device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/55da3443-ad5b-469d-a493-0e2e8ea21f0c">GetDeviceIcon</a>
</td>
<td align="left" width="63%">
Retrieves a handle to the icon that the device manufacturer wants to display when the device is connected.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a917660d-300f-4ac4-befe-a3f78172411e">GetFormatSupport</a>
</td>
<td align="left" width="63%">
Retrieves all the formats supported by the device, including codecs and file formats.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/42e862e4-bfbc-4fca-b5df-001416173d6e">GetManufacturer</a>
</td>
<td align="left" width="63%">
Retrieves the name of the manufacturer of the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4bc5d550-6631-40ea-b020-2f5bb55899d6">GetName</a>
</td>
<td align="left" width="63%">
Retrieves the human-readable name of the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0e13ac64-69b7-4c44-8690-8fcef6cb354f">GetPowerSource</a>
</td>
<td align="left" width="63%">
Retrieves information about the power source and the percentage of power remaining for the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e2498ca3-7109-4713-9110-2dbca0436d00">GetSerialNumber</a>
</td>
<td align="left" width="63%">
Retrieves a serial number that uniquely identifies the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/18445ba5-6c91-4b4c-8f9b-b9d94fd96155">GetStatus</a>
</td>
<td align="left" width="63%">
Retrieves device status information.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b240d6ac-99bd-4cc2-92d8-e9c7c5834bd7">GetType</a>
</td>
<td align="left" width="63%">
Retrieves the operations supported by the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ae0253f2-30cd-46d0-b9e9-f2cb878c1ff3">GetVersion</a>
</td>
<td align="left" width="63%">
Retrieves the manufacturer-defined version number of the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4554318b-497f-488f-a52f-a392b8fee992">SendOpaqueCommand</a>
</td>
<td align="left" width="63%">
Sends a device-specific command to the device through Windows Media Device Manager.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/d8dcbde1-24ae-4ca6-aaf4-2d1511102ae9">IWMDMDevice2 Interface</a>



<a href="https://msdn.microsoft.com/29e0ec95-c1ea-4157-b5aa-39d80fff407d">IWMDMDevice3 Interface</a>



<a href="https://msdn.microsoft.com/bea867d6-a875-4150-9958-7f683cd215b9">Interfaces for Applications</a>
 

 

