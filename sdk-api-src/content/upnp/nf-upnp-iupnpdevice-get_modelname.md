---
UID: NF:upnp.IUPnPDevice.get_ModelName
title: IUPnPDevice::get_ModelName (upnp.h)
description: The ModelName property specifies a human-readable form of the model name of the device.
helpviewer_keywords: ["IUPnPDevice interface [UPnP APIs]","get_ModelName method","IUPnPDevice.get_ModelName","IUPnPDevice::get_ModelName","_upnp_iupnpdevice_modelname","get_ModelName","get_ModelName method [UPnP APIs]","get_ModelName method [UPnP APIs]","IUPnPDevice interface","upnp.iupnpdevice_modelname","upnp/IUPnPDevice::get_ModelName"]
old-location: upnp\iupnpdevice_modelname.htm
tech.root: upnp
ms.assetid: c71868ab-e05d-4e6a-b157-4474afc8f61f
ms.date: 12/05/2018
ms.keywords: IUPnPDevice interface [UPnP APIs],get_ModelName method, IUPnPDevice.get_ModelName, IUPnPDevice::get_ModelName, _upnp_iupnpdevice_modelname, get_ModelName, get_ModelName method [UPnP APIs], get_ModelName method [UPnP APIs],IUPnPDevice interface, upnp.iupnpdevice_modelname, upnp/IUPnPDevice::get_ModelName
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
 - IUPnPDevice::get_ModelName
 - upnp/IUPnPDevice::get_ModelName
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
 - IUPnPDevice.get_ModelName
---

# IUPnPDevice::get_ModelName


## -description

The 
<b>ModelName</b> property specifies a human-readable form of the model name of the device.

## -parameters

### -param pbstr [out]

Receives a reference to a string that contains the model name. Release this string with <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a> when it is no longer required.

## -returns

For C++: If this property's "get" method succeeds, the return value is S_OK. Otherwise, the method returns one of the COM error codes defined in WinError.h.

## -see-also

<a href="/windows/desktop/api/upnp/nn-upnp-iupnpdevice">IUPnPDevice</a>



<a href="/windows/desktop/api/upnp/nf-upnp-iupnpdevice-get_modelnumber">IUPnPDevice::ModelNumber</a>



<a href="/windows/desktop/api/upnp/nf-upnp-iupnpdevice-get_modelurl">IUPnPDevice::ModelURL</a>