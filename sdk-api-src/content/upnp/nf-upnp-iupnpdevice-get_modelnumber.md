---
UID: NF:upnp.IUPnPDevice.get_ModelNumber
title: IUPnPDevice::get_ModelNumber (upnp.h)
description: The ModelNumber property specifies a human-readable form of the model number of the device.
helpviewer_keywords: ["IUPnPDevice interface [UPnP APIs]","get_ModelNumber method","IUPnPDevice.get_ModelNumber","IUPnPDevice::get_ModelNumber","_upnp_iupnpdevice_modelnumber","get_ModelNumber","get_ModelNumber method [UPnP APIs]","get_ModelNumber method [UPnP APIs]","IUPnPDevice interface","upnp.iupnpdevice_modelnumber","upnp/IUPnPDevice::get_ModelNumber"]
old-location: upnp\iupnpdevice_modelnumber.htm
tech.root: upnp
ms.assetid: 7e9b92a6-efad-41f0-b083-a2fed0f70c8b
ms.date: 12/05/2018
ms.keywords: IUPnPDevice interface [UPnP APIs],get_ModelNumber method, IUPnPDevice.get_ModelNumber, IUPnPDevice::get_ModelNumber, _upnp_iupnpdevice_modelnumber, get_ModelNumber, get_ModelNumber method [UPnP APIs], get_ModelNumber method [UPnP APIs],IUPnPDevice interface, upnp.iupnpdevice_modelnumber, upnp/IUPnPDevice::get_ModelNumber
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
 - IUPnPDevice::get_ModelNumber
 - upnp/IUPnPDevice::get_ModelNumber
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
 - IUPnPDevice.get_ModelNumber
---

# IUPnPDevice::get_ModelNumber


## -description

The 
<b>ModelNumber</b> property specifies a human-readable form of the model number of the device.

## -parameters

### -param pbstr [out]

Receives a reference to a string that contains the model number. Release this string with <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a> when it is no longer required. If the device does not specify a model number, this parameter is set to <b>NULL</b>.

## -returns

For C++: If this property's "get" method succeeds, the return value is S_OK. If the device does not specify a model number, the return value is S_FALSE and <i>pbstr</i> is <b>NULL</b>. Otherwise, the method returns one of the COM error codes defined in WinError.h.

## -remarks

This property is optional and <i>pbstr</i> can return <b>NULL</b>.

## -see-also

<a href="/windows/desktop/api/upnp/nn-upnp-iupnpdevice">IUPnPDevice</a>



<a href="/windows/desktop/api/upnp/nf-upnp-iupnpdevice-get_modelname">IUPnPDevice::ModelName</a>



<a href="/windows/desktop/api/upnp/nf-upnp-iupnpdevice-get_modelurl">IUPnPDevice::ModelURL</a>