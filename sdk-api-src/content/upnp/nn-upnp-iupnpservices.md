---
UID: NN:upnp.IUPnPServices
title: IUPnPServices (upnp.h)
description: The IUPnPServices interface enumerates a collection of services.
helpviewer_keywords: ["IUPnPServices","IUPnPServices interface [UPnP APIs]","IUPnPServices interface [UPnP APIs]","described","_upnp_iupnpservices","upnp.iupnpservices","upnp/IUPnPServices"]
old-location: upnp\iupnpservices.htm
tech.root: upnp
ms.assetid: 8d5e487f-d2d4-4603-918c-e751d698be3c
ms.date: 12/05/2018
ms.keywords: IUPnPServices, IUPnPServices interface [UPnP APIs], IUPnPServices interface [UPnP APIs],described, _upnp_iupnpservices, upnp.iupnpservices, upnp/IUPnPServices
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
 - IUPnPServices
 - upnp/IUPnPServices
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
 - IUPnPServices
 - IUPnPServices.This interface has no methods.
---

# IUPnPServices interface


## -description

The 
<b>IUPnPServices</b> interface enumerates a collection of services.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUPnPServices</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IUPnPServices</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IUPnPServices</b> interface has these methods.
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
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUPnPServices</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="/windows/desktop/api/upnp/nf-upnp-iupnpservices-get__newenum">_NewEnum</a>


</td>
<td align="left" width="63%">
Enumerator interface for the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="/windows/desktop/api/upnp/nf-upnp-iupnpservices-get_count">Count</a>


</td>
<td align="left" width="63%">
Number of services in the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="/windows/desktop/api/upnp/nf-upnp-iupnpservices-get_item">Item</a>


</td>
<td align="left" width="63%">
An 
<a href="/windows/desktop/api/upnp/nn-upnp-iupnpservice">IUPnPService</a> interface in the collection.

</td>
</tr>
</table>