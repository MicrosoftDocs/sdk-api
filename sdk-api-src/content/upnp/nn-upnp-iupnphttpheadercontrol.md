---
UID: NN:upnp.IUPnPHttpHeaderControl
title: IUPnPHttpHeaderControl (upnp.h)
description: Enables the caller to specify additional HTTP headers sent in HTTP requests to a device.
helpviewer_keywords: ["IUPnPHttpHeaderControl","IUPnPHttpHeaderControl interface [UPnP APIs]","IUPnPHttpHeaderControl interface [UPnP APIs]","described","upnp.iupnphttpheadercontrol","upnp/IUPnPHttpHeaderControl"]
old-location: upnp\iupnphttpheadercontrol.htm
tech.root: upnp
ms.assetid: aed33117-9bfd-4a23-998f-4b8d040d6e3b
ms.date: 12/05/2018
ms.keywords: IUPnPHttpHeaderControl, IUPnPHttpHeaderControl interface [UPnP APIs], IUPnPHttpHeaderControl interface [UPnP APIs],described, upnp.iupnphttpheadercontrol, upnp/IUPnPHttpHeaderControl
req.header: upnp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
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
 - IUPnPHttpHeaderControl
 - upnp/IUPnPHttpHeaderControl
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
 - IUPnPHttpHeaderControl
---

# IUPnPHttpHeaderControl interface


## -description

The <b>IUPnPHttpHeaderControl</b> interface enables the caller to specify additional HTTP headers sent in HTTP requests to a device.

## -inheritance

The <b>IUPnPHttpHeaderControl</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IUPnPHttpHeaderControl</b> also has these types of members:

## -remarks

This interface is obtained by calling QueryInterface on the same object that provides an implementation of the <a href="/windows/desktop/api/upnp/nn-upnp-iupnpdevicefinder">IUPnPDeviceFinder</a> or <a href="/windows/desktop/api/upnp/nn-upnp-iupnpdescriptiondocument">IUPnPDescriptionDocument</a> interfaces, after which <a href="/windows/desktop/api/upnp/nf-upnp-iupnphttpheadercontrol-addrequestheaders">AddRequestHeaders</a> can be called on it.

## -see-also

<a href="/windows/desktop/UPnP/control-point-api-with-upnp-technology-reference">Control Point API Reference</a>



<a href="/windows/desktop/api/upnp/nn-upnp-iupnpdescriptiondocument">IUPnPDescriptionDocument</a>



<a href="/windows/desktop/api/upnp/nn-upnp-iupnpdevicefinder">IUPnPDeviceFinder</a>
