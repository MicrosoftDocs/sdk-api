---
UID: NF:upnp.IUPnPDevice.get_ModelURL
title: IUPnPDevice::get_ModelURL (upnp.h)
description: The ModelURL property specifies the URL for a Web page that contains model-specific information for the device.
helpviewer_keywords: ["IUPnPDevice interface [UPnP APIs]","get_ModelURL method","IUPnPDevice.get_ModelURL","IUPnPDevice::get_ModelURL","_upnp_iupnpdevice_modelurl","get_ModelURL","get_ModelURL method [UPnP APIs]","get_ModelURL method [UPnP APIs]","IUPnPDevice interface","upnp.iupnpdevice_modelurl","upnp/IUPnPDevice::get_ModelURL"]
old-location: upnp\iupnpdevice_modelurl.htm
tech.root: upnp
ms.assetid: e9f3231a-5836-4629-9df5-6ed9184fb753
ms.date: 12/05/2018
ms.keywords: IUPnPDevice interface [UPnP APIs],get_ModelURL method, IUPnPDevice.get_ModelURL, IUPnPDevice::get_ModelURL, _upnp_iupnpdevice_modelurl, get_ModelURL, get_ModelURL method [UPnP APIs], get_ModelURL method [UPnP APIs],IUPnPDevice interface, upnp.iupnpdevice_modelurl, upnp/IUPnPDevice::get_ModelURL
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
 - IUPnPDevice::get_ModelURL
 - upnp/IUPnPDevice::get_ModelURL
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
 - IUPnPDevice.get_ModelURL
---

# IUPnPDevice::get_ModelURL


## -description

The 
<b>ModelURL</b> property specifies the URL for a Web page that contains model-specific information for the device.

## -parameters

### -param pbstr [out]

Receives a reference to a string that contains the URL. Release this string with <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a> when it is no longer required. If the device does not specify this URL, this parameter is set to <b>NULL</b>.

## -returns

For C++: If this property's "get" method succeeds, the return value is S_OK. If the device does not specify this URL, the return value is S_FALSE and <i>pbstr</i> is <b>NULL</b>. Otherwise, the method returns one of the COM error codes defined in WinError.h.

## -remarks

This property is optional and <i>pbstr</i> can be <b>NULL</b>.

## -see-also

<a href="/windows/desktop/api/upnp/nn-upnp-iupnpdevice">IUPnPDevice</a>



<a href="/windows/desktop/api/upnp/nf-upnp-iupnpdevice-get_modelname">IUPnPDevice::ModelName</a>



<a href="/windows/desktop/api/upnp/nf-upnp-iupnpdevice-get_modelnumber">IUPnPDevice::ModelNumber</a>