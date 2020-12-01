---
UID: NF:upnp.IUPnPDevice.get_ManufacturerName
title: IUPnPDevice::get_ManufacturerName (upnp.h)
description: The ManufacturerName property specifies a human-readable form of the manufacturer name of the device.
helpviewer_keywords: ["IUPnPDevice interface [UPnP APIs]","get_ManufacturerName method","IUPnPDevice.get_ManufacturerName","IUPnPDevice::get_ManufacturerName","_upnp_iupnpdevice_manufacturername","get_ManufacturerName","get_ManufacturerName method [UPnP APIs]","get_ManufacturerName method [UPnP APIs]","IUPnPDevice interface","upnp.iupnpdevice_manufacturername","upnp/IUPnPDevice::get_ManufacturerName"]
old-location: upnp\iupnpdevice_manufacturername.htm
tech.root: upnp
ms.assetid: b62ba17d-4d0f-4609-ae34-0d8bd350f761
ms.date: 12/05/2018
ms.keywords: IUPnPDevice interface [UPnP APIs],get_ManufacturerName method, IUPnPDevice.get_ManufacturerName, IUPnPDevice::get_ManufacturerName, _upnp_iupnpdevice_manufacturername, get_ManufacturerName, get_ManufacturerName method [UPnP APIs], get_ManufacturerName method [UPnP APIs],IUPnPDevice interface, upnp.iupnpdevice_manufacturername, upnp/IUPnPDevice::get_ManufacturerName
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
 - IUPnPDevice::get_ManufacturerName
 - upnp/IUPnPDevice::get_ManufacturerName
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
 - IUPnPDevice.get_ManufacturerName
---

# IUPnPDevice::get_ManufacturerName


## -description

The 
<b>ManufacturerName</b> property specifies a human-readable form of the manufacturer name of the device.

## -parameters

### -param pbstr [out]

Receives a reference to a string that contains the manufacturer's name. Release this string with <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a> when it is no longer required.

## -returns

For C++: If this property's "get" method succeeds, the return value is S_OK. Otherwise, the method returns one of the COM error codes defined in WinError.h.

## -see-also

<a href="/windows/desktop/api/upnp/nn-upnp-iupnpdevice">IUPnPDevice</a>



<a href="/windows/desktop/api/upnp/nf-upnp-iupnpdevice-get_manufacturerurl">IUPnPDevice::ManufacturerURL</a>