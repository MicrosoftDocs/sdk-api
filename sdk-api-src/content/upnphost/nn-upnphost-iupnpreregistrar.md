---
UID: NN:upnphost.IUPnPReregistrar
title: IUPnPReregistrar (upnphost.h)
description: The IUPnPReregistrar interface allows the application to re-register a UPnP-based device with the device host.helpviewer_keywords: ["IUPnPReregistrar","IUPnPReregistrar interface [UPnP APIs]","IUPnPReregistrar interface [UPnP APIs]","described","_upnp_iupnpreregistrar","upnp.iupnpreregistrar","upnphost/IUPnPReregistrar"]
old-location: upnp\iupnpreregistrar.htm
tech.root: upnp
ms.assetid: e01f325b-8fbd-43f2-a835-41cd3232f62e
ms.date: 12/05/2018
ms.keywords: IUPnPReregistrar, IUPnPReregistrar interface [UPnP APIs], IUPnPReregistrar interface [UPnP APIs],described, _upnp_iupnpreregistrar, upnp.iupnpreregistrar, upnphost/IUPnPReregistrar
f1_keywords:
- upnphost/IUPnPReregistrar
dev_langs:
- c++
req.header: upnphost.h
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
req.dll: Upnphost.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Upnphost.dll
api_name:
- IUPnPReregistrar
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IUPnPReregistrar interface


## -description


The 
<b>IUPnPReregistrar</b> interface allows the application to re-register a UPnP-based device with the device host.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUPnPReregistrar</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IUPnPReregistrar</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IUPnPReregistrar</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/upnphost/nf-upnphost-iupnpreregistrar-reregisterdevice">ReregisterDevice</a>
</td>
<td align="left" width="63%">
Method that re-registers a non-running device by using the original UDN.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/upnphost/nf-upnphost-iupnpreregistrar-reregisterrunningdevice">ReregisterRunningDevice</a>
</td>
<td align="left" width="63%">
Method that re-registers a running device by using the original UDN.

</td>
</tr>
</table> 

