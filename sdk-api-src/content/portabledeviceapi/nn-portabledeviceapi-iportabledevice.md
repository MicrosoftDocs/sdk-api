---
UID: NN:portabledeviceapi.IPortableDevice
title: IPortableDevice
author: windows-sdk-content
description: The IPortableDevice interface provides access to a portable device.
old-location: wpdsdk\iportabledevice.htm
old-project: wpd_sdk
ms.assetid: 98c48e56-56b8-4800-b52b-ac08f2abf27e
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IPortableDevice, IPortableDevice interface [Windows Portable Devices SDK], IPortableDevice interface [Windows Portable Devices SDK],described, IPortableDeviceInterface, portabledeviceapi/IPortableDevice, wpdsdk.iportabledevice
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: portabledeviceapi.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: PNRPINFO_V2, *PPNRPINFO_V2
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - PortableDeviceGUIDs.lib
 - PortableDeviceGUIDs.dll
api_name:
 - IPortableDevice
product: Windows
targetos: Windows
req.lib: PortableDeviceGUIDs.lib
req.dll: 
req.irql: 
req.product: ADAM
---

# IPortableDevice interface


## -description


The <b>IPortableDevice</b> interface provides access to a portable device.

To create and open this interface, first call <a href="6f361b8b-490a-4ee9-88a9-129a0f0f91dd">CoCreateInstance</a> with <b>CLSID_PortableDeviceFTM</b>  or <b>CLSID_PortableDevice</b>to retrieve an <b>IPortableDevice</b> interface, and then call <a href="https://msdn.microsoft.com/d505fc34-9b6d-417a-a53e-e74773dcc8a4">Open</a> to open a connection to the device.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IPortableDevice</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IPortableDevice</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IPortableDevice</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bab28a19-7ba2-4edd-b5aa-c2017b4bf8ca">Advise</a>
</td>
<td align="left" width="63%">
Registers an application-defined callback that receives device events.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/dcda2e43-ee12-44a4-a7ab-a2a542082d07">Cancel</a>
</td>
<td align="left" width="63%">
Cancels a pending operation on this interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3d44e488-1bef-4cdd-bb0b-2b8154deb19e">Capabilities</a>
</td>
<td align="left" width="63%">
Retrieves an interface used to query the capabilities of a portable device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/aa60a439-7589-465e-98e5-56b93d594f96">Close</a>
</td>
<td align="left" width="63%">
Closes the connection with the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f65ff0b5-ca3b-498f-9c5e-36a76104d220">Content</a>
</td>
<td align="left" width="63%">
Retrieves an interface used to access objects on a device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e6bde2ac-ceef-47f8-b60b-e61595078e8c">GetPnPDeviceID</a>
</td>
<td align="left" width="63%">
Retrieves a Plug-and-Play (PnP) identifier used to open a device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d505fc34-9b6d-417a-a53e-e74773dcc8a4">Open</a>
</td>
<td align="left" width="63%">
Opens a connection between the application and the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ccc7f87a-dea3-4a1e-a181-86928e23bd35">SendCommand</a>
</td>
<td align="left" width="63%">
Sends a command to the device and retrieves the results synchronously.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6720e92b-35cd-4e3f-bd21-36337cf80140">Unadvise</a>
</td>
<td align="left" width="63%">
Unregisters a client from receiving callback notifications.

</td>
</tr>
</table> 


## -remarks



The client interfaces are designed to be used for any WPD object; it is not necessary to create a new instance for each object referenced by the application. After an application opens an instance of the <b>IPortableDevice</b> interface, it should open and cache any other WPD client interfaces that it will require.
      

For Windows 7, <a href="https://msdn.microsoft.com/f57344d5-c978-4c27-b8a9-b42492bd9312">IPortableDevice</a> supports two CLSIDs for <b>CoCreateInstance</b>. <b>CLSID_PortableDevice</b> returns an <b>IPortableDevice</b> pointer that does not aggregate the free-threaded marshaler; <b>CLSID_PortableDeviceFTM</b> is a new CLSID that returns an <b>IPortableDevice</b> pointer that aggregates the free-threaded marshaler.  Both pointers support the same functionality otherwise.

Applications that live in Single Threaded Apartments should use <b>CLSID_PortableDeviceFTM</b> as this eliminates the overhead of interface pointer marshaling.  <b>CLSID_PortableDevice</b> is still supported for legacy applications.




## -see-also




<a href="https://msdn.microsoft.com/fbe53f17-940a-485e-82b2-c11ae39b3300">Client Interfaces</a>
 

 

