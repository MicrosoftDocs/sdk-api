---
UID: NF:upnp.IUPnPDevices.get_Item
title: IUPnPDevices::get_Item (upnp.h)
description: The Item property specifies the IUPnPDevice interface for a device, identified by the UDN, in the collection.
helpviewer_keywords: ["IUPnPDevices interface [UPnP APIs]","get_Item method","IUPnPDevices.get_Item","IUPnPDevices::get_Item","_upnp_iupnpdevices_item","get_Item","get_Item method [UPnP APIs]","get_Item method [UPnP APIs]","IUPnPDevices interface","upnp.iupnpdevices_item","upnp/IUPnPDevices::get_Item"]
old-location: upnp\iupnpdevices_item.htm
tech.root: upnp
ms.assetid: 38648c9c-6d5a-4215-9270-fd1f893fa360
ms.date: 12/05/2018
ms.keywords: IUPnPDevices interface [UPnP APIs],get_Item method, IUPnPDevices.get_Item, IUPnPDevices::get_Item, _upnp_iupnpdevices_item, get_Item, get_Item method [UPnP APIs], get_Item method [UPnP APIs],IUPnPDevices interface, upnp.iupnpdevices_item, upnp/IUPnPDevices::get_Item
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
 - IUPnPDevices::get_Item
 - upnp/IUPnPDevices::get_Item
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
 - IUPnPDevices.get_Item
---

# IUPnPDevices::get_Item


## -description

The 
<b>Item</b> property specifies the <a href="/windows/desktop/api/upnp/nn-upnp-iupnpdevice">IUPnPDevice</a> interface for a  device, identified by the UDN, in the collection.

## -parameters

### -param bstrUDN [in]

Specifies a device in the collection.

### -param ppDevice [out]

Receives a reference to an 
<a href="/windows/desktop/api/upnp/nn-upnp-iupnpdevice">IUPnPDevice</a> interface for the specified device.

## -returns

For C++: If this property's "get" method succeeds, the return value is S_OK. Otherwise, the method returns one of the COM error codes defined in WinError.h.

## -see-also

<a href="/windows/desktop/api/upnp/nn-upnp-iupnpdevices">IUPnPDevices</a>