---
UID: NF:upnp.IUPnPService.get_ServiceTypeIdentifier
title: IUPnPService::get_ServiceTypeIdentifier (upnp.h)
description: The ServiceTypeIdentifier property specifies the service type identifier for the device.
helpviewer_keywords: ["IUPnPService interface [UPnP APIs]","get_ServiceTypeIdentifier method","IUPnPService.get_ServiceTypeIdentifier","IUPnPService::get_ServiceTypeIdentifier","_upnp_iupnpservice_servicetypeidentifier","get_ServiceTypeIdentifier","get_ServiceTypeIdentifier method [UPnP APIs]","get_ServiceTypeIdentifier method [UPnP APIs]","IUPnPService interface","upnp.iupnpservice_servicetypeidentifier","upnp/IUPnPService::get_ServiceTypeIdentifier"]
old-location: upnp\iupnpservice_servicetypeidentifier.htm
tech.root: upnp
ms.assetid: 440344c9-b229-421b-b8a7-76f2f98c2c6b
ms.date: 12/05/2018
ms.keywords: IUPnPService interface [UPnP APIs],get_ServiceTypeIdentifier method, IUPnPService.get_ServiceTypeIdentifier, IUPnPService::get_ServiceTypeIdentifier, _upnp_iupnpservice_servicetypeidentifier, get_ServiceTypeIdentifier, get_ServiceTypeIdentifier method [UPnP APIs], get_ServiceTypeIdentifier method [UPnP APIs],IUPnPService interface, upnp.iupnpservice_servicetypeidentifier, upnp/IUPnPService::get_ServiceTypeIdentifier
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
 - IUPnPService::get_ServiceTypeIdentifier
 - upnp/IUPnPService::get_ServiceTypeIdentifier
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
 - IUPnPService.get_ServiceTypeIdentifier
---

# IUPnPService::get_ServiceTypeIdentifier


## -description

The 
<b>ServiceTypeIdentifier</b> property specifies the service type identifier for the device.

## -parameters

### -param pVal [out]

Receives a reference to a string that contains the service type identifier. Release this string with <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a> when it is no longer required.

## -returns

For C++: If this property's "get" method succeeds, the return value is S_OK. Otherwise, the method returns one of the COM error codes defined in WinError.h.

## -see-also

<a href="/windows/desktop/api/upnp/nn-upnp-iupnpservice">IUPnPService</a>