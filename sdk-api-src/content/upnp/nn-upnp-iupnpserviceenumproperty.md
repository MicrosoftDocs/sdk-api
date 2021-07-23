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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IUPnPServiceEnumProperty
 - upnp/IUPnPServiceEnumProperty
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
 - IUPnPServiceEnumProperty
---

# IUPnPServiceEnumProperty interface


## -description

Use this interface to delay Service Control Protocol Description (SCPD) download and event subscription on the <a href="/windows/desktop/api/upnp/nn-upnp-iupnpservice">IUPnPService</a> objects enumerated from the <a href="/windows/desktop/api/upnp/nn-upnp-iupnpservices">IUPnPServices</a> object.

This interface can be obtained through a <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">QueryInterface</a> off the <a href="/windows/desktop/api/upnp/nn-upnp-iupnpservices">IUPnPServices</a> object.

## -inheritance

The <b>IUPnPServiceEnumProperty</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IUPnPServiceEnumProperty</b> also has these types of members:

## -see-also

<a href="/windows/desktop/api/upnp/nn-upnp-iupnpserviceasync">IUPnPServiceAsync</a>
