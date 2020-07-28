---
UID: NN:upnp.IUPnPServiceEnumProperty
title: IUPnPServiceEnumProperty (upnp.h)
description: Use this interface to delay Service Control Protocol Description (SCPD) download and event subscription on the IUPnPService objects enumerated from the IUPnPServices object.
helpviewer_keywords: ["IUPnPServiceEnumProperty","IUPnPServiceEnumProperty interface [UPnP APIs]","IUPnPServiceEnumProperty interface [UPnP APIs]","described","upnp.iupnpserviceenumproperty","upnp/IUPnPServiceEnumProperty"]
old-location: upnp\iupnpserviceenumproperty.htm
tech.root: upnp
ms.assetid: B63CCE08-548F-44D3-BAE3-84E4358F25AD
ms.date: 12/05/2018
ms.keywords: IUPnPServiceEnumProperty, IUPnPServiceEnumProperty interface [UPnP APIs], IUPnPServiceEnumProperty interface [UPnP APIs],described, upnp.iupnpserviceenumproperty, upnp/IUPnPServiceEnumProperty
f1_keywords:
- upnp/IUPnPServiceEnumProperty
dev_langs:
- c++
req.header: upnp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
- IUPnPServiceEnumProperty
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IUPnPServiceEnumProperty interface


## -description


Use this interface to delay Service Control Protocol Description (SCPD) download and event subscription on the <a href="https://docs.microsoft.com/windows/desktop/api/upnp/nn-upnp-iupnpservice">IUPnPService</a> objects enumerated from the <a href="https://docs.microsoft.com/windows/desktop/api/upnp/nn-upnp-iupnpservices">IUPnPServices</a> object.

This interface can be obtained through a <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">QueryInterface</a> off the <a href="https://docs.microsoft.com/windows/desktop/api/upnp/nn-upnp-iupnpservices">IUPnPServices</a> object.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUPnPServiceEnumProperty</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IUPnPServiceEnumProperty</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IUPnPServiceEnumProperty</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/upnp/nf-upnp-iupnpserviceenumproperty-setserviceenumproperty">SetServiceEnumProperty</a>
</td>
<td align="left" width="63%">
Sets the flag that indicates  opt-in to the delayed SCPD download and event subscription. 

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/upnp/nn-upnp-iupnpserviceasync">IUPnPServiceAsync</a>
 

 

