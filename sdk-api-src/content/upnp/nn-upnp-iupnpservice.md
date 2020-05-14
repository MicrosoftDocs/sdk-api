---
UID: NN:upnp.IUPnPService
title: IUPnPService (upnp.h)
description: The IUPnPService interface enables an application to query state variables and invoke actions on an instance of a service.helpviewer_keywords: ["IUPnPService","IUPnPService interface [UPnP APIs]","IUPnPService interface [UPnP APIs]","described","_upnp_iupnpservice","upnp.iupnpservice","upnp/IUPnPService"]
old-location: upnp\iupnpservice.htm
tech.root: upnp
ms.assetid: 48b20b03-62a4-4dcd-8eda-f1bfef1eef38
ms.date: 12/05/2018
ms.keywords: IUPnPService, IUPnPService interface [UPnP APIs], IUPnPService interface [UPnP APIs],described, _upnp_iupnpservice, upnp.iupnpservice, upnp/IUPnPService
f1_keywords:
- upnp/IUPnPService
dev_langs:
- c++
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
- IUPnPService
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IUPnPService interface


## -description


The 
<b>IUPnPService</b> interface enables an application to query state variables and invoke actions on an instance of a service.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUPnPService</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IUPnPService</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IUPnPService</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/upnp/nf-upnp-iupnpservice-addcallback">AddCallback</a>
</td>
<td align="left" width="63%">
Registers a service callback.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/upnp/nf-upnp-iupnpservice-invokeaction">InvokeAction</a>
</td>
<td align="left" width="63%">
Invokes the specified action.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/upnp/nf-upnp-iupnpservice-querystatevariable">QueryStateVariable</a>
</td>
<td align="left" width="63%">
Returns the value of the specified state variable.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUPnPService</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/upnp/nf-upnp-iupnpservice-get_id">Id</a>


</td>
<td align="left" width="63%">
Service ID for the service.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/upnp/nf-upnp-iupnpservice-get_lasttransportstatus">LastTransportStatus</a>


</td>
<td align="left" width="63%">
HTTP status of the last request sent to the service on the device. The request is either to invoke an action or query the value of a non-evented state variable.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/upnp/nf-upnp-iupnpservice-get_servicetypeidentifier">ServiceTypeIdentifier</a>


</td>
<td align="left" width="63%">
Service type identifier for the service.

</td>
</tr>
</table> 

