---
UID: NF:upnp.IUPnPDevice.get_UPC
title: IUPnPDevice::get_UPC (upnp.h)
description: The UPC property specifies a human-readable form of the product code.
helpviewer_keywords: ["IUPnPDevice interface [UPnP APIs]","get_UPC method","IUPnPDevice.get_UPC","IUPnPDevice::get_UPC","_upnp_iupnpdevice_upc","get_UPC","get_UPC method [UPnP APIs]","get_UPC method [UPnP APIs]","IUPnPDevice interface","upnp.iupnpdevice_upc","upnp/IUPnPDevice::get_UPC"]
old-location: upnp\iupnpdevice_upc.htm
tech.root: upnp
ms.assetid: 33349885-96da-47ef-9b09-83c2c332b509
ms.date: 12/05/2018
ms.keywords: IUPnPDevice interface [UPnP APIs],get_UPC method, IUPnPDevice.get_UPC, IUPnPDevice::get_UPC, _upnp_iupnpdevice_upc, get_UPC, get_UPC method [UPnP APIs], get_UPC method [UPnP APIs],IUPnPDevice interface, upnp.iupnpdevice_upc, upnp/IUPnPDevice::get_UPC
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
 - IUPnPDevice::get_UPC
 - upnp/IUPnPDevice::get_UPC
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
 - IUPnPDevice.get_UPC
---

# IUPnPDevice::get_UPC


## -description

The 
<b>UPC</b> property specifies a human-readable form of the product code.

## -parameters

### -param pbstr [out]

Receives a reference to a string that contains the product code. Release this string with <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a> when it is no longer required. If the device does not specify a product code, this parameter receives an empty string.

## -returns

For C++: If this property's "get" method succeeds, the return value is S_OK. If the device did not specify a product code, the return value is S_FALSE. Otherwise, the method returns one of the COM error codes defined in WinError.h.

## -remarks

This property is optional and <i>pbstr</i> may be <b>NULL</b>.

It is possible for multiple devices to have the same product code. To determine if two device objects describe the same device, use the unique device name. For more information, see 
<a href="/windows/desktop/api/upnp/nf-upnp-iupnpdevice-get_uniquedevicename">UniqueDeviceName</a>.

## -see-also

<a href="/windows/desktop/api/upnp/nn-upnp-iupnpdevice">IUPnPDevice</a>



<a href="/windows/desktop/api/upnp/nf-upnp-iupnpdevice-get_uniquedevicename">IUPnPDevice::UniqueDeviceName</a>