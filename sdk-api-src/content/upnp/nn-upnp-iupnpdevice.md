---
UID: NN:upnp.IUPnPDevice
title: IUPnPDevice (upnp.h)
author: windows-sdk-content
description: The IUPnPDevice interface enables an application to retrieve information about a specific device.
old-location: upnp\iupnpdevice.htm
tech.root: upnp
ms.assetid: 566cc606-3dfb-4052-93b0-3c922bf30f84
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IUPnPDevice, IUPnPDevice interface [UPnP APIs], IUPnPDevice interface [UPnP APIs],described, _upnp_iupnpdevice, upnp.iupnpdevice, upnp/IUPnPDevice
ms.topic: interface
f1_keywords: ["upnp/IUPnPDevice"]
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
req.lib: 
req.dll: Upnp.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Upnp.dll
api_name:
 - IUPnPDevice
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IUPnPDevice interface


## -description


The 
<b>IUPnPDevice</b> interface enables an application to retrieve information about a specific device.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUPnPDevice</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IUPnPDevice</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/upnp/nf-upnp-iupnpdevice-iconurl">IconURL</a>
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

<a href="https://docs.microsoft.com/windows/desktop/api/upnp/nf-upnp-iupnpdevice-get_children">Children</a>


</td>
<td align="left" width="63%">
Child devices of the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/upnp/nf-upnp-iupnpdevice-get_description">Description</a>


</td>
<td align="left" width="63%">
Human-readable form of the summary of a device's functionality.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/upnp/nf-upnp-iupnpdevice-get_friendlyname">FriendlyName</a>


</td>
<td align="left" width="63%">
Device display name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/upnp/nf-upnp-iupnpdevice-get_haschildren">HasChildren</a>


</td>
<td align="left" width="63%">
Indicates whether the device has any child devices.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/upnp/nf-upnp-iupnpdevice-get_isrootdevice">IsRootDevice</a>


</td>
<td align="left" width="63%">
Indicates whether the device is the top-most device in the device tree.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/upnp/nf-upnp-iupnpdevice-get_manufacturername">ManufacturerName</a>


</td>
<td align="left" width="63%">
Human-readable form of the manufacturer name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/upnp/nf-upnp-iupnpdevice-get_manufacturerurl">ManufacturerURL</a>


</td>
<td align="left" width="63%">
URL for the manufacturer's Web site.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/upnp/nf-upnp-iupnpdevice-get_modelname">ModelName</a>


</td>
<td align="left" width="63%">
Human-readable form of the model name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/upnp/nf-upnp-iupnpdevice-get_modelnumber">ModelNumber</a>


</td>
<td align="left" width="63%">
Human-readable form of the model number.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/upnp/nf-upnp-iupnpdevice-get_modelurl">ModelURL</a>


</td>
<td align="left" width="63%">
URL for a Web page that contains model-specific information.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/upnp/nf-upnp-iupnpdevice-get_parentdevice">ParentDevice</a>


</td>
<td align="left" width="63%">
Parent of the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/upnp/nf-upnp-iupnpdevice-get_presentationurl">PresentationURL</a>


</td>
<td align="left" width="63%">
Presentation URL for a Web page that can be used to control the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/upnp/nf-upnp-iupnpdevice-get_rootdevice">RootDevice</a>


</td>
<td align="left" width="63%">
Top-most device in the device tree.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/upnp/nf-upnp-iupnpdevice-get_serialnumber">SerialNumber</a>


</td>
<td align="left" width="63%">
Human-readable form of the serial number.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/upnp/nf-upnp-iupnpdevice-get_services">Services</a>


</td>
<td align="left" width="63%">
List of services provided by the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/upnp/nf-upnp-iupnpdevice-get_type">Type</a>


</td>
<td align="left" width="63%">
 Uniform resource identifier (URI) for the device type.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/upnp/nf-upnp-iupnpdevice-get_uniquedevicename">UniqueDeviceName</a>


</td>
<td align="left" width="63%">
Unique device name (UDN) of the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/upnp/nf-upnp-iupnpdevice-get_upc">UPC</a>


</td>
<td align="left" width="63%">
Human-readable form of the product code.

</td>
</tr>
</table> 

