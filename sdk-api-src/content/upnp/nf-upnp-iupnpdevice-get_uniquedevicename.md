---
UID: NF:upnp.IUPnPDevice.get_UniqueDeviceName
title: IUPnPDevice::get_UniqueDeviceName (upnp.h)
description: The UniqueDeviceName property specifies the unique device name (UDN) of the device. A UDN is unique; no two devices can have the same UDN.
helpviewer_keywords: ["IUPnPDevice interface [UPnP APIs]","get_UniqueDeviceName method","IUPnPDevice.get_UniqueDeviceName","IUPnPDevice::get_UniqueDeviceName","_upnp_iupnpdevice_uniquedevicename","get_UniqueDeviceName","get_UniqueDeviceName method [UPnP APIs]","get_UniqueDeviceName method [UPnP APIs]","IUPnPDevice interface","upnp.iupnpdevice_uniquedevicename","upnp/IUPnPDevice::get_UniqueDeviceName"]
old-location: upnp\iupnpdevice_uniquedevicename.htm
tech.root: upnp
ms.assetid: ca644bd3-6580-44da-87f5-11d543814043
ms.date: 12/05/2018
ms.keywords: IUPnPDevice interface [UPnP APIs],get_UniqueDeviceName method, IUPnPDevice.get_UniqueDeviceName, IUPnPDevice::get_UniqueDeviceName, _upnp_iupnpdevice_uniquedevicename, get_UniqueDeviceName, get_UniqueDeviceName method [UPnP APIs], get_UniqueDeviceName method [UPnP APIs],IUPnPDevice interface, upnp.iupnpdevice_uniquedevicename, upnp/IUPnPDevice::get_UniqueDeviceName
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
 - IUPnPDevice::get_UniqueDeviceName
 - upnp/IUPnPDevice::get_UniqueDeviceName
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
 - IUPnPDevice.get_UniqueDeviceName
---

# IUPnPDevice::get_UniqueDeviceName


## -description

The 
<b>UniqueDeviceName</b> property specifies the unique device name (UDN) of the device. A UDN is unique; no two devices can have the same UDN.

## -parameters

### -param pbstr [out]

Receives a reference to a string that contains the UDN of the device. Release this string with <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a> when it is no longer required.

## -returns

For C++: If this property's "get" method succeeds, the return value is S_OK. Otherwise, the method returns one of the COM error codes defined in WinError.h.

## -see-also

<a href="/windows/desktop/api/upnp/nn-upnp-iupnpdevice">IUPnPDevice</a>