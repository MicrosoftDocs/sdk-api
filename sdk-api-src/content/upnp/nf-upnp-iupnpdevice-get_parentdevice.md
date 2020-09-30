---
UID: NF:upnp.IUPnPDevice.get_ParentDevice
title: IUPnPDevice::get_ParentDevice (upnp.h)
description: The ParentDevice property specifies the parent of the device.
helpviewer_keywords: ["IUPnPDevice interface [UPnP APIs]","get_ParentDevice method","IUPnPDevice.get_ParentDevice","IUPnPDevice::get_ParentDevice","_upnp_iupnpdevice_parentdevice","get_ParentDevice","get_ParentDevice method [UPnP APIs]","get_ParentDevice method [UPnP APIs]","IUPnPDevice interface","upnp.iupnpdevice_parentdevice","upnp/IUPnPDevice::get_ParentDevice"]
old-location: upnp\iupnpdevice_parentdevice.htm
tech.root: upnp
ms.assetid: 662a0bda-32f5-4756-8851-e7b2d0b9cc44
ms.date: 12/05/2018
ms.keywords: IUPnPDevice interface [UPnP APIs],get_ParentDevice method, IUPnPDevice.get_ParentDevice, IUPnPDevice::get_ParentDevice, _upnp_iupnpdevice_parentdevice, get_ParentDevice, get_ParentDevice method [UPnP APIs], get_ParentDevice method [UPnP APIs],IUPnPDevice interface, upnp.iupnpdevice_parentdevice, upnp/IUPnPDevice::get_ParentDevice
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
 - IUPnPDevice::get_ParentDevice
 - upnp/IUPnPDevice::get_ParentDevice
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
 - IUPnPDevice.get_ParentDevice
---

# IUPnPDevice::get_ParentDevice


## -description

The 
<b>ParentDevice</b> property specifies the parent of the device.

## -parameters

### -param ppudDeviceParent [out]

Receives a reference to an 
<a href="/windows/desktop/api/upnp/nn-upnp-iupnpdevice">IUPnPDevice</a> object that describes the parent device. This reference must be released when it is no longer required. If the device has no parent, it is a topmost device, and the parameter receives <b>NULL</b>.

## -returns

For C++: If this property's "get" method succeeds, the return value is S_OK. If the device is a topmost device, the return value is S_FALSE. Otherwise, the method returns one of the COM error codes defined in WinError.h.

## -remarks

To determine if the device has no parent, use <a href="/windows/desktop/api/upnp/nf-upnp-iupnpdevice-get_isrootdevice">IUPnPDevice::IsRootDevice</a>.

## -see-also

<a href="/windows/desktop/api/upnp/nn-upnp-iupnpdevice">IUPnPDevice</a>



<a href="/windows/desktop/api/upnp/nf-upnp-iupnpdevice-get_children">IUPnPDevice::Children</a>