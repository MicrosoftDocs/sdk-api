---
UID: NF:upnp.IUPnPDevice.get_HasChildren
title: IUPnPDevice::get_HasChildren (upnp.h)
description: The HasChildren property specifies whether the device has any child devices.
helpviewer_keywords: ["IUPnPDevice interface [UPnP APIs]","get_HasChildren method","IUPnPDevice.get_HasChildren","IUPnPDevice::get_HasChildren","_upnp_iupnpdevice_haschildren","get_HasChildren","get_HasChildren method [UPnP APIs]","get_HasChildren method [UPnP APIs]","IUPnPDevice interface","upnp.iupnpdevice_haschildren","upnp/IUPnPDevice::get_HasChildren"]
old-location: upnp\iupnpdevice_haschildren.htm
tech.root: upnp
ms.assetid: 18a7c7e0-389d-4fc4-b98c-4eb1afea4a7e
ms.date: 12/05/2018
ms.keywords: IUPnPDevice interface [UPnP APIs],get_HasChildren method, IUPnPDevice.get_HasChildren, IUPnPDevice::get_HasChildren, _upnp_iupnpdevice_haschildren, get_HasChildren, get_HasChildren method [UPnP APIs], get_HasChildren method [UPnP APIs],IUPnPDevice interface, upnp.iupnpdevice_haschildren, upnp/IUPnPDevice::get_HasChildren
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
 - IUPnPDevice::get_HasChildren
 - upnp/IUPnPDevice::get_HasChildren
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
 - IUPnPDevice.get_HasChildren
---

# IUPnPDevice::get_HasChildren


## -description

The 
<b>HasChildren</b> property specifies whether the device has any child devices.

## -parameters

### -param pvarb [out]

Receives a reference to a <b>VARIANT_BOOL</b> that contains the value VARIANT_TRUE if the device has one or more child devices; otherwise, it contains the value VARIANT_FALSE.

## -returns

For C++: If this property's "get" method succeeds, the return value is S_OK. Otherwise, the method returns one of the COM error codes defined in WinError.h.

## -remarks

Use this property to determine whether or not the application should access the <a href="/windows/desktop/api/upnp/nf-upnp-iupnpdevice-get_children">IUPnPDevice::Children</a> property.

## -see-also

<a href="/windows/desktop/api/upnp/nn-upnp-iupnpdevice">IUPnPDevice</a>



<a href="/windows/desktop/api/upnp/nf-upnp-iupnpdevice-get_children">IUPnPDevice::Children</a>