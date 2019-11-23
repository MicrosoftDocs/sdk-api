---
UID: NN:mbnapi.IMbnDeviceService
title: IMbnDeviceService (mbnapi.h)

description: Allows for communicating with a device service on a particular Mobile Broadband device.
old-location: mbn\imbndeviceservice.htm
tech.root: mbn
ms.assetid: 5C587408-DF03-4123-BA5A-C2CCC378F60A

ms.date: 12/05/2018
ms.keywords: IMbnDeviceService, IMbnDeviceService interface [Microsoft Broadband Networks], IMbnDeviceService interface [Microsoft Broadband Networks],described, mbn.imbndeviceservice, mbnapi/IMbnDeviceService
ms.topic: interface
f1_keywords: 
 - "mbnapi/IMbnDeviceService"
dev_langs:
 - c++
req.header: mbnapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Mbnapi.idl
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
 - mbnapi.h
api_name:
 - IMbnDeviceService
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMbnDeviceService interface


## -description

> [!IMPORTANT]
> Starting in Windows 10, version 1803, the Win32 APIs described in this section are replaced by the Windows Runtime APIs in the [Windows.Networking.Connectivity](/uwp/api/windows.networking.connectivity) namespace.

Allows for communicating with a device service on a particular Mobile Broadband device.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMbnDeviceService</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMbnDeviceService</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IMbnDeviceService</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mbnapi/nf-mbnapi-imbndeviceservice-closecommandsession">CloseCommandSession</a>
</td>
<td align="left" width="63%">
Closes a command session to a device service on a Mobile Broadband device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mbnapi/nf-mbnapi-imbndeviceservice-closedatasession">CloseDataSession</a>
</td>
<td align="left" width="63%">
Closes the data session to a device service on a Mobile Broadband device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mbnapi/nf-mbnapi-imbndeviceservice-opencommandsession">OpenCommandSession</a>
</td>
<td align="left" width="63%">
Opens a command session to a device service on a Mobile Broadband device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mbnapi/nf-mbnapi-imbndeviceservice-opendatasession">OpenDataSession</a>
</td>
<td align="left" width="63%">
Open a data session to the device service on a Mobile Broadband device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mbnapi/nf-mbnapi-imbndeviceservice-querycommand">QueryCommand</a>
</td>
<td align="left" width="63%">
Sends a <b>QUERY</b> control command to the device service of a Mobile Broadband device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mbnapi/nf-mbnapi-imbndeviceservice-querysupportedcommands">QuerySupportedCommands</a>
</td>
<td align="left" width="63%">
Gets the list of commands IDs supported by the Mobile Broadband device service.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mbnapi/nf-mbnapi-imbndeviceservice-setcommand">SetCommand</a>
</td>
<td align="left" width="63%">
Sends a <b>SET</b> control command to the device service of a Mobile Broadband device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mbnapi/nf-mbnapi-imbndeviceservice-writedata">WriteData</a>
</td>
<td align="left" width="63%">
Write data to a device service data session.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMbnDeviceService</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/mbnapi/nf-mbnapi-imbndeviceservice-get_deviceserviceid">DeviceServiceID</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The ID of the device service to which this object is associated.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/mbnapi/nf-mbnapi-imbndeviceservice-get_interfaceid">InterfaceID</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The interface ID of the Mobile Broadband device to which this object is associated.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/mbnapi/nf-mbnapi-imbndeviceservice-get_iscommandsessionopen">IsCommandSessionOpen</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Reports if the device service command session is open.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/mbnapi/nf-mbnapi-imbndeviceservice-get_isdatasessionopen">IsDataSessionOpen</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Reports if the device service data session is open.

</td>
</tr>
</table> 


## -remarks




<a href="https://docs.microsoft.com/windows/desktop/api/mbnapi/nn-mbnapi-imbndeviceservice">IMbnDeviceService</a> objects are provided by a call to the <a href="https://docs.microsoft.com/windows/desktop/api/mbnapi/nf-mbnapi-imbndeviceservicescontext-getdeviceservice">GetDeviceService</a> method of the <a href="https://docs.microsoft.com/windows/desktop/api/mbnapi/nn-mbnapi-imbndeviceservicescontext">IMbnDeviceServicesContext</a> interface.



