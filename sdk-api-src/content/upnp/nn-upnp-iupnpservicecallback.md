---
UID: NN:upnp.IUPnPServiceCallback
title: IUPnPServiceCallback (upnp.h)
description: The IUPnPServiceCallback interface is used to send event notifications to clients of Service objects.
old-location: upnp\iupnpservicecallback.htm
tech.root: upnp
ms.assetid: 44515be4-891b-4f3d-a2c2-1699e468e708
ms.date: 12/05/2018
ms.keywords: IUPnPServiceCallback, IUPnPServiceCallback interface [UPnP APIs], IUPnPServiceCallback interface [UPnP APIs],described, _upnp_iupnpservicecallback, upnp.iupnpservicecallback, upnp/IUPnPServiceCallback
ms.topic: interface
f1_keywords:
- upnp/IUPnPServiceCallback
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
- IUPnPServiceCallback
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IUPnPServiceCallback interface


## -description


The 
<b>IUPnPServiceCallback</b> interface is used to send event notifications to clients of Service objects.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUPnPServiceCallback</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IUPnPServiceCallback</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IUPnPServiceCallback</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/upnp/nf-upnp-iupnpservicecallback-serviceinstancedied">ServiceInstanceDied</a>
</td>
<td align="left" width="63%">
Method that indicates that a service will no longer be sending events.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/upnp/nf-upnp-iupnpservicecallback-statevariablechanged">StateVariableChanged</a>
</td>
<td align="left" width="63%">
Method that indicates that a state variable has changed.

</td>
</tr>
</table> 

