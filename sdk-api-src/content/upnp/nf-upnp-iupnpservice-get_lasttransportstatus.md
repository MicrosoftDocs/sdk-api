---
UID: NF:upnp.IUPnPService.get_LastTransportStatus
title: IUPnPService::get_LastTransportStatus (upnp.h)
description: For queries related to evented variables, the LastTransportStatus property specifies the HTTP status of the last IUPnPService::InvokeAction operation.
helpviewer_keywords: ["IUPnPService interface [UPnP APIs]","get_LastTransportStatus method","IUPnPService.get_LastTransportStatus","IUPnPService::get_LastTransportStatus","_upnp_iupnpservice_lasttransportstatus","get_LastTransportStatus","get_LastTransportStatus method [UPnP APIs]","get_LastTransportStatus method [UPnP APIs]","IUPnPService interface","upnp.iupnpservice_lasttransportstatus","upnp/IUPnPService::get_LastTransportStatus"]
old-location: upnp\iupnpservice_lasttransportstatus.htm
tech.root: upnp
ms.assetid: 8593b800-ae0a-41b8-9a61-92bdfc106c8b
ms.date: 12/05/2018
ms.keywords: IUPnPService interface [UPnP APIs],get_LastTransportStatus method, IUPnPService.get_LastTransportStatus, IUPnPService::get_LastTransportStatus, _upnp_iupnpservice_lasttransportstatus, get_LastTransportStatus, get_LastTransportStatus method [UPnP APIs], get_LastTransportStatus method [UPnP APIs],IUPnPService interface, upnp.iupnpservice_lasttransportstatus, upnp/IUPnPService::get_LastTransportStatus
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
 - IUPnPService::get_LastTransportStatus
 - upnp/IUPnPService::get_LastTransportStatus
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
 - IUPnPService.get_LastTransportStatus
---

# IUPnPService::get_LastTransportStatus


## -description

For queries related to evented variables, the 
<b>LastTransportStatus</b> property specifies the HTTP status of the last 
<a href="/windows/desktop/api/upnp/nf-upnp-iupnpservice-invokeaction">IUPnPService::InvokeAction</a> operation. For queries related to non-evented variables, the 
<b>LastTransportStatus</b> property specifies the last 
<a href="/windows/desktop/api/upnp/nf-upnp-iupnpservice-querystatevariable">IUPnPService::QueryStateVariable</a> operation, if the caller invoked a query for a non-evented variable.

## -parameters

### -param plValue [out]

Receives a reference to the status. If <i>plValue</i> is the HTTP status 200, the operation was successful.

## -returns

For C++: If this property's "get" method succeeds, the return value is S_OK. Otherwise, the method returns one of the COM error codes defined in WinError.h.

## -see-also

<a href="/windows/desktop/api/upnp/nn-upnp-iupnpservice">IUPnPService</a>