---
UID: NF:upnp.IUPnPDevice.get_Services
title: IUPnPDevice::get_Services (upnp.h)
description: The Services property specifies the list of services provided by the device.
helpviewer_keywords: ["IUPnPDevice interface [UPnP APIs]","get_Services method","IUPnPDevice.get_Services","IUPnPDevice::get_Services","_upnp_iupnpdevice_services","get_Services","get_Services method [UPnP APIs]","get_Services method [UPnP APIs]","IUPnPDevice interface","upnp.iupnpdevice_services","upnp/IUPnPDevice::get_Services"]
old-location: upnp\iupnpdevice_services.htm
tech.root: upnp
ms.assetid: 3b854a5a-a0a9-4236-83c1-98b3671bfc74
ms.date: 12/05/2018
ms.keywords: IUPnPDevice interface [UPnP APIs],get_Services method, IUPnPDevice.get_Services, IUPnPDevice::get_Services, _upnp_iupnpdevice_services, get_Services, get_Services method [UPnP APIs], get_Services method [UPnP APIs],IUPnPDevice interface, upnp.iupnpdevice_services, upnp/IUPnPDevice::get_Services
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
 - IUPnPDevice::get_Services
 - upnp/IUPnPDevice::get_Services
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
 - IUPnPDevice.get_Services
---

# IUPnPDevice::get_Services


## -description

The 
<b>Services</b> property specifies the list of services provided by the device.

## -parameters

### -param ppusServices [out]

Receives a reference to an 
<a href="/windows/desktop/api/upnp/nn-upnp-iupnpservices">IUPnPServices</a> collection that enumerates the services provided by the device. This reference must be released when it is no longer required.

## -returns

For C++: If this property's "get" method succeeds, the return value is S_OK. Otherwise, the method returns one of the COM error codes defined in WinError.h.

## -see-also

<a href="/windows/desktop/api/upnp/nn-upnp-iupnpdevice">IUPnPDevice</a>



<a href="/windows/desktop/api/upnp/nn-upnp-iupnpservices">IUPnPServices</a>