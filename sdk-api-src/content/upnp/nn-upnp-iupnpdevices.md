---
UID: NN:upnp.IUPnPDevices
title: IUPnPDevices (upnp.h)
description: The IUPnPDevices interface enumerates a collection of devices.
helpviewer_keywords: ["IUPnPDevices","IUPnPDevices interface [UPnP APIs]","IUPnPDevices interface [UPnP APIs]","described","_upnp_iupnpdevices","upnp.iupnpdevices","upnp/IUPnPDevices"]
old-location: upnp\iupnpdevices.htm
tech.root: upnp
ms.assetid: 237715dc-2b5a-45b4-b006-d31c0b4e89e3
ms.date: 12/05/2018
ms.keywords: IUPnPDevices, IUPnPDevices interface [UPnP APIs], IUPnPDevices interface [UPnP APIs],described, _upnp_iupnpdevices, upnp.iupnpdevices, upnp/IUPnPDevices
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IUPnPDevices
 - upnp/IUPnPDevices
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Upnp.dll
api_name:
 - IUPnPDevices
 - IUPnPDevices.This interface has no methods.
---

# IUPnPDevices interface


## -description

The 
<b>IUPnPDevices</b> interface enumerates a collection of devices.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUPnPDevices</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IUPnPDevices</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IUPnPDevices</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">This interface has no methods.</td>
<td align="left" width="63%">
N/A

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUPnPDevices</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="/windows/desktop/api/upnp/nf-upnp-iupnpdevices-get__newenum">_NewEnum</a>


</td>
<td align="left" width="63%">
Enumerator interface for the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="/windows/desktop/api/upnp/nf-upnp-iupnpdevices-get_count">Count</a>


</td>
<td align="left" width="63%">
Number of devices in the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="/windows/desktop/api/upnp/nf-upnp-iupnpdevices-get_item">Item</a>


</td>
<td align="left" width="63%">
An 
<a href="/windows/desktop/api/upnp/nn-upnp-iupnpdevice">IUPnPDevice</a> interface in the collection.

</td>
</tr>
</table>