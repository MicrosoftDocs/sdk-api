---
UID: NF:upnp.IUPnPDevice.get_IsRootDevice
title: IUPnPDevice::get_IsRootDevice (upnp.h)
description: The IsRootDevice property specifies whether the device is the topmost device in the device tree.
helpviewer_keywords: ["IUPnPDevice interface [UPnP APIs]","get_IsRootDevice method","IUPnPDevice.get_IsRootDevice","IUPnPDevice::get_IsRootDevice","_upnp_iupnpdevice_isrootdevice","get_IsRootDevice","get_IsRootDevice method [UPnP APIs]","get_IsRootDevice method [UPnP APIs]","IUPnPDevice interface","upnp.iupnpdevice_isrootdevice","upnp/IUPnPDevice::get_IsRootDevice"]
old-location: upnp\iupnpdevice_isrootdevice.htm
tech.root: upnp
ms.assetid: 0416c4f0-1289-4e91-be34-23f8b80df5c3
ms.date: 12/05/2018
ms.keywords: IUPnPDevice interface [UPnP APIs],get_IsRootDevice method, IUPnPDevice.get_IsRootDevice, IUPnPDevice::get_IsRootDevice, _upnp_iupnpdevice_isrootdevice, get_IsRootDevice, get_IsRootDevice method [UPnP APIs], get_IsRootDevice method [UPnP APIs],IUPnPDevice interface, upnp.iupnpdevice_isrootdevice, upnp/IUPnPDevice::get_IsRootDevice
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
 - IUPnPDevice::get_IsRootDevice
 - upnp/IUPnPDevice::get_IsRootDevice
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
 - IUPnPDevice.get_IsRootDevice
---

# IUPnPDevice::get_IsRootDevice


## -description

The 
<b>IsRootDevice</b> property specifies whether the device is the topmost device in the device tree.

## -parameters

### -param pvarb [out]

Receives a reference to a <b>VARIANT_BOOL</b> that contains the value VARIANT_TRUE if the device is the topmost device in the device tree; otherwise, it contains the value VARIANT_FALSE.

## -returns

For C++: If this property's "get" method succeeds, the return value is S_OK. Otherwise, the method returns one of the COM error codes defined in WinError.h.

## -see-also

<a href="/windows/desktop/api/upnp/nn-upnp-iupnpdevice">IUPnPDevice</a>



<a href="/windows/desktop/api/upnp/nf-upnp-iupnpdevice-get_children">IUPnPDevice::Children</a>



<a href="/windows/desktop/api/upnp/nf-upnp-iupnpdevice-get_rootdevice">IUPnPDevice::RootDevice</a>