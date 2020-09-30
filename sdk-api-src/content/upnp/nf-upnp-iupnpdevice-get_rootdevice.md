---
UID: NF:upnp.IUPnPDevice.get_RootDevice
title: IUPnPDevice::get_RootDevice (upnp.h)
description: The RootDevice property specifies the topmost device in the device tree. The root device represents a physical object.
helpviewer_keywords: ["IUPnPDevice interface [UPnP APIs]","get_RootDevice method","IUPnPDevice.get_RootDevice","IUPnPDevice::get_RootDevice","_upnp_iupnpdevice_rootdevice","get_RootDevice","get_RootDevice method [UPnP APIs]","get_RootDevice method [UPnP APIs]","IUPnPDevice interface","upnp.iupnpdevice_rootdevice","upnp/IUPnPDevice::get_RootDevice"]
old-location: upnp\iupnpdevice_rootdevice.htm
tech.root: upnp
ms.assetid: 6c6d1782-693a-4b23-b9e0-7e379ba7f96c
ms.date: 12/05/2018
ms.keywords: IUPnPDevice interface [UPnP APIs],get_RootDevice method, IUPnPDevice.get_RootDevice, IUPnPDevice::get_RootDevice, _upnp_iupnpdevice_rootdevice, get_RootDevice, get_RootDevice method [UPnP APIs], get_RootDevice method [UPnP APIs],IUPnPDevice interface, upnp.iupnpdevice_rootdevice, upnp/IUPnPDevice::get_RootDevice
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
 - IUPnPDevice::get_RootDevice
 - upnp/IUPnPDevice::get_RootDevice
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
 - IUPnPDevice.get_RootDevice
---

# IUPnPDevice::get_RootDevice


## -description

The 
<b>RootDevice</b> property specifies the topmost device in the device tree. The root device represents a physical object.

## -parameters

### -param ppudRootDevice [out]

Receives a reference to an 
<a href="/windows/desktop/api/upnp/nn-upnp-iupnpdevice">IUPnPDevice</a> object that describes the root device. This reference must be released when it is no longer required.

## -returns

For C++: If this property's "get" method succeeds, the return value is S_OK. Otherwise, the method returns one of the COM error codes defined in WinError.h.

## -see-also

<a href="/windows/desktop/api/upnp/nn-upnp-iupnpdevice">IUPnPDevice</a>



<a href="/windows/desktop/api/upnp/nf-upnp-iupnpdevice-get_isrootdevice">IUPnPDevice::IsRootDevice</a>