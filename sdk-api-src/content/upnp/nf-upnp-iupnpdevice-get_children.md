---
UID: NF:upnp.IUPnPDevice.get_Children
title: IUPnPDevice::get_Children (upnp.h)
description: The Children property specifies all the child devices of the device. The devices are stored in an IUPnPDevices collection.
helpviewer_keywords: ["IUPnPDevice interface [UPnP APIs]","get_Children method","IUPnPDevice.get_Children","IUPnPDevice::get_Children","_upnp_iupnpdevice_children","get_Children","get_Children method [UPnP APIs]","get_Children method [UPnP APIs]","IUPnPDevice interface","upnp.iupnpdevice_children","upnp/IUPnPDevice::get_Children"]
old-location: upnp\iupnpdevice_children.htm
tech.root: upnp
ms.assetid: a8cdc66f-c5c0-4328-a8f2-f40d55a20a4f
ms.date: 12/05/2018
ms.keywords: IUPnPDevice interface [UPnP APIs],get_Children method, IUPnPDevice.get_Children, IUPnPDevice::get_Children, _upnp_iupnpdevice_children, get_Children, get_Children method [UPnP APIs], get_Children method [UPnP APIs],IUPnPDevice interface, upnp.iupnpdevice_children, upnp/IUPnPDevice::get_Children
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
 - IUPnPDevice::get_Children
 - upnp/IUPnPDevice::get_Children
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
 - IUPnPDevice.get_Children
---

# IUPnPDevice::get_Children


## -description

The 
<b>Children</b> property specifies all the child devices of the device. The devices are stored in an 
<a href="/windows/desktop/api/upnp/nn-upnp-iupnpdevices">IUPnPDevices</a> collection.

## -parameters

### -param ppudChildren [out]

Receives a reference to an 
<a href="/windows/desktop/api/upnp/nn-upnp-iupnpdevices">IUPnPDevices</a> collection that enumerates the child devices of the device. This reference must be released when it is no longer required. 




If the device has no child devices, the collection object has a length of zero.

## -returns

For C++: If this property's "get" method succeeds, the return value is S_OK. Otherwise, the method returns one of the COM error codes defined in WinError.h.

## -remarks

To determine if a device has any children (but not the actual number of children), use <a href="/windows/desktop/api/upnp/nf-upnp-iupnpdevice-get_haschildren">IUPnPDevice::HasChildren</a>.

## -see-also

<a href="/windows/desktop/api/upnp/nn-upnp-iupnpdevice">IUPnPDevice</a>



<a href="/windows/desktop/api/upnp/nf-upnp-iupnpdevice-get_haschildren">IUPnPDevice::HasChildren</a>



<a href="/windows/desktop/api/upnp/nn-upnp-iupnpdevices">IUPnPDevices</a>