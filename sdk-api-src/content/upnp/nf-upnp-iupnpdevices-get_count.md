---
UID: NF:upnp.IUPnPDevices.get_Count
title: IUPnPDevices::get_Count (upnp.h)
description: The Count property specifies the number of devices in the collection.
helpviewer_keywords: ["IUPnPDevices interface [UPnP APIs]","get_Count method","IUPnPDevices.get_Count","IUPnPDevices::get_Count","_upnp_iupnpdevices_count","get_Count","get_Count method [UPnP APIs]","get_Count method [UPnP APIs]","IUPnPDevices interface","upnp.iupnpdevices_count","upnp/IUPnPDevices::get_Count"]
old-location: upnp\iupnpdevices_count.htm
tech.root: upnp
ms.assetid: 1a3e3b65-b147-41e7-a5df-7424613b50f6
ms.date: 12/05/2018
ms.keywords: IUPnPDevices interface [UPnP APIs],get_Count method, IUPnPDevices.get_Count, IUPnPDevices::get_Count, _upnp_iupnpdevices_count, get_Count, get_Count method [UPnP APIs], get_Count method [UPnP APIs],IUPnPDevices interface, upnp.iupnpdevices_count, upnp/IUPnPDevices::get_Count
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
 - IUPnPDevices::get_Count
 - upnp/IUPnPDevices::get_Count
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
 - IUPnPDevices.get_Count
---

# IUPnPDevices::get_Count


## -description

The 
<b>Count</b> property specifies the number of devices in the collection.

## -parameters

### -param plCount [out]

Receives a reference to the number of devices in the collection.

## -returns

For C++: If this property's "get" method succeeds, the return value is S_OK. Otherwise, the method returns one of the COM error codes defined in WinError.h.

## -see-also

<a href="/windows/desktop/api/upnp/nn-upnp-iupnpdevices">IUPnPDevices</a>