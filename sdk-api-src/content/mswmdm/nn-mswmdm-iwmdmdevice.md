---
UID: NN:mswmdm.IWMDMDevice
title: IWMDMDevice (mswmdm.h)
author: windows-sdk-content
description: The IWMDMDevice interface provides methods to examine and explore a single portable device. The interface can be used to get information about a device and enumerate its storages. IWMDMDevice2 extends the capabilities of this interface.
old-location: wmdm\iwmdmdevice.htm
tech.root: WMDM
ms.assetid: 44212da9-a38a-4ed5-86af-cf60b40bb54d
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IWMDMDevice, IWMDMDevice interface [windows Media Device Manager], IWMDMDevice interface [windows Media Device Manager],described, IWMDMDeviceInterface, mswmdm/IWMDMDevice, wmdm.iwmdmdevice
ms.topic: interface
f1_keywords: 
 - "mswmdm/IWMDMDevice"
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMDMDevice interface


## -description



The <b>IWMDMDevice</b> interface provides methods to examine and explore a single portable device. The interface can be used to get information about a device and enumerate its storages. <a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice2">IWMDMDevice2</a> extends the capabilities of this interface.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMDMDevice</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWMDMDevice</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice-enumstorage">EnumStorage</a>
</td>
<td align="left" width="63%">
Retrieves an <a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmenumstorage">IWMDMEnumStorage</a> interface to enumerate the storages on a device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice-getdeviceicon">GetDeviceIcon</a>
</td>
<td align="left" width="63%">
Retrieves a handle to the icon that the device manufacturer wants to display when the device is connected.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice-getformatsupport">GetFormatSupport</a>
</td>
<td align="left" width="63%">
Retrieves all the formats supported by the device, including codecs and file formats.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice-getmanufacturer">GetManufacturer</a>
</td>
<td align="left" width="63%">
Retrieves the name of the manufacturer of the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice-getname">GetName</a>
</td>
<td align="left" width="63%">
Retrieves the human-readable name of the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice-getpowersource">GetPowerSource</a>
</td>
<td align="left" width="63%">
Retrieves information about the power source and the percentage of power remaining for the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice-getserialnumber">GetSerialNumber</a>
</td>
<td align="left" width="63%">
Retrieves a serial number that uniquely identifies the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice-getstatus">GetStatus</a>
</td>
<td align="left" width="63%">
Retrieves device status information.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice-gettype">GetType</a>
</td>
<td align="left" width="63%">
Retrieves the operations supported by the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice-getversion">GetVersion</a>
</td>
<td align="left" width="63%">
Retrieves the manufacturer-defined version number of the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice-sendopaquecommand">SendOpaqueCommand</a>
</td>
<td align="left" width="63%">
Sends a device-specific command to the device through Windows Media Device Manager.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice2">IWMDMDevice2 Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice3">IWMDMDevice3 Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/WMDM/interfaces-for-applications">Interfaces for Applications</a>
 

 

