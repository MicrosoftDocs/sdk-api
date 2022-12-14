---
UID: NN:upnp.IUPnPDeviceFinderAddCallbackWithInterface
title: IUPnPDeviceFinderAddCallbackWithInterface (upnp.h)
description: The IUPnPDeviceFinderAddCallbackWithInterface interface allows the UPnP framework to communicate to an application
helpviewer_keywords: ["IUPnPDeviceFinderAddCallbackWithInterface","IUPnPDeviceFinderAddCallbackWithInterface interface [UPnP APIs]","IUPnPDeviceFinderAddCallbackWithInterface interface [UPnP APIs]","described","upnp.iupnpdevicefinderaddcallbackwithinterface","upnp/IUPnPDeviceFinderAddCallbackWithInterface"]
old-location: upnp\iupnpdevicefinderaddcallbackwithinterface.htm
tech.root: upnp
ms.assetid: b0d78121-35d0-4f33-b1e9-19e0b2c5b78f
ms.date: 12/05/2018
ms.keywords: IUPnPDeviceFinderAddCallbackWithInterface, IUPnPDeviceFinderAddCallbackWithInterface interface [UPnP APIs], IUPnPDeviceFinderAddCallbackWithInterface interface [UPnP APIs],described, upnp.iupnpdevicefinderaddcallbackwithinterface, upnp/IUPnPDeviceFinderAddCallbackWithInterface
req.header: upnp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
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
 - IUPnPDeviceFinderAddCallbackWithInterface
 - upnp/IUPnPDeviceFinderAddCallbackWithInterface
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
 - IUPnPDeviceFinderAddCallbackWithInterface
---

# IUPnPDeviceFinderAddCallbackWithInterface interface


## -description

The <b>IUPnPDeviceFinderAddCallbackWithInterface</b> interface allows the UPnP framework to communicate to an application:

<ul>
<li>The devices found during an asynchronous search.</li>
<li>The network interface through which the device advertisement came.</li>
</ul>

## -inheritance

The <b>IUPnPDeviceFinderAddCallbackWithInterface</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IUPnPDeviceFinderAddCallbackWithInterface</b> also has these types of members:

## -remarks

If you implement this interface, you must also implement the <a href="/windows/desktop/api/upnp/nn-upnp-iupnpdevicefindercallback">IUPnPDeviceFinderCallback</a> interface.

## -see-also

<a href="/windows/desktop/api/upnp/nn-upnp-iupnpdevicefindercallback">IUPnPDeviceFinderCallback</a>
