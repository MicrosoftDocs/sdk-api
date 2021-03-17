---
UID: NF:upnp.IUPnPDevice.get_Description
title: IUPnPDevice::get_Description (upnp.h)
description: The Description property specifies a human-readable summary of the device's functionality.
helpviewer_keywords: ["IUPnPDevice interface [UPnP APIs]","get_Description method","IUPnPDevice.get_Description","IUPnPDevice::get_Description","_upnp_iupnpdevice_description","get_Description","get_Description method [UPnP APIs]","get_Description method [UPnP APIs]","IUPnPDevice interface","upnp.iupnpdevice_description","upnp/IUPnPDevice::get_Description"]
old-location: upnp\iupnpdevice_description.htm
tech.root: upnp
ms.assetid: 99842f92-b57d-43fa-aa44-412f260b8af3
ms.date: 12/05/2018
ms.keywords: IUPnPDevice interface [UPnP APIs],get_Description method, IUPnPDevice.get_Description, IUPnPDevice::get_Description, _upnp_iupnpdevice_description, get_Description, get_Description method [UPnP APIs], get_Description method [UPnP APIs],IUPnPDevice interface, upnp.iupnpdevice_description, upnp/IUPnPDevice::get_Description
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
 - IUPnPDevice::get_Description
 - upnp/IUPnPDevice::get_Description
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
 - IUPnPDevice.get_Description
---

# IUPnPDevice::get_Description


## -description

The 
<b>Description</b> property specifies a human-readable summary of the device's functionality.

## -parameters

### -param pbstr [out]

Receives a reference to a string that contains a short description of the intended functionality of devices of this type. Release this string with <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a> when it is no longer required. If the device does not specify a description, this parameter is set to <b>NULL</b>.

## -returns

For C++: If this property's "get" method succeeds, the return value is S_OK. If the device does not specify this URL, the return value is S_FALSE and <i>pbstr</i> is <b>NULL</b>. Otherwise, the method returns one of the COM error codes defined in WinError.h.

## -remarks

This property is optional and <i>pbstr</i> can return <b>NULL</b>.

## -see-also

<a href="/windows/desktop/api/upnp/nn-upnp-iupnpdevice">IUPnPDevice</a>