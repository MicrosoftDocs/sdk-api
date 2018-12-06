---
UID: NN:mbnapi.IMbnDeviceService
title: IMbnDeviceService
author: windows-sdk-content
description: Allows for communicating with a device service on a particular Mobile Broadband device.
old-location: mbn\imbndeviceservice.htm
tech.root: mbn
ms.assetid: 5C587408-DF03-4123-BA5A-C2CCC378F60A
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IMbnDeviceService, IMbnDeviceService interface [Microsoft Broadband Networks], IMbnDeviceService interface [Microsoft Broadband Networks],described, mbn.imbndeviceservice, mbnapi/IMbnDeviceService
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMbnDeviceService interface


## -description


Allows for communicating with a device service on a particular Mobile Broadband device.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMbnDeviceService</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMbnDeviceService</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/B0066062-0F10-49B8-85CC-0658757BF52B">CloseCommandSession</a>
</td>
<td align="left" width="63%">
Closes a command session to a device service on a Mobile Broadband device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/E00322FC-05DF-4342-A182-E1F4F40FBD60">CloseDataSession</a>
</td>
<td align="left" width="63%">
Closes the data session to a device service on a Mobile Broadband device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/EC4FF42D-EFE9-432C-997F-426B2187BBBE">OpenCommandSession</a>
</td>
<td align="left" width="63%">
Opens a command session to a device service on a Mobile Broadband device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/A26EBECA-4390-4BB2-88CD-EE2356E44E3A">OpenDataSession</a>
</td>
<td align="left" width="63%">
Open a data session to the device service on a Mobile Broadband device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/EA68206E-5656-4C83-AFB0-26E7F3692DE2">QueryCommand</a>
</td>
<td align="left" width="63%">
Sends a <b>QUERY</b> control command to the device service of a Mobile Broadband device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/E82AAD40-1E91-449D-8F1C-CE31B394B2DF">QuerySupportedCommands</a>
</td>
<td align="left" width="63%">
Gets the list of commands IDs supported by the Mobile Broadband device service.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/DA45B319-4E6A-4999-85A7-7F5A4F9BED7B">SetCommand</a>
</td>
<td align="left" width="63%">
Sends a <b>SET</b> control command to the device service of a Mobile Broadband device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/D2CD630B-FCD5-485D-84A6-B2A942842A1F">WriteData</a>
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

<a href="https://msdn.microsoft.com/3AE6D7A6-3974-4517-AEB6-992CAC543247">DeviceServiceID</a>


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

<a href="https://msdn.microsoft.com/3789F9FA-703E-486D-8B4E-AE4128DE705B">InterfaceID</a>


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

<a href="https://msdn.microsoft.com/7A986AD8-9DC3-4543-8FB9-5F633DEC95C7">IsCommandSessionOpen</a>


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

<a href="https://msdn.microsoft.com/97F58FC5-D960-4EBA-8441-12472F2771DE">IsDataSessionOpen</a>


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




<a href="IMbnDeviceService">IMbnDeviceService</a> objects are provided by a call to the <a href="https://msdn.microsoft.com/293E9BE5-AD7D-41B7-9A27-E964EE745183">GetDeviceService</a> method of the <a href="https://msdn.microsoft.com/0B97FCCD-0A90-4FA2-9122-B00BD3F1A033">IMbnDeviceServicesContext</a> interface.



