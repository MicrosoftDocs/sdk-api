---
UID: NN:upnp.IUPnPDevice
title: IUPnPDevice
author: windows-sdk-content
description: The IUPnPDevice interface enables an application to retrieve information about a specific device.
old-location: upnp\iupnpdevice.htm
old-project: UPnP
ms.assetid: 566cc606-3dfb-4052-93b0-3c922bf30f84
ms.author: windowssdkdev
ms.date: 04/25/2018
ms.keywords: IUPnPDevice, IUPnPDevice interface [UPnP APIs], IUPnPDevice interface [UPnP APIs],described, _upnp_iupnpdevice, upnp.iupnpdevice, upnp/IUPnPDevice
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: upnp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: None supported
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
req.typenames: UI_EVENTPARAMS_COMMAND
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Upnp.dll
api_name:
-	IUPnPDevice
product: Windows
targetos: Windows
req.lib: 
req.dll: Upnp.dll
req.irql: 
req.product: Windows UI
---

# IUPnPDevice interface


## -description


The 
<b>IUPnPDevice</b> interface enables an application to retrieve information about a specific device.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUPnPDevice</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>IUPnPDevice</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IUPnPDevice</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/17b3d4f1-a51a-42f9-8fc0-4156d4975889">IconURL</a>
</td>
<td align="left" width="63%">
Returns a URL from which an icon of the specified format can be loaded.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUPnPDevice</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/a8cdc66f-c5c0-4328-a8f2-f40d55a20a4f">Children</a>


</td>
<td align="left" width="63%">
Child devices of the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/library/windows/hardware/dn915161">Description</a>


</td>
<td align="left" width="63%">
Human-readable form of the summary of a device's functionality.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/dd24384f-2657-4cb0-812e-1b51d53b73de">FriendlyName</a>


</td>
<td align="left" width="63%">
Device display name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/18a7c7e0-389d-4fc4-b98c-4eb1afea4a7e">HasChildren</a>


</td>
<td align="left" width="63%">
Indicates whether the device has any child devices.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/0416c4f0-1289-4e91-be34-23f8b80df5c3">IsRootDevice</a>


</td>
<td align="left" width="63%">
Indicates whether the device is the top-most device in the device tree.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/b62ba17d-4d0f-4609-ae34-0d8bd350f761">ManufacturerName</a>


</td>
<td align="left" width="63%">
Human-readable form of the manufacturer name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/7019716a-4a64-43cd-bb44-21bdb6b022c2">ManufacturerURL</a>


</td>
<td align="left" width="63%">
URL for the manufacturer's Web site.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/library/windows/hardware/ff549311">ModelName</a>


</td>
<td align="left" width="63%">
Human-readable form of the model name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/library/windows/hardware/ff549321">ModelNumber</a>


</td>
<td align="left" width="63%">
Human-readable form of the model number.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/e9f3231a-5836-4629-9df5-6ed9184fb753">ModelURL</a>


</td>
<td align="left" width="63%">
URL for a Web page that contains model-specific information.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/662a0bda-32f5-4756-8851-e7b2d0b9cc44">ParentDevice</a>


</td>
<td align="left" width="63%">
Parent of the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/8dba8289-2f2f-482c-abd6-38f81a11f5e2">PresentationURL</a>


</td>
<td align="left" width="63%">
Presentation URL for a Web page that can be used to control the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/library/windows/hardware/hh406413">RootDevice</a>


</td>
<td align="left" width="63%">
Top-most device in the device tree.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/de2f8594-a183-440a-aeb1-240cf0709e36">SerialNumber</a>


</td>
<td align="left" width="63%">
Human-readable form of the serial number.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/library/windows/hardware/dn926947">Services</a>


</td>
<td align="left" width="63%">
List of services provided by the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/library/windows/hardware/hh439450">Type</a>


</td>
<td align="left" width="63%">
 Uniform resource identifier (URI) for the device type.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/ca644bd3-6580-44da-87f5-11d543814043">UniqueDeviceName</a>


</td>
<td align="left" width="63%">
Unique device name (UDN) of the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/33349885-96da-47ef-9b09-83c2c332b509">UPC</a>


</td>
<td align="left" width="63%">
Human-readable form of the product code.

</td>
</tr>
</table> 

