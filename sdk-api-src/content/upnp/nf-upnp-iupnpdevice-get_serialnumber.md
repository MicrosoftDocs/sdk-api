---
UID: NF:upnp.IUPnPDevice.get_SerialNumber
title: IUPnPDevice::get_SerialNumber (upnp.h)
description: The SerialNumber property specifies a human-readable form of the serial number of the device.
helpviewer_keywords: ["IUPnPDevice interface [UPnP APIs]","get_SerialNumber method","IUPnPDevice.get_SerialNumber","IUPnPDevice::get_SerialNumber","_upnp_iupnpdevice_serialnumber","get_SerialNumber","get_SerialNumber method [UPnP APIs]","get_SerialNumber method [UPnP APIs]","IUPnPDevice interface","upnp.iupnpdevice_serialnumber","upnp/IUPnPDevice::get_SerialNumber"]
old-location: upnp\iupnpdevice_serialnumber.htm
tech.root: upnp
ms.assetid: de2f8594-a183-440a-aeb1-240cf0709e36
ms.date: 12/05/2018
ms.keywords: IUPnPDevice interface [UPnP APIs],get_SerialNumber method, IUPnPDevice.get_SerialNumber, IUPnPDevice::get_SerialNumber, _upnp_iupnpdevice_serialnumber, get_SerialNumber, get_SerialNumber method [UPnP APIs], get_SerialNumber method [UPnP APIs],IUPnPDevice interface, upnp.iupnpdevice_serialnumber, upnp/IUPnPDevice::get_SerialNumber
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
 - IUPnPDevice::get_SerialNumber
 - upnp/IUPnPDevice::get_SerialNumber
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
 - IUPnPDevice.get_SerialNumber
---

# IUPnPDevice::get_SerialNumber


## -description

The 
<b>SerialNumber</b> property specifies a human-readable form of the serial number of the device.

## -parameters

### -param pbstr [out]

Receives a reference to a string that contains the serial number. Release this string with <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a> when it is no longer used. This property is optional and the device may not have a serial number.

## -returns

For C++: If this property's "get" method succeeds, the return value is S_OK. If the device did not specify a serial number, the return value is S_FALSE. Otherwise, the method returns one of the COM error codes defined in WinError.h.

## -remarks

This property is optional and <i>pbstr</i> may be <b>NULL</b>.

It is possible for multiple devices to have the same serial number. To determine if two device objects describe the same device, use the unique device name. For more information, see 
<a href="/windows/desktop/api/upnp/nf-upnp-iupnpdevice-get_uniquedevicename">UniqueDeviceName</a>.

## -see-also

<a href="/windows/desktop/api/upnp/nn-upnp-iupnpdevice">IUPnPDevice</a>



<a href="/windows/desktop/api/upnp/nf-upnp-iupnpdevice-get_uniquedevicename">IUPnPDevice::UniqueDeviceName</a>