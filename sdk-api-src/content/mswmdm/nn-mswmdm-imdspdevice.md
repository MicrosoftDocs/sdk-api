---
UID: NN:mswmdm.IMDSPDevice
title: IMDSPDevice (mswmdm.h)
author: windows-sdk-content
description: The IMDSPDevice interface provides an instance-based association with a media device.
old-location: wmdm\imdspdevice.htm
tech.root: WMDM
ms.assetid: 98f16547-4d8a-4422-ba08-c3c678142492
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IMDSPDevice, IMDSPDevice interface [windows Media Device Manager], IMDSPDevice interface [windows Media Device Manager],described, IMDSPDeviceInterface, mswmdm/IMDSPDevice, wmdm.imdspdevice
ms.topic: interface
f1_keywords: 
 - "mswmdm/IMDSPDevice"
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
 - IMDSPDevice
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMDSPDevice interface


## -description



The <b>IMDSPDevice</b> interface provides an instance-based association with a media device. Using this interface, the client can get a storage media enumerator for the device, get information about the device, and send opaque (pass-through) commands to the device. <a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nn-mswmdm-imdserviceprovider2">IMDServiceProvider2</a> extends <b>IMDSPDevice</b> by providing methods for getting video formats, getting Plug and Play (PnP) device names, enabling the use of property pages, and making it possible to get a pointer to a storage medium from its name. This interface is optional for the service provider but is recommended.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMDSPDevice</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMDSPDevice</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nf-mswmdm-imdspdevice-enumstorage">EnumStorage</a>
</td>
<td align="left" width="63%">
Enumerates the top-level storage medium on the device. This method is mandatory.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nf-mswmdm-imdspdevice-getdeviceicon">GetDeviceIcon</a>
</td>
<td align="left" width="63%">
Retrieves a <b>HICON</b> value that represents the icon that the device service provider indicates must be used to represent this device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nf-mswmdm-imdspdevice-getformatsupport">GetFormatSupport</a>
</td>
<td align="left" width="63%">
Enumerates the formats supported by the device. This method is mandatory.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nf-mswmdm-imdspdevice-getmanufacturer">GetManufacturer</a>
</td>
<td align="left" width="63%">
Retrieves the name of the manufacturer of the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nf-mswmdm-imdspdevice-getname">GetName</a>
</td>
<td align="left" width="63%">
Retrieves the name of the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nf-mswmdm-imdspdevice-getpowersource">GetPowerSource</a>
</td>
<td align="left" width="63%">
Reports whether the device is capable of running on batteries, external power, or both, and on which type of power source it is currently running.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nf-mswmdm-imdspdevice-getserialnumber">GetSerialNumber</a>
</td>
<td align="left" width="63%">
Retrieves the serial number that uniquely identifies the device. This method is mandatory.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nf-mswmdm-imdspdevice-getstatus">GetStatus</a>
</td>
<td align="left" width="63%">
Retrieves the device status information. This method is mandatory.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nf-mswmdm-imdspdevice-gettype">GetType</a>
</td>
<td align="left" width="63%">
Retrieves device type information. This method is mandatory.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nf-mswmdm-imdspdevice-getversion">GetVersion</a>
</td>
<td align="left" width="63%">
Retrieves the version number of the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nf-mswmdm-imdspdevice-sendopaquecommand">SendOpaqueCommand</a>
</td>
<td align="left" width="63%">
Sends a command to a device through Windows Media Device Manager. Windows Media Device Manager transmits the command without acting on it.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nn-mswmdm-imdspdevice2">IMDSPDevice2 Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nn-mswmdm-imdspdevice3">IMDSPDevice3 Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/WMDM/interfaces-for-service-providers">Interfaces for Service Providers</a>
 

 

