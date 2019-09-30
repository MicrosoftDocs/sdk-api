---
UID: NN:portabledeviceapi.IPortableDeviceManager
title: IPortableDeviceManager (portabledeviceapi.h)
author: windows-sdk-content
description: Enumerates devices that are connected to the computer and provides a simple way to request installation information, including manufacturer, friendly name, and description.
old-location: wpdsdk\iportabledevicemanager.htm
tech.root: wpd_sdk
ms.assetid: 11cd5b2b-e8f8-4ba1-8527-f7a403f399d5
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IPortableDeviceManager, IPortableDeviceManager interface [Windows Portable Devices SDK], IPortableDeviceManager interface [Windows Portable Devices SDK],described, IPortableDeviceManagerInterface, portabledeviceapi/IPortableDeviceManager, wpdsdk.iportabledevicemanager
ms.topic: interface
f1_keywords: 
 - "portabledeviceapi/IPortableDeviceManager"
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IPortableDeviceManager interface


## -description



Enumerates devices that are connected to the computer and provides a simple way to request installation information, including manufacturer, friendly name, and description. This is typically the first Windows Portable Devices interface created by an application. To create an instance of this interface, call <b>CoCreateInstance</b> and specify <b>CLSID_PortableDeviceManager</b>.

The properties that are requested using this interface can also be requested by using the <a href="https://docs.microsoft.com/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties">IPortableDeviceProperties</a> interface. However, that interface requires several steps to acquire; using this interface is a much simpler way to request device information.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IPortableDeviceManager</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IPortableDeviceManager</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/portabledeviceapi/nf-portabledeviceapi-iportabledevicemanager-getdevicedescription">GetDeviceDescription</a>
</td>
<td align="left" width="63%">
Retrieves the description of a device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/portabledeviceapi/nf-portabledeviceapi-iportabledevicemanager-getdevicefriendlyname">GetDeviceFriendlyName</a>
</td>
<td align="left" width="63%">
Retrieves the user-friendly name for the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/portabledeviceapi/nf-portabledeviceapi-iportabledevicemanager-getdevicemanufacturer">GetDeviceManufacturer</a>
</td>
<td align="left" width="63%">
Retrieves the name of the device manufacturer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/portabledeviceapi/nf-portabledeviceapi-iportabledevicemanager-getdeviceproperty">GetDeviceProperty</a>
</td>
<td align="left" width="63%">
Retrieves a property value stored by the device on the computer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/portabledeviceapi/nf-portabledeviceapi-iportabledevicemanager-getdevices">GetDevices</a>
</td>
<td align="left" width="63%">
Retrieves a list of portable devices connected to the computer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/portabledeviceapi/nf-portabledeviceapi-iportabledevicemanager-getprivatedevices">GetPrivateDevices</a>
</td>
<td align="left" width="63%">
Retrieves a list of private portable devices connected to the computer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/portabledeviceapi/nf-portabledeviceapi-iportabledevicemanager-refreshdevicelist">RefreshDeviceList</a>
</td>
<td align="left" width="63%">
Refreshes the list of portable devices that are connected to the computer.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/wpd_sdk/client-interfaces">Client Interfaces</a>
 

 

